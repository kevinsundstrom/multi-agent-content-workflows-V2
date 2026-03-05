Mar 4, 2026  #AgenticWorkflows #GitHubCopilot #AI
Welcome to another episode of GitHub Checkout! This time, Andrea is joined by Idan to explore the brand-new agentic workflows. We dive into how you can use plain English and GitHub Copilot to automate complex repository tasks, from syncing documentation to upgrading frameworks. Watch as we build a "super Dependabot" and see how major open-source projects are already using these tools to reduce maintainer burnout.

#AgenticWorkflows #GitHubCopilot #AI 

GitHub Agentic Workflows: https://github.github.com/gh-aw/
GitHub Next Discord: https://gh.io/next-discord

— CHAPTERS —  
 
00:00 Welcome to GitHub Checkout 
00:26 What are agentic workflows? 
01:04 Building a super Dependabot for Astro 
02:35 How Copilot turns English into workflows 
03:41 Setting guardrails and safe outputs 
06:12 Exploring the agentic workflows examples repo 
08:30 Real world example: Home Assistant issue triage 
10:01 What's next for agentic workflows? 
10:26 The future of open source maintenance 
11:05 Outro and next steps 

Stay up-to-date on all things GitHub by subscribing and following us at: 

YouTube: http://bit.ly/subgithub 
Blog: https://github.blog 
X:   / github   
LinkedIn:   / github   
Instagram:   / github   
TikTok:   / github   
Facebook:   / github   

About GitHub:
It’s where over 180 million developers create, share, and ship the best code possible. It’s a place for anyone, from anywhere, to build anything—it’s where the world builds software. https://github.com
Explore how to leverage AI to automate complex repository tasks beyond basic scripting. Learn to implement secure, intelligent workflows for maintenance, documentation, and testing using natural language instructions.
Summary

How this was made
Auto-dubbed
Audio tracks for some languages were automatically generated. Learn more
Ask
Get answers, explore topics, and more

Ask questions
Chapters

View all
Transcript
Follow along using the transcript.


Show transcript

GitHub
604K subscribers
Videos
About

LinkedIn

Instagram

GitHub Agentic Workflows
Learn More

38
GitHub Checkout
by GitHub

Join the GitHub Next Discord Server!
Join now
2 Comments
Kevin Sundstrom
Add a comment...

@blanky_nap
5 hours ago
was trying this feature today, looks very powerful!

1


Reply


@OmegaAlfa-p7h
40 minutes ago



Reply

Top is selected, so you'll see featured comments
In this video



Chapters

