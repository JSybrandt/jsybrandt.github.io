+++ 
draft = false
date = "2017-11-06T23:18:26-04:00"
title = "Producer and Consumer Model in C++"
slug = "" 
description = """
  Describes a pattern to write really easy parallel code using tasks in OpenMP.
"""
aliases = [
  "/post/producer-consumer-openmp-cpp/"
]
+++

So recently, I needed to parallelize a lot of my old code.
This initially seemed like a daunting task.
Now its not like I've never had to write parallel code before, and its not like my task was that hard.
My issue primarily came from a staunch unwillingness to look anything up.
After all, I could just throw my problem into python, right?

While that may be true, the version of myself today would like to tell the version of myself from last week that the C++ solution is not as bad as I thought.

## The Task

I have a file with 40 million lines, and I have to parse and run a calculation on each.
There are no dependencies between these lines, and the whole thing is just encoded as plain text. A line consists of an id followed by 500 floats, representing a vector in $\Re^{500}$. I just wanted to load each vector and compute two distances.
Based on those distances, I would either keep the vector or throw it away.

Sequentially, this took forever.

## The Problem

There are two synchronization points in this task.
Firstly, each line from the file must be read sequentially.
Because the lines are of variable length, I can't do any fancy parallel file system tricks to make loading faster.
Secondly, the resulting data structure, my collection of selected vectors, needs to be protected so two different threads don't try to modify it at the same time.

This means firstly that only a single thread can read from the time at a time, and only a single thread can store its results at a time.
That being said, we are only going to be saving a small fraction of the total vectors.
Also, other threads shouldn't have to wait while the reading thread actually _parses_ the input.

So the idea is pretty simple.
One thread should read from the data file, extracting each line as fast as possible.
We will call this the __producer__ thread because it produces work.
The __consumer__ threads will be all other threads.

Whenever a new line is found, one of the available threads should take it and start parsing.
Once parsed, the thread can independently do its distance calculations.
If the conditions are right, then the thread should get a lock on the data structure, store its result, and repeat.

In python that's pretty much as easy as:

```python
pool.map(doWork, [line for line in file])
# Note: This line doesn't do EXACTLY what I just described, but you get the gist.
```

How on earth do you do that in C++?

## The C++ Solution

Okay, we are going to use [OpenMP](http://www.openmp.org/) and their _#pragma_ statements.
For unfamiliar readers, these are statements that the compiler will use to do a lot of the gritty parallel work for us.
For the semi-familiar readers, you probably do something like this:

```c++
#pragma omp parallel for
for(unsigned int i = 0; i < N; ++i){
  //Make Magic Happen
}
```

The above code block says _"Do the following for loop in parallel"_.
Unsurprisingly, each iteration of the for loop is done be a different thread.
Unfortunately, there is no single _#pragma_ statement for our little producer-consumer idea described above.
That said, its easier than you might think.

The code looks a little something like this:

```c++
DataStructure data;
ifstream fileStream;
string line;

// ...

#pragma omp parallel
{
#pragma omp single
  {
    while(getline(fileStream, line)){
#pragma omp task firstprivate(line)
      {
        Vector vec(line); // Parse line
        // Get Work Done
        if(condition_met){
#pragma omp critical
          data.add(line);
        }
      }
    }
  }
}
```

So whats going on?

First thing first, we get our data setup before the _#pragma_ nonsense.
This is because once we enter these _#pragma_ statements, we are going to be in a new scope, and we won't be able to get the data back out. We enter the new scope with:

```c++
#pragma omp parallel
{
  // Everything here is run in parallel.
}
```

This says that the following block will be run using all the threads available on the system.
What confused me at first is that the next line seems to say the opposite:

```c++
#pragma omp single
{
  // Everything here is run by one thread.
}
```

This line says that the following block will be run on only __one__ of the many threads.
Whats important to note here is that the remaining threads still exist, and are waiting for work.
Its this _#pragma_ which allows us to set up our __producer__.
We get our __consumers__ with this:

```c++
#pragma omp task
{
  // A new thread takes this work.
}
```

This statement creates work for a __consumer__ to take on.
Our single producer thread creates a new task every time they enter the body of our loop.
The option __firstprivate(line)__ specifies that each task should copy over its own version of the __line__ variable.
That way, each thread doesn't need to worry about it when the __producer__ gets a new line.

Finally, we use the following to protect our data structure:
```c++
#pragma omp critical
{
  // Only one thread can run this at a time.
}
```

By using the __critical__ keyword, we specify that only one thread is allowed to write to our data structure at a time.


And that's it!
Who knew it was so easy to set this up?
All we need to do now is compile our code with the _-fopenmp_ flag and we are off to the races.
I was able to use a 64 core machine at 100% using this method!
Hope this helps you too.



