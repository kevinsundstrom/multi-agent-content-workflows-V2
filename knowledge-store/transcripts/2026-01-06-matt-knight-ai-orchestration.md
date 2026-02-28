# Interview Transcript: Matt Nigh, Director of AI for Everyone, GitHub
**Date**: 2026-01-06
**Interviewer**: Kevin Sundstrom
**Format**: Video call, 53:01 minutes
**Topics**: GitHub Copilot for Enterprise, agent-orchestration, security controls, ROI measurement

---

00:00 Thank you.
00:07 Sounds good. And I'm recording because, uh, my hope for this conversation is that I'll use the transcript to hand that not only do refine an outline that I might work on patented over to the writer.
00:17 This can be assigned to this to give them a little bit of additional context. I want to write your blog post already helped quite a bit.
00:23 It was, it doesn't usually work out that way that we publish something that's great on the same topic that I'm going to be writing on.
00:30 But I was happy to see it because we can just lift and shift on a lot of things, but it is an agent orchestration and all of this is a thing that I know a little bit about, not nearly enough, so I'm hoping it can be just kind of somewhat informal conversation where I can let you talk a lot so that I 
00:48 can get all of your thoughts on the subject. I don't know if you have somewhere you want to start. I sent over those questions, but I was just going to start top down.
00:55 I've kind of thought through them all. So yeah, yeah, I feel happy to just go top to bottom. Cool. Awesome.
01:04 So first, I would start with a suggestion. I would say for the business case, core operational gain, as well as specifically, let me find it, there's, you have another question.
01:32 Oh, how much time should a manager spend actively monitoring for that question and the core operational one. I would also refer you to Ben Balter.
01:44 Ben is one of the top three users of Code-Coding Agent across the organization and he's probably going to be able to give you some really cool quotes.
01:53 It's kind of what I'm saying. So I have my own answers there but I would also encourage you if you're not familiar with been he's great with Async too, you could just send him these questions and he will write great stuff for you Async.
02:08 But yeah, let me just jump into my own answers. So first, the business and since you're using AI to summarize, I'll talk more formally.
02:17 The business case envision the core operational gain, what is the main operational gain or ROI return on investment for an engineering manager using agent orchestration.
02:32 So first, and this to some degree goes with the second thing, the next question about the cultural shift that managers have to make.
02:40 But an easy way I tend to think about it is managers aren't just managing humans, now they're managing agents. So what's the ROI for one?
02:51 You have additional team members in a way Underneath you, as in you have these agents who can perform work for you, if you can just delegate work to them, no different than like having an additional junior engineer on staff.
03:07 So a specific example of what I mean is I work in operations within the Hubber programs and platforms team.
03:17 Part of what we do is we maintain internal operational platforms like the Hub, for example. Like Mission Control, which is the digital signage that you will see and some of the dashboards that you will see if you go into any hub or physical location that we have.
03:39 We don't have a developer in our group. It's me and Ben using co-pilot, and we are using these agents to effectively act as junior developers, so we can maintain these internal applications.
03:55 So what's the ROI? The ROI is that, like today, for example, we are not waiting on engineering resources in order to do our work.
04:04 As long as the work is something we feel comfortable enough with, we use mission control and agents to basically update, add new features, refactor, improve performance on these platforms, as well as catch bugs, Because oftentimes, and this is the case with our work as well, some of the work that we 
04:26 pick up because they're operational platforms, they don't receive the high level of investment that external products would, for example. So oftentimes we're picking up work that has not been improved or worked on for a long time.
04:41 For example, we recently redid the mission control, which is this big GitHub display at every site that shows the commits as they're happening live, the PRs as they're happening live, and it's summarizing activity to give this cool display to anyone there.
04:59 I think it had been four years since that code base was touched. There were security vulnerabilities. There were significant build problems.
05:09 There were upgrades and refactoring that needed to happen because there was like an issue with a memory leak, for example.
05:18 And effectively, we had co-pilot do almost all of this work for us without having to wait on an engineering resource.
05:26 So the ROI is that you have a technical agent on the team you can assign work to and you don't have to wait for external people.
05:34 and it's not dissimilar than just delegating work to an employee, for example. You have to write out what you want, you have to write out its goals, and you assign it to co-pilot and BAM.
05:47 So what's the biggest cultural shift it's implied in kind of what I'm talking about, which is some managers still see co-pilot as this thing to actively do sync.
06:01 right? So like, for example, I'm an IC, an individual contributor. So I actually do most of my AI work sync rather than async.
06:12 And I can do that because I have hours during a day to focus on a single task where I can sit there and I can look at my screen for three hours and I can work on one problem.
06:23 My manager Ben, for example, can't do that. He's going going between meetings during the day, you know, he's running out to lunch real fast and coming back and then sitting in a meeting and then he has a 15 minute break and then he's joining a next meeting.
06:38 That's where Async becomes incredibly powerful because if you're not someone who has hours to sit there and work on one task, then you need a way to effectively assign work to an agent in an Async way, where it can work in a way that you could observe it and you you could, if you will, pivot it, instruct
06:59 it, but you could also walk away and attend that meeting completely while the agent does that work and you don't look at it once.
07:07 And that really can help managers who embrace that philosophy of, I now need to understand how to effectively throughout my day create work that is reasonable and right for an agent to do, assign it, and then I need to find time in my day to review that work as well.
07:27 That's a new concept because a lot of the time managers are really used to just, you know, sending a Slack message with an instruction, for example, and you're sending it to an employee or a junior developer on your team.
07:38 Well, now you put it in an issue. You assign it to co-pilot. You come back and you review the work later, right?
07:44 That's a shift in your workflow. That's a shift in thinking and how you schedule yourself, for example. And to me, that's one of the biggest cultural shifts that that I think a manager has where so many managers think about their work with AI, like an IC would, which is, you know, how would I use this
08:05 if I have hours to focus using it at a time? Instead of thinking, I now have this new ASync tool that I can apply an instruction, send it on its merry way, and I can come back one to four hours a day later, a week later, if I go on vacation, then review it and put it in.
08:26 To me, that's one of the biggest challenges that I see with managers today. Greg, I'm going jump in. One question I have is when we think about a fleet of agents rather than one agent individually, so far what you've spoken to makes total sense when I think about one agent and one task.
08:43 But if we think about a host of tasks and more than one agent, how does that change the mindset? Because my proxy for it is with the way that I play with Copilot is I have a resume website.
08:53 And when I think of the thing I want done on it, I say, hey, I think let's have a light mode in a dark mode.
08:58 That'd be fun. And all I'll do is just what you were saying. Like, before I hop on a call, we'll just create the issue.
09:02 And then it does it while I'm on a call. And then I act back on it. But I have 10 things in my head.
09:07 And I would love to come back to more than one thing being done. So how does that change? And how does that change when it's not just me thinking about it for myself, but it's me thinking about that in terms of how it's utilized across the entire team?
09:19 In my perception, it's the same journey, but the next step. The first step people have to get used to is that thinking async, right?
09:28 Is that a sign work walk away or observe if it's complicated enough? And then you come back. The next step is, okay, well, now you're comfortable doing async.
09:38 How do you treat it like you're saying, a fleet, or I will commonly say a team, a team of agents that you can assign work to?
09:45 So, I'll continue using Ben as an example here. So, when Ben manages a few repos, Ben manages the hub, which is the internal internet, Ben manages mission control, which is the thing I talked about earlier, essentially almost like digital dashboards and signage, Ben manages the onboarding site.
10:07 We both together manage the AI learning and development site and all of these require code changes, right? code changes, everything you're thinking about, right?
10:17 Sometimes it's like the hub refactoring for performance because we have a long-build process. Sometimes like for my AI, for everyone's site, it's you're adding a quick feature, you're adding quick content, or mission control, where you're making changes to how the API works because we're gathering a 
10:36 lot of data from different APIs within that. So how do you shift from thinking, how do I, you know, I'm now just working and sending one message to this agent and I'm coming back.
10:46 Now, how do I think how am I solving this portfolio of problems that I have to deal with and how am I imagining agents for that?
10:56 So first, custom agents come into that concept. So if you hit mission control, you have the ability you see a screen, you select a repo, you have the ability to select a custom agent, though the normal agent is selected by default.
11:13 And what you would do is you would think, A, do I have custom agents set up for the work that you're talking about?
11:22 And I'll give you an example here. So in the hub, we have a documentation agent. We have a writing agent to help people that are authoring internet articles, essentially.
11:35 We have a sweet agent, which is basically just some commands and instructions for the normal coding agent to understand how we kind of have coding practices on the hub as an easy way to think about and kind of what folders to avoid, for example.
11:53 And what you're doing is you're essentially thinking, okay, I have these, let's say five pieces of work that I want to try to make sure I get done today.
12:05 The way you do it is I generally recommend you build an issue for each one, whatever those things are, and simply put, you just spend that time that you're thinking about building out an issue and assigning co-pilot to it to work on.
12:21 The tactical thing you have to think about is you need to budget time for creating issues in a way that you probably didn't in the past.
12:30 In the past, managers might have relied more on Slack to communicate and things like that because you're telling an employee or asking an employee to do a thing.
12:41 Well, now, the way you do that with an agent, I would say the best way you do that is you put that in an issue.
12:47 you, you then assign it to co-pilot, and then obviously you have the PR from that work. Well that means you have to change your workflow.
12:56 That means that you need to think about how are you budgeting time for issue creation. So like for Ben Balter, for example, every single day from five to five fifteen, he spends just creating tickets or issues, excuse me, and he has multiple times like that throughout the day where he has these 15 minute
13:18 increments of time, where his whole thing is I'm going to create issues. And then the next day he has review time.
13:26 So as a manager you need to think about well what I'm not going to do as much anymore is I'm not going to necessarily like slack or email a problem to someone.
13:38 I'm going to have that live in a persistent place and an issue. you, and then that gives me the ability to assign co-pilot.
13:46 And if I have multiple problems that I want to use co-pilot for, not just one issue, then you need to think about how are you blocking time off for that so you stay and flow.
13:56 Because what you don't want to catch yourself doing and you'll hear complaints from people who do this is, if you get into a practice where you're just randomly creating these issues throughout the day and you're not having like thoughtful book time for them, it's going to be a lot harder to get the 
14:12 throughput from co-pilot that you want. You need to make sure you're booking time to be thoughtful that you're creating these as step-by-step instructions.
14:22 You'll get much more returned out of it, and you'll be able to effectively use a team or a fleet of agents rather than just, you know, trying to treat it as ad hoc, which doesn't necessarily get you those same results, and it doesn't feel as much like a fleet of agents behind you, if you will.
14:41 One thing I'm not aware of is now that we have sub-issues. Yeah. Is there any role that sub-issues play? And like, can you create one issue for a series of work that you want done and sub-issues and have agents assigned to each sub-issue?
14:53 Or is it, you can absolutely do that. I mean, in essence, the way the functionality works is any type of issue that you create, if you assign co-pilot to it, it's going to create a subsequent PR for that individual issue.
15:09 So you could have a parent issue that, for example, is never assigned to Copilot. And that parent issue has 10 sub-issues within it.
15:18 You do have to individually assign issues to Copilot. You, for example, at least today, you can't assign the parent to Copilot and then have the sub-issues automatically picked up, just FYI, but absolutely yes, you could and should think about structuring your issues in the right way and things like 
15:41 that because that will also help the agent understand your work better, right? Because it's reading the issues that you're riding.
15:48 To what degree of this point are you or Ben using AI for the creation or triaging of the issues the you're creating.
15:59 So I would see the functionality you're talking about more in customer success. Triaging, generally speaking, is like, you know, I have a thing I want to work on, that thing needs prioritization, that thing needs scoping out to some degree or fitting within some sort of priority and escalation framework
16:16 within our team. We don't really use that and opt so much because like most of our things are like third tier, like oh you have a problem we'll get to it tomorrow because these aren't production systems, for example.
16:31 For that question, I would probably refer you, I think, let me message you after this in name. There's an individual within GitHub.
16:44 Pablo, I can't remember his last name right now. Yeah, I need to look it up. He just spoke at the recent get-together and he's one of the AI advocates for the group I run but they just came up with a great triaging process themselves because yes absolutely you can and should do that on like production
17:04 grade systems where you are having to triage work. We just don't have work within operations that is production level so we don't really triage in the same way.
17:14 Well I'm sure there's some sort of like six cents you develop over time and working with agents on what their hit rates going to be on different tasks.
17:23 Short of having that developed innately over time, the thing that I've done occasionally is say, hey, I have this bucket of work that I need done.
17:31 And I'll ask Kopai that, like, what are the most likely tasks to be to run seamlessly through an agent versus what's the stuff that I'm going to have to hand hold a little bit more?
17:40 And then the stuff that it's likely to just solve entirely, then I'll just create issues and have that run whereas the synchronous time I do spend is the stuff that I think it's likely to fail on.
17:54 But I do feel like I'm wasting time in that triaging step, you know? Yeah, my advice there would be, there's new functionality, brainstorming mode, I believe it's still called.
18:06 If you're on mission control, if you're using VS code, it's called planning. But effectively, they've created what I would call chat modes, if you will.
18:20 They're just basically modes that are fed to an agent that are meant to help you build out your idea. So, if you use planning or brainstorm mode, which you should, when you create an issue, it's fantastic.
18:34 It's basically going to reduce the time that it takes you to do what you're talking about, and it's going to assist in terms of, well, let me break down what you're saying by triage.
18:47 It's going to help turn your idea into individual components that can be executed independently. It's going to help you prioritize and understand what should be done first, what's the biggest priority, what stuff you should consider later.
19:01 It's going to help you put a detail around each one of those ideas by asking you a series of questions like a mini interview almost and then it's going to use your responses to form that issue document or whatever it is that you're working on.
19:20 So yes, I would strongly recommend planning or brainstorm being used as almost a kickoff to creating that issue or to creating that piece of work because it will do some of what you're saying.
19:34 But it would still be a chat form and so you'd have to like take that and copy and paste it into an issue or do we, I want to say the, so I use VS code.
19:44 So I know in VS Code, you'd connect to your MCP server and it would create the issue for you because that's what I do.
19:51 But give me a second and let me confirm the functionality of the other because I want to say brainstorm mode doesn't require that.
19:58 That you wouldn't have to do that kind of copy and paste effort. But I could be wrong. Let's see. So I'll just say to ask.
20:16 Agents, how they're calling it, something else now. It's task mode now, is what they're calling it. It's on chat. Okay, perfect.
20:39 So, no, I mean, my thinking and my advice would be this. This happens in GitHub chat, where GitHub chat has the ability to create issues for you.
20:53 You just have to ask. So, what I would do is I would essentially plan in chat and then I would ask it to take the output of what we worked on together and make that an issue.
21:05 I think that, that to me, probably represents the best workflow I can think of today. So, you almost stay in flow, where all you're really doing is you're kicking it off in chat, you're expanding on your idea, you're using, again, depending on the product slash surface you're using, you're either using
21:24 planning mode or using something like brainstorm or task mode. And then you're creating an issue from the output which you can do within chat, you just ask it to create the issue in whatever specific repo you're working in, or you specify the repo.
21:40 And then you hand that work off to an agent just simply by opening the issue that was created and then assigning co-pilot to it.
21:50 Makes sense. Where should we jump next? The parallel bit. I feel like it's still the area that, Yeah, it's a good one.
21:58 So, let me rephrase it because I think the right question might be, what are the two to three key rules for deciding if a task should not be run by parallel agents?
22:12 I think that's the real question. One are kind of like when shouldn't you run parallel agents. So first, what's the problem with parallel agents?
22:23 What's the thing that happens if you do it wrong? Merge conflicts, generally. So essentially what's happening is if you, for example, use an agent to make code changes, let's say you kick off two agents.
22:39 Both of those agents could be asked to change the same file. And it's possible that their changes don't integrate easily or well.
22:49 And that's what happens as a consequence when you don't orchestrate well, is you just have administrative time on the back end fixing those merge conflicts, which it's not fun, it's a lot of paper cuts.
23:04 It's often easier to kick off into agent and just redo that work, than it is solving the merge conflict. So, that's the end problem you're looking to avoid.
23:15 Now, what's the right way to think about, when should I have a warning sign in my brain for maybe I shouldn't run an agent parallel here?
23:25 Generally, if it's touching the same files, I automatically just won't run parallel agents. If it's touching, If you will, fundamental code that is a dependency for the other work of an agent, even if it's not the same file, if it represents a dependency that could change with it, that's something that
23:52 you should also think about or avoid if you don't necessarily understand the consequences and you don't understand those dependencies well, then don't run agents concurrently.
24:00 If you're very educated on that code base and you have an understanding of, well, I expect it to only read from this and not write to it, for example, then you're probably fine.
24:14 Those are the main things I would think of. Is that area of the code base effectively overlapping between those agents?
24:22 If it is, consider not running them in parallel or set a different way, at least have a reason and you want to run them in parallel.
24:31 Maybe you want an experiment. Maybe you're just looking to see two different outputs. But if you're thinking, these are changes I want to ship, these are changes that really need to be deeply reviewed because they're normal software code changes, and this isn't special, then I would urge you to be cautious
24:47 with running multiple agents effectively in the same area on the same files. The other thing I would think about is, is the change that I make a code breaking change.
25:01 So sometimes you're asking an agent to do something that is a large refactor. It depends on your code base size, but if you're doing a very large refactor and that large refactor is a question mark in your mind of you don't know what areas of the code are going to be changed.
25:20 You are asking the agent to do something in which maybe you're not a technical expert in. I would also then think about single threading, because if you just don't understand the consequences of your actions, it's a lot easier to unravel something if you're asking it one thing at a time.
25:39 And you're having it take one action at a time. Then it is if you do a lot of work at once and you effectively then have a ball of code you have to unwind when, you know, maybe, you know, the first three things it did were great, but the fifth things are wrong, for example.
25:57 That's harder to unwind than you've asked it sequentially, five different things. Those are the use cases I would think of.
26:05 For the next question, which is the perfect spec beyond descriptive language, what are kind of essential structured pieces of information that must be in the prompt.
26:17 So, and this question I think I think that the AI picked up on me talking about spectrum and development in my curiosity about what where spectrum and development connects with the prompts that we are writing at what level because there's some prompting that is less formal and you know you're not writing
26:35 a fully developed specification for every issue that you're creating I wouldn't imagine but in some Senate situations you are and so I think that was more or what I was leading in on this?
26:45 That makes sense. So yeah, I would say my advice would there would be the main thing I would tell people to think about is structuring your issues in a way that it is a clear sliver of work.
27:00 You want to give an agent a clear piece of work that has a start and a finish and is small enough that it can be accomplished in a reasonable time.
27:09 So like for example, if you have one feature, that one feature might be three different issues because you might have a UI component, you might have a backend component, and you might have some sort of integration component.
27:22 Don't try to make those one issue where the agents doing completely separate tasks and completely pieces of different work because that's going to a be harder to create a good issue where it has boundaries within the issue.
27:39 and it's clear, you know, this is referring to that, use the structure that you talked about initially, which is like having an issue and have subtasks, and then sign those subtasks to that agent.
27:50 That's the main advice I would give. So in a way, prompts our issues in this new world, where you can assign co-pilot.
28:00 And I would say make sure that you're just simply not asking the agent to do too much in one thing otherwise it's going to have problems.
28:10 Think about it like assigning work again to a junior engineer where it's small pieces of work that are very clear that are very constrained and you'll have a lot more success when directing that fleet of agents, if you will.
28:24 And that's very similar to the advice I would give your next question, which is the custom agents. So what's like a concrete example or maybe what are the types of rules?
28:35 I would encourage people to put in the agents.md file that a regular prompt can't handle. Well a regular prompt could handle anything.
28:45 That's an an agent md file. The problem is in the reason you want to put things in an agent md file is you don't want to have to type it out every single prompt.
28:53 So the type of things I would put in there are the things that I wish were in every single prompt I would write.
28:59 And good examples of that are like, maybe there are files that I do not want the agent changing ever. For example, I will explicitly list them out in an agent MD file.
29:09 Maybe I want to make sure when an agent creates a file that it's always created in a certain way or in a certain folder.
29:19 I would use the agent MD file for that. maybe I want it to all always follow a specific coding practice and I don't want to have to tell it every single time to you know maybe I have a coding standards document in the repo for example which which many GitHub users actually have and I just want to always
29:40 point my agent at it so I don't have to every single time I prompt say refer to this file for your coding standards for For example, but essentially it would be what something that I would give the agent pretty much every single time I prompt, no matter what.
29:59 That's where an agent's MD file can really help you when it just saves you time because there's a lot of context you want to give something, but you wish you might write 100 prompts over the year and imagine if you're having to add these extra two to four sentences to every single one and you're having
30:16 to remember it. That's how I use that. The real-time governance and steering, so like log signals, what are the most critical log patterns that show when an agent is stuck or drifting off task?
30:30 I'll start with getting drifting off task because that's one of the more common ones that I see. Drifting off task is normally I have written instructions that are imperfect.
30:42 And the agent is interpreting, sorry, the agent is interpreting whatever I write in very specific ways, right? So even if you write something vague or not, it still needs to interpret what you're saying to a very specific action and a very specific thing.
31:00 So the main thing that I see is a misreading of intention, which is I didn't say something clearly, and the agent is pursuing a line of work that is not aligned with my intention.
31:15 And this actually goes to kind of a future question of like how much time should you spend monitoring it? I find the main time that I monitor is when I kick it off the beginning.
31:26 As in, I want to validate, did it just understand my instructions? So once I'm generally speaking, sure that it looks like it's understanding everything that I kind of said, I'm seeing it start on the right path, then I go look and I do other work.
31:43 But in my mind, that is the most common thing that happens. The second thing that's still very common is when you provide it with information, if there are problems with that information, AI models tend to have hallucination.
31:59 What I mean by that, for example, is like, if I point within my issue to a piece of data that maybe requires integration, that's not successfully executed.
32:11 So like, it can't pull that data for some reason. Like, maybe I'm like, reach out to this API, gather this data, maybe use this MCP server first.
32:20 And let's say, for example, for some reason, it doesn't do that, and it fails. because maybe I haven't successfully integrated that MCP server a lot of times I'll see AI hallucinate at that point which is it's been asked to look at data but it doesn't have access to that data for some reason or it can't
32:41 get it that data. Then sometimes at a high percentage I see the coding agent make that data up. That's one of those things like if you have a data integration point or MCPs that you're using, I would basically say it's valuable to watch to see if you have failures at that part of your tooling, which 
33:03 is the integration point. Yeah, that would be one of the other common ones that I would see. The rest really just deeply depends on your use case, I would say.
33:15 And then on the steering bit, I'm sensing this may have changed since I was last using the tooling, But I would create an issue and assign an agent and they would say here's what I'm going to work on and I would look at its plan of attack And I'd be like, ah, that's missing.
33:27 That's clearly a misunderstanding or I wasn't clear enough to your point in what I wanted to happen And so then I would comment on the issue like, ah, no, it's not really that it's this and it would not look at my comment And they would just continue on with its plan It sounds like there's been changes
33:41 made so that I can steer more effectively than this Well, we'll keep talking, but I actually, let me share my screen to just give you a visual of how it is.
33:53 So, yes and no to your answer. There is a part no, so yes is your answer to one second, I'm going to share my screen.
34:06 Okay, you should see a window that just says agents. I'm taking a cheap way out. Imagine this is an issue, or you know it, let me go on my personal repo.
34:21 I can do whatever in there without breaking anything. So, the yes part of your answer is absolutely right about the first part, right?
34:29 You create an issue. You have some intent in an issue. right a block for me right a blog and over and you know what I might actually try to show you what it looks like when it's broken.
34:53 I'll just grab a link use this file. Okay, so create. I could have assigned it from co-pilot there, but I'm just going to click this.
35:13 So I could provide additional instructions here if I want. This is the repo that the work is going to end up in.
35:23 And this is the custom agent that I talked about. I have a readme agent in my repo. So all it does is write documentation, but you could create custom ones.
35:33 So yeah, I'm going to use Codex for this. And yeah, let's go with main. OK, so here's the difference, or if you will, then no.
35:43 So you're going to the issue. It should open a PR from here. Now what's going to happen is this is the difference.
35:56 I need to see the session. Then it should pop up any second. So I want to steer this agent, and let's say we want to watch this agent.
36:09 Come on, give me a start session. I should have run co-pilot. I've actually never used Codex in Windows before. Well, while we wait a second, you can even answer a question I've always had.
36:20 There's the initial plan thing that you could click on. How is that different than the session that kicks off after?
36:27 That's, So perfect. This is what I'm trying to show. So the PR is just, you know, almost a beginning in an end view session is how you steer an agent.
36:39 So I'm clicking on view agent. And let me say steer an agent on using that word intentionally. I'm saying steer because it is driving right now.
36:50 You are watching co-pilot drive. When it's done with this work In my mind, you're no longer steering an agent because it is stop driving.
37:00 It is done with its work, right? That's when you go in there and you have issue comments because it's spent maybe that 15 to 45 minutes and it did the work that you ask and it has actually output something.
37:15 To me, that's almost not steering because you're not correcting behavior as it's happening. You are correcting behavior after it has happened and that is to some degree harder.
37:26 Now here, okay, so I wonder if they've changed this. That might be in the normal, you have a thing that you can type in here.
37:40 So let me actually just go back here and create another issue and assign it to co-pilot. So I get for trying something new.
37:53 Alright, I'll blog for me, I'll blog for me on how to use, how to go by and use these Okay, make sure Copilot good.
38:21 Okay, same thing's going to happen. You're going to see, hey, assigned to Copilot sees that. Any second, we should see a PR jump up.
38:29 Perfect. So I've given instructions. It created a PR off of that. But oftentimes, this is better, frankly, just because my thing's so small, and it's such a small ask a lot of times it's like a summary of what you've asked for here, basically.
38:47 But this is not where the real work is happening. If you want to steer an agent, you're basically waiting for a pop-up to happen in a second, and that's there.
38:58 It is the view session. So view session is, I want to watch the agent work. I want to steer it while it's live, perfect.
39:06 Here you go. So this is what I normally am used to where I can steer while it's working. Small asterisk.
39:13 I don't know if this matters for you ebook. There is a you might not know me putting in this agent and sending this one request spent one PRU.
39:29 You can steer an agent, but it might consume an additional PRU, depending on how far along it is. I don't personally remember or even know what that distinction is, but like it's like at some point it's done enough work that they have it triggered where it will create another PRU.
39:46 I don't know if that needs to be specified in your documentation, but I just want to say that in case it does.
39:52 But here's a great thing. So like, you know, we're watching it work and what I would be doing and what I normally would be doing is I'd be like, okay, great.
40:02 I see this. Perfect. This is what I wanted to see. It looks like it's having problems fetching the writing standards, which is what I wanted to show you some sort of problem.
40:14 It might work because I'm authorized to see it, but like it's trying to treat it. Like it's a public repo.
40:22 I can just understand that and it's just trying to get that information. It's not using my creds yet, which you would need because it's a GitHub organization repository, so it need to know I'm a member of, you know, GitHub employees or whatever.
40:35 So like, okay, great. So I look at this and I'm like, I feel like that's probably wrong. I feel like that we don't publish our writing standards on the web.
40:49 That feels crazy to me. So I would do what you're seeing now. And I would be like, okay, so where did it really f****** find this at?
41:00 And I'm really not sure yet. That's funny So like here here's a great example of I would say I would I would be digging into this and I would be Colin Fetch You read me no But yeah, I'm trying to more show you what I would do.
41:22 Okay, here we go Instructure sure, you know what, that actually might be right. Give me a second, make your writing sparkle.
41:36 So like, yeah, I'm gonna sparkle. Ooh, it doesn't find that word on the page, which means I think it is possibly hallucinating.
41:49 And I'm voicing tone number one. Okay, here's a great example. It's done one or two things. I do have a writing agent, which it actually might have grabbed, but this is a hallucination.
42:08 So here's a great example of I sent it a link that I thought wouldn't work, and it looks like what it did is it took that link, couldn't find it, and it found the second best thing which is actually a behind the scenes writing agent that I have that I use with VS code that's what it looks like to me 
42:27 so yeah I would come in here and I'd be like no this is absolutely wrong so like this is not the best way but I'm gonna copy the file I'm gonna say you didn't find the correct writing standards here they are used this instead and you know I would come in there I just paste that for example it wouldn't
42:56 solve the underlying problem of I would probably actually want to know why it can't access that file but still solves this piece of work if you will so that's Steering, if you will.
43:06 I watch it live. I happen to know that this is an existing problem where it might not correctly grab that from the repo.
43:14 So while I don't care to watch the whole thing, I just wanted to make sure it got that piece right now.
43:19 I would now I would move on to other work as it actually goes behind the scenes and finishes quickly like did it already respond to your comment or is it like continue on for a while before my experiences is pretty slow to be blunt.
43:34 Yeah, and it let I'm guessing this might be two premium requests because I saw this pop up before I hit enter So it feels like it might have already consumed one PRU In my experience And I don't know how you want to count for this.
43:53 It's also not perfect ingesting it if you give it steering instructions and it's like 90% of the way done I have seen times in which that steering hasn't taken, for example, and you have to move it to issue comments.
44:10 I wouldn't necessarily Sell steering hard is kind of what I'm communicating because I would also say to me steering isn't necessarily a big feature steering is just Because if you're if you're having to watch 20 agents You're probably not being super efficient anyway, to be honest, like generally speaking
44:32 , you probably shouldn't be watching your agents unless you feel like there's a specific problem. Well, yeah, I would think a lot of time, I know it is what's happened to me is I immediately is immediately clear that I didn't communicate what I wanted correctly.
44:46 Yeah. At that point do you steer or do you just like that point I steer that's why like the kind of what I'm saying is like at least with today's functionality on steering and my mind, there's not much of a reason to watch after a few minutes.
45:01 Like once you know it, it has grasped your intent and it has correctly fetched whatever files or information you're referring to, which is basically what we did, right?
45:12 Like I was like, is it going to fetch this one file correctly before I move on? Then to me, let me say it differently in a way that's almost more storytelling.
45:24 To me, it's kind of like you have a kid on a bicycle And once you get them up on the bike and once you see them moving, they're fine, but you want to stand there And you want to watch them get on that bike and make sure that you know, they move three feet.
45:37 Okay if you will Yeah, no, yeah, that makes sense cool. We're pretty much time. I don't know if you have a couple more minutes.
45:44 I do I can let I can run through some stuff Okay, so monitoring time I would just repeat my previous answer, which is like like five minutes at the start.
45:55 I would kind of cap it there. Like generally speaking, it's the same thing I said which you're just watching it get on track with the basics of what's you said.
46:04 And once you feel like it has the basics, right? Which are like, did it understand my intent? Did it correctly?
46:10 User refer to any information that I cited within it, which might be technical documentation, coding standards. It might be an API, whatever the heck you're pointing to.
46:24 the review workflow. I think that the right place to look is start with the agent's summary or let me say differently.
46:38 So it's the session log technically, right? I would start with the session log if it's complex. If you're asking it to do a piece of complex work, I think it's valuable to look at the session log, I think it should be scanned, not read in depth.
46:53 And you're mostly looking for anything that's really big. Like, for example, we saw the failed fetch. Just, it was there, right?
47:01 Like, that's a big thing to see. Don't look for details. Look for big warning signs if you will. Red light, yellow, green.
47:09 Then where you spend your real time is Copilot has gotten really good at creating extremely detailed comments about its work.
47:17 That's where you should focus on, combined with the code. The self correction prompts, I wouldn't tackle that because I don't feel like there are good ways to make an agent check its own work unless you're in specific scenarios.
47:37 So specific scenarios are like, if I'm you doing UI development, I can use playwright to do that. What you might consider alluding to, and this might allow you to point to other blog content.
47:48 There's a lot of blog content across Microsoft for sure, and I want to say GitHub. I think I've seen it there, but people talk about using playwright and unit testing to have it check its own work.
48:02 For software development use cases, I think those are very good. Now, those only generally apply to specific types of work, but that's where I would point people to.
48:11 I would say that using unit tests and using things like playwright tests, which are basically just UI tests, if you will, are the right way to go with that.
48:24 So the agent can run those for you and you can say things like keep working on this until you pass all of your tests.
48:33 Qualification for you that I would include in that, agents do sometimes hallucinate and They'll say they have correctly done all of those tests when they haven't, especially if it's a very long-running problem, where it's like made 20 changes, it's still failing.
48:49 It's honestly likely to hallucinate at some point. So I would have some form of documentation in there, which is like, absolutely, you can still do that, but that doesn't mean a human gets out of the loop.
49:01 You still need to check its work. You still need to validate it. And yeah, use case validation, are there plan use cases, the strongest examples to focus on, let me take it the different way, because I would say instead of the strongest ones to focus on, I would call out a few weak ones, it currently
49:22 sucks it like monoliths. So anything that is just so big that it can't be contained within a context window today, the Github Monolith, for example, it's, I wouldn't say it's bad at, it just really requires specific instructions and guidance that you wouldn't necessarily give it in a very small code 
49:45 base where it can kind of figure things out for itself. So to some extent, the guidance I would offer on the use case validation is scale your investment in breaking down the work with the complexity of the work.
49:58 work, the harder the work is, the more complex the repo, the more time you need to spend on instructions, no different than if it was a junior engineer, right?
50:09 If you were to give a junior engineer a very easy code base to make a change in, you might give very vague instructions and be like, you know, make the button blue because I don't need to tell you about the 14 things you can break as you make that button blue.
50:22 But like if you're in the GitHub monolith, you need to think about it in the same way, where if you're giving a junior person instructions about how to do something, your investment of breaking down that use case for the AI needs to scale with the complexity.
50:40 And the future of mission control, man, I would ask the product team. I have no idea what features are upcoming for it, frankly.
50:48 Well, I think it went a little bit off on the questions that I need on the use cases where I was headed with that.
50:55 The thing that I'm hearing from revenue folks is we want use cases and what they mean by that is they want a story about co-pilot code review.
51:03 They want a story about, right? And so they want at the end of this, they want to show the products to show up in the end of it so that people can align it with the name that they're hearing.
51:12 And so like what are my extensions that use something? Because my extension of that is what are the use cases in the more the way you and I mean the word use case.
51:21 What are the use cases that will highlight our products in the way that the revenue team wants? Click on, I'm gonna send this link in Zoom chat if I can find the chat button.
51:34 There we go. Okay, what you're looking at when you click on this link is I pulled a large number of merged PRs to be clear that coding assistant has worked on since February through the, it was like whenever I did this, so a few weeks into it.
51:56 So this actually shows you how hubbers are using it, different ways and the common use cases. Now note, those numbers are imperfect in the analysis, so like I wouldn't say anything like that.
52:09 I wouldn't be like 12% of all PRs or this, and things like that. But I would say, directionally, it is good data, even though it is in precise.
52:19 So you could use this to get a feel for, frankly, the type of work that is happening. Yeah. No, that's helpful.
52:28 It's cool. I appreciate you chatting today. I'm sure I'll follow up and need some more information. But I think we'll have enough to get through some sort of a first draft.
52:36 And obviously, if you have time for it, I'd love to have you review the drafts as well. Yeah, I'm happy to help however, just FYI, my role is turning into more external storytelling, so yeah, I can help however it would be valuable to you.
52:50 Perfect, sounds good. And then peek to your calendar. I think you're chatting with Amy. Tell her I said hi. And me and I worked together all the time.
52:56 Awesome. I will. Sounds good. Thanks a lot. We'll talk to you later. I'll see you.