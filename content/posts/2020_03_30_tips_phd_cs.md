+++
draft = false
date = 2020-03-29T13:42:36-04:00
title = "Tips for Succeeding in a CS Ph.D."
slug = ""
description = """
  Or: Things I Wish I Knew Four Years Ago.
  A collection of lessons that took me longer to learn than I would have liked.
  Much of these are the soft skills needed to survive a Ph.D.
"""
aliases = [
]
+++

Now that I am wrapping up my Ph.D., an endeavor that has defined my last four
years, it seems as good a time as any to take stock of the advice I've given and
received. I'm recording this mostly for myself, in hopes that a few years from
now I might do this again and compare notes. However, I also hope that if any
up-and-coming grad students stumble on this list, maybe it might do some good.
Also, given there's a pandemic outside, this seems as good a time as any to wax
philosophical.

I did my best to only include information I found useful. I'm very aware that a
lot of this advice is contradictory, at least in part. Take all of this with a
grain of salt. I am graduating from Clemson University with a Ph.D. in computer
science, a focus on machine learning, and will be starting a career in industry.
While I hope you find this information useful, results may vary.  I find advice
like this to be better interpreted as a set of proverbs, rather than a set of
rules. Following all of it is probably impossible, but following none of it
probably won't work out.

## Other People's Good Ideas

