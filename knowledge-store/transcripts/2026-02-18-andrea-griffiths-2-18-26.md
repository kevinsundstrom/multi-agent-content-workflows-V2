Chapters

Transcript
Search in video
Introduction to Copilot Coding Agent
0:00
Tim: GitHub Advanced Security has
0:01
been around for quite a few years now
0:02
and we’re kind of trying
0:03
to bring all that magic
0:04
and all that expertise to AI as well
0:05
so you get the most trusted
0:07
developer AI around.
0:09
We’re going to continue
0:10
to work on that
0:11
and continue to iterate
0:13
and drive forward here.
0:15
Andrea: Well, hello, Tim.
0:16
Welcome back to GitHub Checkout.
0:19
Tim: Hey. It’s great to be here.
0:20
It’s been too long.
0:22
Andrea: It has been
0:23
and a lot has changed.
0:25
Please tell us, what is new
0:26
with the GitHub Copilot coding agent?
0:28
Tim: Just to kind of set the scene and intro
0:31
Copilot coding agent
0:32
because I know that not
0:33
everyone will have seen it and used it.
0:35
Copilot coding agent is a coding agent
0:37
just like
0:38
Agent Mode
0:39
in VS Code, for example,
0:40
or the Copilot CLI,
0:42
but instead of running
0:43
on your computer
0:44
with your local repo in your local state,
0:47
instead it
0:48
runs in the cloud in the background.
0:50
One of the great things
0:51
about this product
0:52
is that we have loads of different ways
0:53
that you can give a task to Copilot
0:55
to work on, so
0:56
you can
0:57
assign an issue to Copilot on GitHub,
0:59
you can open the GitHub
1:00
app on your phone
1:01
and just type in a prompt
1:02
to ask Copilot to do something
1:03
and that’s going to go and
1:04
work on that in the cloud,
1:06
you can do it from VS Code,
1:08
we have integrations into Slack
1:09
and Teams that are really cool,
1:11
but the one that I’m going to show you
1:12
today is something
The Agents Panel & Model Picker
1:13
that we call the Agents panel.
1:14
So I click this button in the top right
1:17
hand corner of GitHub,
1:19
and it opens up this nice little panel
1:21
where I can enter a prompt to ask
1:23
Copilot to do something,
1:25
and I can see a list of other
1:27
sessions, other tasks
1:28
that Copilot has been working on
1:30
for me recently.
1:31
The thing that’s changed here
1:32
that’s really exciting,
1:33
over the past couple of months
1:34
is that we now have a model picker here.
1:37
This is available for Copilot
1:38
Pro and Pro+ users,
1:39
and we’re bringing it
1:40
to business and enterprise users
1:42
in the near future.
1:43
Before, we always use Claude Sonnet 4.5
1:46
when you were using this
1:47
background coding agent,
1:48
but now we give you options.
1:49
But, the one that I probably love
1:51
the most is being able to upgrade
1:52
to Opus for tasks
1:54
where I want to do that.
1:54
So using Opus costs a little bit more
1:57
so you’ll pay
1:58
three premium requests.
Demo: Delegating Background Tasks
2:00
To start something off,
2:01
I just enter a prompt in here.
2:03
So I’m going to choose one of my repos,
2:07
just one of my personal open source ones
2:09
and I’m going to say,
2:10
“Add comprehensive
2:12
unit tests with Jest”.
2:15
This is exactly the kind of work
2:16
that I don’t like doing,
2:17
so that’s the kind of thing
2:18
that I want to give Copilot
2:19
to do for me in the background.
2:20
I’m going to go for GPT-5.2-Codex
2:23
for that.
2:24
Then Copilot is going to go
2:25
and start working on
2:26
that for me in the background.
2:28
So, you know,
2:29
I can shut my laptop, I can disconnect
2:30
my internet, it’s not dependent on me.
2:32
It’s able to just do that
2:34
and then come back to me
2:35
with the PR once it’s done.
2:37
So let’s just click on this
2:38
and we can see kind of
2:40
where we get taken.
2:41
You’re going to see Copilot’s output
2:43
as it starts working.
2:45
The startup time here
2:46
takes a little bit longer
2:47
because we have to kind of spin things
2:48
up in the cloud.
2:49
Right now this uses
2:50
GitHub Actions.
2:51
It’s the kind of compute layer
2:52
to where Copilot is going to work,
2:54
so the same place you’re running CI/CD.
2:56
While this get started though,
2:57
I’m going to go to another example
2:58
that I kicked off earlier,
2:59
just so we don’t have to wait
3:00
for things to get ready.
3:01
This is another one
3:02
of my open source projects,
3:03
and I was doing some back and forth
3:05
with Copilot earlier on today.
3:07
It’s got its own development environment.
3:09
So it can run git, it can
3:11
run tests, all of those great things.
3:14
The same stuff that we expect
3:15
from an agent anywhere.
Automated Code Review & Security Scanning
3:16
I want to show you a couple of cool
3:18
things that we’re doing in here
3:19
to improve the quality of the code
3:20
that Copilot writes.
3:22
So if I scroll down, you know,
3:25
all these edits
3:25
that Copilot is making,
3:26
it’s making changes,
3:27
it’s running tests, it’s running the linter.
3:29
Here it says that it’s reviewing its changes
3:31
with Copilot code review.
3:32
This is a really nice kind of
3:34
Spider-Man pointing at
3:35
Spider-Man moment where
3:37
Copilot coding agent
3:38
is working with Copilot code review
3:40
to improve the quality
3:41
of work that it’s doing.
3:42
And you can see here
3:43
that Copilot got some
3:45
feedback on the changes
3:46
it made.
3:47
It got told that the string concatenation
3:49
is overly complex, which is great.
3:51
It’s writing code
3:52
that’s not so good,
3:53
and it’s able to take that feedback
3:54
and then go and make changes
3:56
based on that,
3:56
and the really nice thing about
3:58
this is this gets done
3:59
before you even see the code.
4:01
When you get that review request,
4:03
You’ve got something that is
4:04
in a much better state,
4:05
that’s higher quality,
4:06
that’s more likely to be ready to merge.
4:08
We also have an integration
4:10
with GitHub code scanning
4:12
and what that does is scans your code
4:15
for security vulnerabilities,
4:16
and again, that’s going to run
4:17
automatically inside
4:18
Copilot as it’s working.
4:20
Usually that’s part of
4:21
GitHub Advanced Security,
4:22
which is
4:23
a premium GitHub feature
4:25
that costs extra per month,
4:27
but we give this away for free
4:28
with Copilot coding agent
4:29
just because we want to make sure
4:30
that all the code
4:31
that we’re generating with AI,
4:33
we want to make sure that’s secure.
4:34
Andrea: Tim, this is all baked
4:36
into the Copilot coding agent’s workflow?
4:39
I don’t need to turn anything on
4:40
for this to happen for me?
4:42
Tim: Yeah, that’s right.
4:43
It all just happens automatically for you
4:45
without clicking anything.
4:46
And it’s all going on in the background.
4:48
We also have detection
4:49
for secrets using GitHub secret scanning.
4:52
So if Copilot accidentally commits
4:55
an API key
4:56
or something like that
4:56
into your codebase,
4:58
that’s also going to get picked up
4:59
and stopped before it happens.
5:01
And, we also have an integration
5:03
with the GitHub Advisory Database,
5:04
which means that
5:05
if Copilot installs
5:06
a new dependency into your project,
5:08
we’re going to scan that
5:09
dependency and check
5:10
whether there are any known
5:11
vulnerabilities
5:12
with the dependency as well.
5:13
So if you think about the LLMs
5:15
that are powering agents like this,
5:17
they don’t know everything
5:18
that’s happening right this second.
5:19
They were trained with data,
5:21
maybe six months old
5:22
or a year old or something like that.
5:25
And that means that
5:25
they will often recommend
5:27
maybe old dependency versions
5:29
and not the latest version.
5:30
With this Advisory Database integration,
5:33
Copilot can pick those things up.
5:36
If the dependency
5:37
it’s picked is vulnerable,
5:37
it has a security issue,
5:38
then it can kind of give a poke and say,
5:40
“You should upgrade this and
5:41
use something later”.
Custom Agents & Performance Optimization
5:42
One other thing I wanted to show
5:43
was a nice feature
5:45
that we have called Custom Agents.
5:46
Obviously like when you’re
5:48
giving a task to Copilot,
5:50
you’re going to write a prompt in here,
5:53
but you’re probably not going to write
5:54
in tons of detail,
5:56
tons of complexity,
5:58
and sometimes
5:59
you might want to create
6:01
different personalities
6:02
or different flavors
6:04
for Copilot to do different things
6:05
and one way that we allow you to do that
6:07
is with this feature called Custom Agent.
6:08
So I go to my repo
6:09
and then I go to “.github”
6:12
and I’ve got this agents directory,
6:14
and in here
6:14
I can write my agents
6:16
and here I’ve created
6:17
an agent called Performance Optimizer,
6:19
and what that does
6:20
is kind of tells Copilot
6:22
to take a particular approach
6:23
when dealing with performance issues.
6:25
So I want it to benchmark first,
6:28
validate how long something is taking now,
6:30
then make a change and then look at
6:33
how big a difference
6:34
it made to be kind of data driven
6:35
in the approach that it’s taking.
6:36
So just to give an example,
6:38
I’m going to open this up again.
6:39
Open up my Agents menu.
6:41
I’m going to use Claude Opus
6:43
because you know for this performance
6:44
optimization task
6:45
I’m willing to spend a bit more money
6:47
to get higher quality.
6:48
I’m going to click here and click
6:49
into the Performance Optimizer agent,
6:51
and I’m going to say, “Optimize how
6:55
airports and airlines are looked up”.
6:59
And I’m going to press Command+Enter
7:00
to go and fire that one off.
7:02
I’ve done a similar one to that before,
7:04
so let me just go and take a look
7:07
and we can see the kind of work that it did.
7:09
It’s running
7:09
a benchmark
7:10
to actually find out
7:11
how performant is the code right now.
7:14
Then it makes changes
7:15
and it runs the benchmark again,
7:17
it can actually say,
7:19
“I’ve made a big performance
7:20
improvement here”.
7:21
So we’ll look at this
7:24
and this performance change
7:25
it can say, “I’ve made a 99% improvement
7:28
of the performance of this code”.
7:29
Obviously, that’s just one small thing.
7:30
It’s not like you know,
7:31
made the whole app 99% more performant,
7:34
but it’s done this targeted change
7:36
and we had to measure the impact.
7:37
Generally I’d say that
7:38
Copilot coding agent
7:39
is going to be great for tasks
7:40
that are small to medium size,
7:43
and you’ve got a really good,
7:44
clear description of what you want.
7:45
It’s not so good if you’re confused
7:48
and you need to make lots of decisions.
7:49
But for, well-scoped things often I find
7:52
I get great results
7:54
sending them to the background.
Copilot CLI: Cloud-to-Local Handoff
7:56
I’ve shown you an example here
7:57
where the performance,
7:58
where the agent is
7:59
where the performance, where the agent is
7:59
stored inside a repo,
8:01
but we also have a way for you to share
8:02
that across a whole organization
8:04
or even across
8:05
the whole enterprise as well.
8:06
So you’ve got ways to scale this up
8:08
and make it work more widely.
8:11
And I’ve got one more thing
8:12
that I want to show you.
8:12
So if you haven’t tried it yet,
8:14
the Copilot CLI is just an agent
8:15
that runs in your terminal.
8:16
So if you’ve used Claude Code,
8:19
for example, or OpenAI Codex,
8:21
it’s a very similar thing,
8:22
but you could use it
8:23
with your Copilot subscription.
8:24
And it’s got some really nice
8:26
magic integration with GitHub.
8:27
This is a session that we
8:28
looked at earlier
8:29
that Copilot was working on
8:30
for me.
8:31
At the bottom
8:31
I’ve got this button here
8:32
that says, “Open in VS Code,”
8:34
but if I click the menu next to it,
8:36
we’ve got other options here as well.
8:38
So you know, checking out with the GitHub CLI
8:40
or create a code space,
8:41
but I’m going to show you
8:42
the “Continue in Copilot CLI” option.
8:44
So this has got
8:45
a little command under it.
8:46
And when I click this,
8:47
it’s going to copy the code to my clipboard.
8:49
So let’s go ahead and try that.
8:51
I’m going to click there.
8:53
And now I’m going to copy and paste
8:54
that command that Copilot gave me.
8:56
If Copilot is actually still working
8:58
then I can
8:59
table those logs in the CLI
9:01
so I can easily monitor from my terminal,
9:03
so if I’m like a tmux guy
9:05
with like four shells
9:06
running at the same time,
9:07
I can, you know,
9:08
have the one where I’m coding
9:09
and the one where I’m watching Copilot,
9:11
but the other really nice thing I can do
9:12
is switch into this local mode.
9:14
And it’s going to check out
9:15
Copilot’s branch
9:16
that it was working on in the cloud locally,
9:18
and let me
9:19
continue that conversation
9:20
in the CLI running on my local machine.
9:23
And the really nice thing about that
9:24
is that
9:25
Copilot is going to have the context
9:26
on what I asked it to do originally.
9:28
So like the message
9:29
at the top of the thread,
9:30
the prompt that I gave it,
9:31
and it’s also going to,
9:32
you know,
9:33
know about all the work that it did.
9:34
So you can see here
9:35
you’ve got all these logs from the cloud,
9:37
and I can just kind of pick up
9:39
where I left off.
9:40
We’ve seen there the way
9:40
that we can kind of pull work
9:42
that Copilot’s been doing in the cloud
9:44
and work on it locally,
9:45
but we can also
9:46
do that in the opposite direction as well
9:48
and be in the CLI working
9:49
and then say, “Actually, we want to
CLI: Delegating Local Work to Cloud
9:51
do this thing in the cloud”.
9:52
So we have a really easy way to do that
9:54
now by pressing the ampersand key,
9:55
which switches
9:57
this into this “Delegate changes
9:58
to remote repository mode”,
10:00
and then Copilot can go off
10:02
and do that thing in the background.
10:03
So I can say, for example,
10:05
“Add CORS headers to allow requests
10:10
from any origin”.
10:16
And then Copilot
10:16
is going to go and pick up that work.
10:18
Do it in the cloud,
10:19
and I can keep working
10:21
on my local machine.
10:21
I can keep working in the CLI
10:23
while it does that,
10:24
So now it’s going to start
10:25
sending the logs.
10:25
It says it’s processing.
10:27
I can obviously open this in my browser
10:28
but I can also press Control-N
10:30
to start a new session
10:32
and just go and do my own thing.
10:34
Andrea: Amazing.
10:35
And so I don’t have to worry about
10:36
worktrees or, like, Copilot is
10:38
taking care of all of this
10:39
for me at this point.
10:40
Tim: Exactly.
Future Roadmap: Planning, Privacy & Reporting
10:41
Right now, this workflow
10:42
we have with the coding
10:42
agent is super focused on writing code,
10:45
so as soon as you
10:46
tell it to do something,
10:47
it opens up a PR, it starts working
10:50
and it tags you for review.
10:51
But this kind of misses
10:53
two things that I really want
10:54
and lots of developers
10:55
tell us that they want as well.
10:57
One thing we’re going to be shipping
10:58
soon is the ability
10:59
to have Copilot work privately,
11:01
and then you can choose to open the PR
11:03
when you’re ready.
11:03
So you could do that
11:05
initial review on Copilot’s work and then say,
11:08
“Okay, now I’m ready for a PR,”
11:09
or you can say, “Actually,
11:11
I don’t want to create a PR for this,”
11:12
like it was an experiment
11:14
or Copilot didn’t do what I wanted.
11:16
It’s going to allow us
11:16
to use the coding agent for
11:19
maybe tasks
11:19
that are a bit different coding.
11:21
So they have to ask it to plan work
11:24
before it does it, and then start coding
11:26
once you’ve reviewed the plan.
11:27
That’s something I do
11:28
all the time in the Copilot CLI,
11:29
but right now
11:30
I can’t really do that
11:31
with Copilot coding agent
11:32
because it opens a PR straightaway.
11:34
But it’s also going to open up
11:35
some other fun
11:37
and random workflows as well.
11:38
So imagine asking Copilot to search
11:41
your repository for
11:42
performance improvements
11:44
and then it can just
11:45
give you a bunch of ideas
11:46
and you could be like,
11:47
“Do this one, do this one,
11:49
but don’t do that one”.
11:50
And another thing that I think
11:51
is going to be really
11:51
cool is using it for
11:54
reporting and dealing with bugs.
11:56
So imagine, at least for me,
11:59
something that I have to do
12:00
every quarter is like,
12:01
tell my manager
12:02
what I’ve been working on,
12:03
like do my personal review
12:04
and I will be able to say to Copilot,
12:06
like, “Hey,
12:07
go through all my work in this repository
12:09
and write a report on the stuff that I did,”
12:11
or similarly,
12:12
if I’ve got an open
12:13
source repository with
12:15
tons of bugs or issues coming in,
12:17
I’ll be able to say,
12:18
“Copilot, like, go through all these issues
12:19
and tell me what I need to know,
12:21
like help to summarize that for me,”
12:23
and I’ll be able to do that
12:24
stuff in the cloud
12:25
and it will just work in the background
12:27
then tell me when it’s done.
12:28
And I won’t have to have a pull request for that.
12:30
It will just be doing it’s thing.
12:32
Andrea: Well, it sounds like
12:33
there is a lot of really big plans
12:34
for the Copilot coding agent.
12:35
I’m excited.
12:36
Tim, thank you so much for coming by
12:38
and showing us.
12:40
And that was your second
12:41
look at the GitHub Copilot coding agent.
12:44
Your coding agent
12:45
anywhere you work.
12:47
Thank you for watching.
12:48
Please don’t forget to like
12:49
and subscribe.
12:50
Push those changes to main
12:52
and we’ll catch you on the next release.