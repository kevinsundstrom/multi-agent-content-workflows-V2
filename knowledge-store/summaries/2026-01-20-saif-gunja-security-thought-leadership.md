# Summary: Saif Gunja & Dan Shanahan, 2026-01-20

**Source:** `knowledge-store/transcripts/2026-01-20-saif-gunja-security-thought-leadership.md`
**Interviewee:** Saif Gunja, PMM, GitHub; Dan Shanahan, Field Services Director, Security Products, GitHub
**Date:** 2026-01-20
**Summarized:** 2026-03-05T04:38:20Z

---

## Key Points

### Project Timeline and Content Brief Constraints

- The team is on a tight timeline: outline and first draft needed within the week, based on Demangent intake timelines and work-back by Jillian `[00:00]`
- The content brief originated from "Shunger" and targets prospects new to GitHub Enterprise who are actively evaluating DevOps platforms and modern application security solutions `[02:41]`
- The hero ebook is meant to "tell a unified story about GHE and advanced security solve the full secure software delivery problem" — described as an "incredibly big" ask `[02:57]`
- The campaign requires a minimum number of assets in market, framed as a Microsoft standard that must be hit — even if not fully agreed with `[04:21]`

> "They're really trying to amass a pretty significant volume of leads and so the more niche we get the less we're connected to where they're going with the campaign." `[03:13]`

### Alternative Content Idea: State of Secrets Report

- Saif raised a competing content idea: a "state of secrets" report/ebook focused specifically on secret scanning `[01:08]`
- He had been meeting with Aaron's team on secret scanning content strategy and felt the secrets insights angle maps directly to revenue goals `[00:46]`
- He wasn't ready to commit to it for at least a couple of weeks due to competing priorities `[01:46]`

> "I love the idea of this like secrets, like kind of insights book, I think actually there's a lot of sports in that and that's easy to map back to goals that that I have inside of revenue." `[02:23]`

### Why Existing Ebooks Can't Simply Be Refreshed

- Existing security ebooks addressed similar questions but are too out of date to carry the current message and perspective `[03:46]`
- Quick refreshes won't incorporate the updated holistic story; the ask is to write fresh `[03:53]`

> "Rather than leaning into trying to update an existing assets. It's like just right and fresh. And so that's what she's asking us to do." `[04:04]`

### The Core Security Narrative: AppSec Collapse to AppSec Renaissance

- Before AI, there was already a widening gap between vulnerabilities found and vulnerabilities fixed — the security debt backlog was growing `[06:58]`
- AI code generation at 10x throughput makes that gap go exponential, positioning AI as a potential villain `[07:11]`
- The counter-narrative: if security is brought earlier into the lifecycle — where the AI is generating code — vulnerabilities can be prevented before entering the codebase `[07:32]`
- AI can also accelerate remediation via Copilot autofix, security campaigns, etc., enabling an "appsec renaissance" `[07:41]`
- The "found means fixed" tagline was noted as having been moved away from; current framing is "secure and high quality by default" `[08:30]`

> "AI is it becoming this villain of this hero and he says, you know, we kind of came up with a story about AI can be the hero where AI, if you bring security earlier into the lifecycle where AI is generating the code, I, you know, security within CCA, you can prevent vulnerabilities from going into the code base in the first place." `[07:32]`

> "And so what do you go from this appsec collapse to a potential appsec renaissance where you're using AI both to prevent vulnerabilities from getting into your code base right at the start." `[07:41]`

### Secure By Default as the Core Narrative Frame

- "Secure by default" was identified as a message with resonance in the security persona and as a story that can be told on multiple levels `[09:10]`
- It covers: embedding security testing inside Copilot Coding Agent (CCA), embedding security testing inside pull request process, and enabling developers to remediate existing vulnerabilities `[09:39]`
- The narrative allows customers to demonstrate to auditors and customers that they are secure by default using GitHub's platform `[09:57]`

> "I love that story. I think that it's a really, really good narrative. And I think that that is maybe a little bit different and adds a little bit more an edge than what we'll see from some of the other competitors in this space." `[10:11]`

### How CCA and Security Tools Actually Work Together

- When CCA is prompted to make a change, it runs code security, secret protection, and dependency review checks automatically after making the change to ensure freedom from secrets, vulnerabilities, and insecure packages `[11:10]`
- This CCA security checking does not require a GitHub Advanced Security (GHAS) license — it is available by default `[11:26]`
- The intent of giving this away by default is to drive awareness of GitHub's security tools `[12:06]`

> "We're the only platform that allows you to, that does by default, static analysis, secret detection, and software composition analysis for fully-agemptic AI generated code, yeah." `[16:10]`

