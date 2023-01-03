+++ 
draft = false
date = "2017-09-20T15:00:00-04:00"
title = "Agile Project Management in Google Sheets"
slug = "" 
description = """
  Many small teams spend a lot of time and money on agile project management
  software. However, you can get a majority of the same function from free tools
  like Google Sheets.
"""
aliases = [
  "/post/google-slides-agile/"
]
+++

I think its way to hard to manage small projects.
There are so many project planning platforms out there and they typically fall into one of two major pitfalls for small teams.
Either they are free and simplistic, i.e. [Trello](https://trello.com/), or they are expensive and complicated, i.e. [Jira](https://www.atlassian.com/software/jira).

Of course, there are millions of people who make these systems work for them everyday, but in my experience I find that it is hard for a small, well-intentioned group to actually use these.
In the case of more simplistic tools, it seems like even a few collaborators can quickly clutter even the best laid system of Trello boards.
Additionally, in the case of enterprise tools, I worry that management overhead quickly absorbs what should be a lean and organic work environment.
This puts aside the point that many groups of this size are either amateurs or academic projects which work on a nonexistent budget.

So I recently looked through at least a dozen potential solutions, and the truth is, Google Sheets may really be the best answer.

![A burndown chart](/img/posts/agile_development_in_google_sheets/burndown.png)

I know it seems like I've found a hammer and I'm just going around looking for nails, but don't dismiss me too fast.
Small groups working on projects of any decent size need some sort of structure to keep on track.
They need a way to track each member's progress, and they need to know their project is on course.
Most importantly, they really don't want to waste a week fiddling around chrome extensions that promise to revolutionize their Trello experience, and they don't want to put money down for a digital manager before a single line of code is written.

**To make it even easier for small groups, I've gone ahead and made that Google Sheet for them!**
[Click Here for a Template](https://docs.google.com/spreadsheets/d/1MfuBr9Aw26RMycB0cB2hWwQ8kErLMgJk0KzflRpUsz4/edit?usp=sharing)

The above template does a remarkable number of things, all you need to do is change the names around.
For one, it manages sprints, just duplicate the existing sprint page.
On each sprint, all you have to is change the start date and the duration and the burndown chart will be resized for you.
Then, you can fill in tasks, estimate work times, and priorities.

As you complete tasks, just mark them as done and set the completion date.
This will automatically be reflected in the given burndown chart.
The chart is smart enough to only include data up to the current date, and will automatically progress over time.
You even get to see how your project's trend compares with the ideal trend.

Most importantly, you can make tweaks pretty quickly if this template doesn't do something your team needs.
To put this in perspective, this whole template only took me about an hour to throw together.

Hopefully this save you some time, and gives you a quick and dirty way to start planning your sprints today!