Transcript
Welcome to GitHub Checkout
0:00
Idan: A big part of Agentic Workflows
0:01
has actually been about
0:02
how do we stick the right
0:03
guardrails around the execution of this
0:06
so that you can have confidence
0:08
that it’s going to do
0:08
what you ask without doing
0:10
any of the things
0:10
that you don’t want it to do?
0:13
Andrea: I’ve been playing a little bit
0:14
about for maintenance
0:15
for my own repositories,
0:17
but I can’t wait to see you,
0:19
first of all, explain to us
0:20
what Agentic Workflows are,
0:21
and then show us
0:22
some of the practical ways
0:24
users can start using them today.
What are agentic workflows?
0:26
Idan: Agentic Workflows is really
0:27
thinking about like,
0:28
how can we push the boundaries
0:29
of what is automatable
0:31
as part of my repository.
0:33
I’d like to create
0:35
an automation
0:36
that detects when my docs in my code
0:37
have diverged,
0:38
or I want an automation that helps me to
0:41
make sure that my code meets
0:43
accessibility standards
0:44
or do performance optimizations.
0:46
There’s a lot of different things
0:48
that we can do with it
0:48
and we don’t even know
0:49
what all those things are yet.
0:50
This is the GitHub Agentic Workflows website,
0:54
we’ll drop a link to it in the show notes,
0:55
but this is public and
0:57
you can show up to this website
0:59
and check out all the different Agentic
1:01
Workflows that we’ve authored.
1:03
But, I actually went
Building a super Dependabot for Astro
1:05
and used it for a specific
1:06
Agentic Workflow.
1:07
I have my blog,
1:09
or not blog, whatever.
1:10
It’s like, here’s my personal site
1:11
and it’s fine.
1:12
It’s a personal website,
1:14
but it runs on Astro, which is like a web
1:17
framework for creating
1:19
static sites.
1:20
Very popular.
1:21
So, I used
1:22
Agentic Workflows to basically make
1:24
a super Dependabot.
1:25
Once in a while
1:27
I need to upgrade Astro,
1:28
the framework itself.
1:30
But upgrading the framework
1:31
is not just like,
1:32
“Okay, bump the version numbers
1:33
in my package.json.”
1:35
Very frequently there’s migrations
1:37
or things that I need to do on top of it.
1:39
And that’s the kind of thing
1:40
that maybe Dependabot
1:41
can’t do for me because it requires,
1:43
again, intelligence and judgment.
1:45
Here I can create a workflow as easily
1:47
as going to the Agents tab of my repo.
1:49
And then there’s
1:50
this important line here,
1:51
“Create a workflow
1:53
for Agentic Workflows using...”
1:54
and here’s basically
1:55
a skill that we publish about
1:57
how to create workflows.
1:58
So you’re using AI to create AI.
2:00
And then I describe in a lot
2:02
the same way that I would
2:03
describe to a teammate,
2:04
“Listen, everyday
2:06
check if there’s a new release from Astro
2:08
for any of my dependencies.
2:10
And if yes,
2:10
look at the changelog,
2:11
look at the upgrading docs,
2:13
come up with a plan to do the migration,
2:16
including dealing
2:17
with any breaking changes,
2:18
and then create a PR
2:19
with all the changes
2:20
related to the upgrade.”
2:22
Copilot picks this up,
2:23
and actually,
2:23
if we look at this thing,
2:25
you can see
2:26
we’re starting with the prompt,
2:27
Copilot reads it,
2:28
it follows all the instructions,
2:29
blah, blah, blah, blah, blah.
2:30
At the end it produces
2:32
a pull request with this workflow.
How Copilot turns English into workflows
2:35
In Agentic Workflows,
2:36
the actual workflow
2:38
description is just Markdown,
2:39
it’s just English,
2:40
with this front matter block up front.
2:43
And this is where
2:44
we put guardrails on the agents
2:45
because you don’t want to set agents
2:47
free to do stuff
2:48
without sticking some guardrails on them.
2:50
What’s the purpose here?
2:52
It’s an upgrade checker,
2:53
it looked at my code,
2:54
it figured out what
2:55
my actual dependencies are,
2:57
and so every time it runs,
2:59
it needs to check those things on npm,
3:02
and then review the changelog,
3:04
review the upgrade guide,
3:06
figure out what to bump,
3:07
and then make the necessary changes.
3:10
And then when it’s done,
3:11
create a pull request.
3:12
Here’s an example of a run, right?
3:14
I actually ran this on my personal site,
3:15
and I didn’t ask it to
3:17
produce this table
3:18
or this highlights of the changelog,
3:21
but this is the kind of thing
3:22
where if I
3:23
tasked a human with doing this,
3:26
they would have understood,
3:27
“Hey, this would be a nice experience
3:28
for me
3:29
as the consumer of this
3:31
Agentic Workflow.”
3:32
In this run,
3:33
I’m upgrading from this version
3:34
to this version
3:34
and that version to that version.
3:36
If it had not found anything,
3:37
then it would have also just said like,
3:38
“Oh, there’s nothing for me to do here,
3:40
therefore no operation.”
Setting guardrails and safe outputs
3:41
Andrea: I’ve been getting a couple of
3:43
Dependabot alerts on my own
3:45
open source projects
3:46
where Dependabot can’t really erase a PR
3:48
because there are breaking changes
3:50
or the percentage,
3:52
the confidence that it will be compatible
3:54
is so low that it’s like,
3:55
“Yeah, there is no PR to be raised.”
3:58
I wonder how Agentic Workflows
3:59
can help in that kind of situation?
4:01
Idan: Again, the answer
4:02
is always write in English
4:04
what you would like to happen.
4:05
Maybe my Agentic Workflow
4:06
is every time Dependabot opens
4:09
a PR on my repo,
4:11
look at the PR
4:13
and figure out what additional work
4:15
needs to be done
4:17
in order for my repo not to break.
4:19
Try building it,
4:21
find any errors, fix them,
4:23
look at the documentation.
4:24
Under the hood,
4:25
this is all running on
4:26
top of GitHub Actions.
4:28
Think of it as if
4:29
GitHub Actions and Copilot had a baby together
4:32
then this is kind of what it is.
4:35
Here we’re looking at the top of
4:37
the Agentic Workflow, right?
4:38
It’s a Markdown file.
4:39
The Agentic Workflow's compiler is responsible
4:41
for taking this Markdown file
4:43
and turning it
4:44
into an actual Actions workflow.
4:45
This front matter
4:46
is where we can specify
4:47
things that the agent
4:49
shouldn’t be able to control.
4:51
For example,
4:52
we have the safe outputs block stanza
4:55
in the front matter.
4:56
And what I’ve said here
4:58
is that this Agentic Workflow is allowed
5:01
per run to create a pull request.
5:05
And specifically it’s allowed
5:06
to create one pull request.
5:07
It’s not allowed to create
5:08
five pull requests, right?
5:10
And it’s also allowed to decide
5:12
to do nothing.
5:13
We’re also constraining
5:14
which tools
5:15
this workflow is allowed to use.
5:17
This workflow is allowed
5:18
to use the web fetcher.
5:19
And it’s not just allowed to fetch
5:21
any domain on the internet, right?
5:23
Because this is
5:24
enforced outside of the agentic loop.
5:27
We’re basically sticking a firewall
5:28
between the agent and the internet.
5:30
Andrea: Is this your edited file,
5:32
or this was out of the box?
5:33
Idan: I didn’t actually write this.
5:34
I just prompted Copilot
5:36
with what I wanted it to get done.
5:38
It wrote this.
5:40
Andrea: Are you able to set up instructions
5:41
to how those are written?
5:43
If you use an agent's .md file,
5:46
or if you have any kind
5:46
of Copilot instructions,
5:47
does it respect that or not at all?
5:50
Idan: The answer is the same answer.
5:52
You’re always going
5:53
to get this answer from me.
5:54
It’s like,
5:54
“Can you give the instruction
5:56
in English?”
5:57
you can say,
6:00
“Pay attention to my agents.md.”
6:01
Andrea: Amazing. Okay.
6:02
And so you just showed us
6:03
your own personal use case, which I love,
6:05
by the way,
6:06
my website’s also on Astro,
6:08
so I will steal that from you.
6:10
And go
6:11
and set it up and forget it,
Exploring the agentic workflows examples repo
6:13
because it’s going to do its job.
6:15
Yeah, Astro is fantastic.
6:16
And so
6:18
I know that there is a ton of workflows
6:19
that the team has kind of
6:21
put together for folks to experiment.
6:24
Can you speak a little
6:25
bit about those?
6:26
Idan: On the Agentic Workflows site
6:27
we have
6:28
quick starts and how to create a workflow
6:30
as quickly as possible.
6:31
We also have about 18 bajillion examples,
6:36
both things
6:37
that you can apply it to and a whole
6:40
series of blog posts
6:43
that talk about different applications.
6:45
Cross-repo workflows,
6:47
infrastructure, testing and validation,
6:50
things involving teamwork,
6:52
there’s a ton.
6:53
This is a repo with
6:55
a billion different examples,
6:57
Issue Triage, CI Doctor,
6:59
any time your CI workflows
7:01
fall over, figure them out and fix them.
7:03
Contribution guidelines.
7:05
You can imagine
7:06
applying this to open source,
7:07
automating the kinds of work
7:09
that open source
7:10
maintainers have had to do.
7:11
It’s a lot of labor,
7:12
but can we
7:13
get the robots to do it instead?
7:15
That would be great.
7:16
Team culture,
7:18
planning, things like that,
7:19
this Dependabot stuff,
7:20
which is very similar
7:21
to what I just showed off,
7:22
accessibility review, documentation.
7:25
We have example
7:26
workflows for all of these.
7:28
Andrea: I love this,
7:29
thinking about how easy it is
7:30
now for all of us to create,
7:32
but the maintenance is such a burden
7:35
that keeping up
7:35
with the documentation,
7:36
like I’m so guilty of that
7:38
I have projects that
7:38
I might have updated the project,
7:40
but the documentation
7:41
looks exactly the same
7:42
as when it shipped.
7:43
Having an automated way to do that,
7:46
that’s a low lift.
7:47
Set it and forget it.
7:48
Amazing.
7:49
Idan: I remember when
7:49
I switched from my music to Spotify,
7:53
I had these moments where like,
7:55
oh, that song is really good,
7:56
but I don’t have it.
7:57
And then I had to catch myself saying,
7:58
“Well, wait a minute,
8:00
I have all the music now.”
8:01
I think about that a lot.
8:02
Now with Agentic Workflows,
8:04
it’s like my relationship with
8:05
what is possible to delegate
8:08
has changed overnight,
8:10
and now the hard part
8:11
is actually thinking about,
8:12
“Wait a minute, that’s something
8:13
I could take off of my plate now,”
8:15
and realizing what those things are.
8:17
If I have a request of folks
8:17
If I have a request of folks
8:18
who are listening to this is,
8:20
come kick the tires,
8:22
use this,
8:23
we desperately
8:23
want you to use this and bang on it
8:25
for us to both shake out
8:27
all the edge cases that we can find now,
Real world example: Home Assistant issue triage
8:30
but also to find out
8:31
what are all the things
8:32
that people want to do with this?
8:33
Come by the Discord
8:35
and show us in the
8:35
Agentic Workflows channel.
8:37
Andrea: Any Agentic Workflows
8:38
that you’ve seen the community come up with
8:39
that kind of made you go like,
8:40
“Huh, that’s cool?”
8:42
Idan: Yeah, actually,
8:43
one of our early testers was
8:45
a gentleman named Franck,
8:47
the maintainer of Home Assistant,
8:48
which is one of the most popular
8:51
and also busiest projects,
8:53
open source projects on GitHub.
8:55
They, as maintainers, face
8:58
a lot of maintenance burden
9:00
just dealing with like,
9:02
“Oh, Samsung’s automatic
9:06
robo-vacuum integration broke.”
9:08
Is it Home Assistant’s fault?
9:10
Is it that Samsung changed
9:11
something in the API?
9:12
I don’t know.
9:13
Those are all issues.
9:15
And so what Franck used this for,
9:17
is he created an Agentic Workflow
9:19
that looks at the stack traces
9:22
of exceptions thrown
9:24
in the bug report,
9:25
figures out if the stack trace
9:28
terminates in Home Assistant’s code
9:30
or not in Home Assistant’s code,
9:32
because the workflow
9:33
can look at the stack trace
9:35
that’s attached to the issue.
9:36
And if the bug
9:39
is in Home Assistant
9:40
and is not in third party code,
9:42
then it tries to solve it.
9:43
It tries to actually produce
9:44
a pull request fixing that problem.
9:46
This is one that
9:47
really stood out to me
9:47
because it’s like,
9:48
"Ah, that feels the future right there.”
9:50
Andrea: I cannot wait to see
9:51
what people come up with.
9:52
I feel like this
9:53
feels like one of those
9:53
very momentous things
9:54
that is going to really change
9:56
the way that people approach it.
9:58
Idan: At the end of the day, it doesn’t matter
9:59
if the agent is really good.
10:00
What matters is
What's next for agentic workflows?
10:01
does it do stuff
10:02
that is valuable to me?
10:04
Does it give me more free time
10:05
for more things that I care about?
10:06
Andrea: So what’s coming up on the
10:07
pipeline for Agentic Workflows?
10:09
What is the team working on?
10:10
Idan: Shaking out those edge cases,
10:12
figuring out where
10:13
the thing
10:14
isn’t serving the needs of people.
10:16
So it’s really just
10:17
everybody coming out of the woodwork
10:19
and being like,
10:19
“I want to use it to do
10:21
X, Y, and Z,
10:21
but I can’t
10:23
because whatever is not there,”
10:25
and then we fix that and
The future of open source maintenance
10:27
enlarge the use cases.
10:29
That’s the big thing
10:29
coming up with those examples.
10:31
I’d really love to see
10:32
us use Agentic Workflows
10:34
for the benefit of
10:35
open source maintainers,
10:36
specifically.
10:37
The cost of creating code
10:39
has gone down significantly.
10:40
That’s a double-edged sword.
10:42
On the upside,
10:43
an open source maintainer now has
10:45
agents that can help them write software
10:47
and maintain
10:47
the software that they’ve written.
10:49
On the flip side,
10:50
contributions from people,
10:52
previously,
10:53
it could have been difficult.
10:54
Now it can be a firehose
10:56
that’s really difficult
10:57
to deal with.
10:57
How do we use AI
10:59
to even out those scales and
11:01
tip them back towards
11:02
maintainers having
11:04
more control over
Outro and next steps
11:06
who gets to spend their time, right?
11:08
Because that’s always been
11:09
a problem for maintainers.
11:11
Andrea: Idan, thank you so much for coming by
11:12
Checkout and showing us Agentic Workflows.
11:15
I cannot wait to see what people try out.
11:17
We’ll be sure to share
11:18
the Discord server link
11:19
so that folks can join in.
11:21
And I know
11:21
you and the team are always in there
11:24
talking to users, and then,
11:25
like, interacting and listening.
11:27
So amazing.
11:28
Idan: I love it.
11:29
It’s my favorite place on the internet
11:30
because everybody’s there
11:31
with positive maker energy
11:33
and it’s great.
11:34
Andrea: Awesome.
11:35
All right, well, now you heard this.
11:36
If you’re a tinkerer,
11:37
this is a place for you.
11:38
Thank you, Idan.
11:39
Idan: Thank you so much.
11:40
Thank you, Andrea.
11:42
Andrea: And that was your first look
11:43
at Agentic Workflows.
11:45
If you want to start building your own,
11:47
we dropped all the links
11:48
in the description.
11:50
The Agentic Workflow site,
11:51
the examples repo,
11:53
and the GitHub Next Discord
11:54
where Idan and team
11:55
are hanging out
11:57
and actually want to see what you build.
11:59
The big takeaway from me here
12:01
is if you can say it in English,
12:02
you can turn it into a workflow.
12:04
That’s it.
12:05
No YAML wizardry required.
12:07
Go try it. Break it.
12:08
Show us what you come up with.
12:10
Like this video if it helped,
12:11
and please subscribe
12:12
so you don’t miss the next GitHub Checkout.
12:14
Push those changes to main,
12:15
and we’ll catch you on the next release.