### The Value of Paid Security Licenses Beyond CCA Defaults

- Without a paid license, there is no governance: no ability to block vulnerabilities from merging, no cross-organization visibility, no visibility across repositories, no aggregate finding counts `[17:33]`
- Paid licenses enable detection and prevention of secrets, governance rules across the whole environment, bulk visibility, and bulk remediation `[20:14]`
- CCA security checks serve as an awareness driver and differentiator for Copilot; the full paid suite covers everything that happens outside of the CCA vacuum `[23:34]`

> "It's governance. It's saying hate like I do not want to allow Developers to be able to introduce security vulnerabilities into the main branch of my repository I want to create a rule across my entire environment that prevents this from happening." `[20:14]`

### AI-Generated Code Security: What's Known and Unknown

- Stats exist on CCA-generated code vulnerabilities before and after security checks were introduced (x% fewer vulnerabilities post-introduction), but were flagged as potentially "spicy" to publicize `[12:45]`
- Whether AI-generated code is inherently more or less secure than human-generated code is genuinely unknown — it would be difficult to go back three years to establish a baseline `[13:49]`
- The framing recommended: AI code generation is happening regardless, so the question is how safe your AI-generated code is — not whether to use AI `[14:13]`

> "I don't know the truth of AI generated code being more or less secure than human generated code. And I think like to be like really honest with Kevin, I'm not sure that anybody actually does at this point, right?" `[13:49]`

### Bulk Remediation and Campaigns as a Narrative Complication

- Security campaigns / bulk remediation is described as an "important story to tell" — identifying large swaths of vulnerabilities and triaging/remediating them with AI assistance `[22:05]`
- This narrative thread was flagged as a complication: it introduces a tension with the "secure by default" story (which implies pristine, clean code) `[22:37]`
- Decision on whether to include it was left to Kevin `[22:28]`

### Ebook Structure: Thought Leadership vs. Product Content Balance

- Question raised: what's the right ratio for a top-of-funnel asset — industry thought leadership vs. product-specific content `[24:35]`
- Top-of-funnel ebooks are typically super high-level; product detail is more middle/bottom-of-funnel `[24:40]`
- Proposed structure: Saif's AppSec collapse/renaissance narrative as the opening and grounding statement → middle section: how GitHub products handle these challenges vs. the landscape → closing: options for how to approach it, positioned as a guide `[26:33]`
- Revenue counterparts are demanding use cases in the content `[27:58]`

> "I think we need to have thought leadership and commentary around that space and then link it back to like what GitHub is doing to help get there because nobody's there, right? Every month, something news coming up. But if we can, I mean, if we can paint a picture of what we think good looks like, I think that would be a good e-book for someone to read." `[26:08]`

> "Follow that like story arc of like us as the the Sherpa the guide for For our customers where like you're here. You've got a problem. You've got AI It's creating code and you worry that it may be secure you want to get to a point where You have secure code." `[27:22]`

---

## Notable Quotes

> "AI is it becoming this villain of this hero and he says, you know, we kind of came up with a story about AI can be the hero where AI, if you bring security earlier into the lifecycle where AI is generating the code, I, you know, security within CCA, you can prevent vulnerabilities from going into the code base in the first place." `[07:32]`

> "We're the only platform that allows you to, that does by default, static analysis, secret detection, and software composition analysis for fully-agemptic AI generated code, yeah." `[16:10]`

> "I don't know the truth of AI generated code being more or less secure than human generated code. And I think like to be like really honest with Kevin, I'm not sure that anybody actually does at this point, right?" `[13:49]`

> "I think we need to have thought leadership and commentary around that space and then link it back to like what GitHub is doing to help get there because nobody's there, right?" `[26:08]`

> "if we can paint a picture of what we think good looks like, I think that would be a good e-book for someone to read." `[26:17]`

---

## Gaps

- `[NEEDS SOURCE]` Exact percentage stats on vulnerability reduction in CCA-generated code after security checks were introduced — referenced but not shared `[12:45]`
- `[NEEDS SOURCE]` The "analyst deck" Saif referenced and tried to find during the call — described as containing graphical formats of the AppSec collapse/renaissance story `[28:35]`
- `[NEEDS SOURCE]` Current state of competitors' (e.g., Claude/Anthropic) integrated security suite capabilities and roadmap `[15:37]`
- `[NEEDS SOURCE]` Shadow AI governance: how GitHub's security products interact with non-CCA AI coding agents run through GitHub `[19:00]`
- `[NEEDS SOURCE]` "Shunger's" full content brief and the minimum asset count standard she is operating from `[02:41]`