Looking back on the last four years, I've internalized a lot of advice that I
lean on pretty frequently. At this point, I can't really tell whether its
something I've come up with, something an adviser said, or something I read
online. While I've done my best to credit others where possible, I certainly
don't want to take credit unduly. Additionally, I don't want to do you, the
reader, a disservice by poorly restating someone else's advice. So maybe now is
a good point to tab over to [Matt Might's articles][matt_might_articles], and
specifically read through the [Illustrated Ph.D.][matt_might_illustrated_phd]
and [Why Ph.D. Students Fail][matt_might_why_phd_students_fail]. Furthermore, if
you can grab a copy, I really recommend skimming [The Pragmatic
Programmer][the_pragmatic_programmer] (here's a [list of the tips from that
book][pragmatic_programmer_tips] if you can't find a copy). Having recently
revisited these sources, I was amazed to see so many tidbits that I've repeated
over and over originated here.

For instance, the Pragmatic Programmer drills in right away that good programmer
as those who:

{{% callout title="Care About Craft."%}}
Why spend your life ~~developing software~~ _pursuing this degree_ unless you care
about doing it well?
{{%/callout %}}

This applies doubly to Ph.D. students. I found it incredibly important to strive
for best practices. The more rigorous your procedures, the greater rationale you
will develop to support your choices. You need a rational for your choices. At
first, your adviser will ask about them, and eventually your reviewers and
conference attendees will challenge them a lot less nicely. Developing a craft,
and understanding the tools you use, the algorithms you choose, and the software
systems you rely on will all have consequences to your conclusions. Be aware of
them.

Now, all of the above references above discuss the mechanics of research and
programming.  However, you will quickly find, as a new Ph.D. student, that your
endeavor will require a whole set of soft skills---writing, speaking, teaching,
and presenting. At a high level, this means you need to:

{{% callout title="Put a high weight on soft skills."%}}
If a paper gets published in a journal, and no one is there to read it, does it
make an impact?
{{% /callout %}}

Like falling trees, publications are only important if observed. There are a
range of ways to increase the probability that someone observes your work.
Firstly, you need to do good research. But, once you have that fated plot that
demonstrates the potential benefit of your wonderful new idea, you still have a
lot of work to do. The first soft skill in this process is writing. I was given
[Strunk & White][strunk_and_white] and picked up [On Writing
Well][on_writing_well] really early in my grad-student career. The former is a
list of practical writing tips stated clearly enough for me (a CS student) to
figure out. The second is a little softer, and expands on the intuitions behind
those tips. Sure, they are written from the perspective of writing nonfiction
broadly, but those principles are foundational to scientific writing.

This is particularly important because:

{{% callout title="You're here to write papers, not software."%}}
Researchers are evaluated by $h$-index, not lines of code. Sure, you need to
write code to get a high $h$-index, but good papers are published with terrible
software all the time.
{{% /callout %}}

There is a lot of truth regarding the above tip, which I received from my
undergraduate adviser before starting my Ph.D., but I would recommend not
following this one all the way. Surely, I have seen some terrible research code,
but for any project lasting more than a couple of months, or exploring more than
one research topics, you're going to be revisiting and revising often. As a
result, you should find a balance around the mantra "good enough is good
enough." I have a lot more to stay on the practice of writing research software
(its hard), but that's probably going to have to wait for another post.

Unlike these references on writing, I've never come across good works on
presentations. However, a professor I had in undergrad gave me some
really good advice:

{{% callout title="No more than 5 points per slide, no more than 5 words per point, use pictures whenever possible."%}}
Your audience is not there to read. You wrote a whole paper that already
explains those details.
{{% /callout %}}

This point is a little controversial, but I'm firmly in the camp that simpler
presentations are more effective than complex ones. The other side of this
argument believes that if someone comes across your slides published online,
they should still be able to read all of the key points of your talk, without
you actually there to speak. This is flawed logic. The vehicle to present your
work in written form is the research paper, so why shoehorn a presentation to
act as a redundant version of that? Instead, your presentation should provide
_only_ the scaffolding necessary to give your talk---the bent wire on which you
will add clay from behind a podium.

The reason you want simpler slides is because you do not want to confuse your
viewers. A paragraph of text screams "read me!" So, many in your audience will
start to read, which necessarily means they will cease to listen. In contrast,
without _any_ text, your audience will not know what aspects of your dialog are
the most important, what words are going to have implications later in the talk,
or what take-aways they should dwell on. The correct balance is achieved through
short sentence fragments. Distill a complex thought, such as "Algebraic distance
is an iterative relaxation process that places each node in the input graph on
the unit interval," to "Algebraic Distance: Iterative relaxation process.
Assigns nodes coordinates in $[0,1]$." _New slide._

## Lessons Learned

As previously stated, I don't want to take credit for any of my own advice. If
you find this useful, I'm probably forgetting where I heard these tips from.
However, a sign that I made these up myself would be if you think they're
totally off base.

To start, I want to focus on the research process itself:

{{% callout title="Limit Complexity"%}}
If $X$ is a problem, are we going to publish a whole paper on $X$, or do we just
need a solution to $X$ in order to publish a paper on $Y$?
{{% /callout %}}

Research papers are fundamentally argumentative writing. You spend months coming
up with ideas and running experiments to collect evidence in support of your
hypothesis that your reviewers will be (correctly) biased against. Therefore,
you must _convince_ a reader by building from a set of accepted propositions and
experimentally backed claims. The more your argument relies on these accepted
prepositions, the less burden you place on experiments. Every time you come up
with a _special_ solution, you will also be expected to defend your choice. As a
result, your whole research project should only contain __ONE__ special
solution.

Here's a concrete example. Imagine we have a new idea for a centrality measure
for nearest-neighbors graphs, and we want to try it out on a particularly large
and high-dimensional dataset. The new grad student may run into a number of
problems simply creating a nearest-neighbors graph from this large dataset. This
is an example of a problem that you need to solve _before_ doing any research.
At this point, the grad student might think of a special case of hashing
function to help construct this nearest-neighbors graph. This very likely is a
bad idea. The reasons for this can be briefly summarized as:

{{% callout title="Corollary: Don't Reinvent the Wheel."%}}
It sounds so simple, but it turns out there's a lot of wheels out there.
{{% /callout %}}

If the grad student can provide a citation for the locality-sensitive hashing
function they have used, then this technique becomes a proposition to their
ultimate argument. If they cannot, a good reviewer will ask "why that function
and not another?" At that point, the grad student might have to run multiple
experiments using a range of potential hashing functions. In effect, the
sub-problem of constructing a large nearest-neighbors network has become a
central point to the work. No one wanted this, especially because there are
_many_ existing ways to construct large nearest-neighbors networks (and there
are probably _many_ ways to solve _your_ sub problem too). So take some time
searching [Google Scholar][google_scholar] and [GitHub][github] before embarking
on a sub problem.

If the reason we want to limit complexity is because we want to create arguments
that are easier to defend, then this means that our whole research process
should be built around defending our day-to-day choice. It is for this reason
that I think its so important to:

{{< callout title="Take notes">}}
If you ask 5 Ph.D. students about note taking, you're going to hear 6
strategies. However, you should have some strategy.
{{< /callout >}}

Notes are incredibly important to help your day-to-day decision making. You
should be able to respond to the question "why did you do that?" or "what else
did you try?" by opening your notes, turning to that date, and reciting whats
there. This means you're going to be taking notes with the knowledge that you
probably will only reference 1\% of the notes you ever write, but that 1\% is so
valuable that you're going to have to build a habit.

Everyone learns differently, and it takes a long time to create a craft around
note taking. My exploration converged to [bullet journals][bullet_journals]
written in cheap paper notebooks with a nice pen. I start each day by hand
writing the date, and reviewing the todo list of that has been recorded over the
last few days. I try to add a line for every task I start, stop, change, or
think of. This way, when asked a question, I can find the date I worked on
whatever it is, see the work I did that day, and any results that may have
influenced my thinking.

## Working with Others

At some point, you're going to be in a room with someone who wants you to work
on their project. Your adviser might have put you there, or a friend is going to
pitch something over lunch. Regardless, I learned the hard way that collaborating
in computer science has some pitfalls. I wish that I had started my Ph.D.
thinking:

{{< callout title="If you're going to help, be a helper.">}}
If you have a choice, don't agree to work you don't want to follow through with.
If you don't have a choice, the work is not going anywhere. In either case, if
you agree to help someone, help them wholeheartedly.
{{< /callout >}}

I got this idea partially from [Lean In][lean_in] wherein Sheryl Sandberg
describes hiring someone because instead of thinking about how the job could
benefit the candidate's career, the candidate instead wanted to learn what
problems Sandberg was facing in order to see if they could help.

This is how you should approach collaborations, if you are going to collaborate.
Hopefully, the reason this collaboration makes sense is because you have already
obtained some expertise needed by a colleague. If things go well, with
relatively little extra work on your part, this could turn into a paper with
your name on it. But, this also means that you need to be flexible, and focus
more on the problems and timeline of your peers, rather than your own personal
research objectives.

It is exceptionally rare for collaborations to align with your own personal
research direction, unless you or your adviser are the one's searching for
teammates. This means that you must:

{{< callout title="Beware trivial collaborations." >}}
You should ultimately feel like you are gaining something from a collaborative
work, even if it is only your name on a paper outside of your field. Do not
agree to be tech support.
{{< /callout >}}

For every fruitful collaboration, there are a number of dangerous time sinks.
Most collaborations are not along your critical path to a Ph.D. These
extra-circulars can be very interesting and provide a new perspective on your
work, and in this case you should be the best helper you can be. If instead you
are asked to "write some code" or  "run some experiments" you should be weary.
Your selfish goal is to learn and gain expertise. Furthermore, your altruistic
goal is to apply your expertise to help other's gain their own. No one is helped
if you become the "linux expert" in a group. This is not research.

## Lastly

Having covered some specifics of the Ph.D. process, I think its most important
to remember:

{{< callout title="It's not a sprint, it's a marathon." >}}
A journey of a thousand miles behind with just one commit.
{{< /callout >}}

The average Ph.D. in CS is between 4 and 6 years long. That means you probably
should take weekends whenever possible. That means you probably need a hobby.
That means that not every day is going to be your best work. Sure, as Matt Might
pointed out, ["Ph.D. school is a monastic experience. And, a jealous
hobby."][matt_might_why_phd_students_fail] And sure, you should expect to work
some late nights and weekends. However, many otherwise successful students burn
out brightly and quick.

The way you get around burnout is to keep your goals in mind, and to find
purpose in the work you've chosen to do. Make sure that you:

{{% callout title="Corollary: Enjoy your research topic."%}}
You're going to be thinking about this while you: wake up, go to sleep, eat lunch,
shower, talk to your significant other, and at midnight in your office the day
the paper's due. You should probably like it.
{{% /callout %}}

This is easier said than done. Personally, I just got lucky and stumbled on the
most interesting project I've had the pleasure of working on to date. However,
if you're entering a Ph.D., you should probably be the sort of weirdo who finds
the idea of pondering a project for a few years exciting.



[matt_might_articles]:http://matt.might.net/articles/
[matt_might_illustrated_phd]:http://matt.might.net/articles/phd-school-in-pictures/
[matt_might_why_phd_students_fail]:http://matt.might.net/articles/ways-to-fail-a-phd/
[the_pragmatic_programmer]:https://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/020161622X
[pragmatic_programmer_tips]:https://pragprog.com/the-pragmatic-programmer/extracts/tips
[strunk_and_white]:https://www.amazon.com/Elements-Style-Fourth-William-Strunk/dp/0881030686
[on_writing_well]:https://www.amazon.com/Writing-Well-Classic-Guide-Nonfiction/dp/0060891548
[google_scholar]:http://scholar.google.com/
[github]:http://github.com/
[bullet_journals]:https://bulletjournal.com/
[lean_in]:https://www.amazon.com/dp/B009LMTDL0/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1
