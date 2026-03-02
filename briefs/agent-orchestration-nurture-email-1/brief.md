# Brief: Agent Orchestration Nurture — Email 1 of 3

## Content goal

This is the first email in a 3-part nurture sequence for people who downloaded an ebook on agent orchestration based on an interview with Matt Nigh, Director of AI for Everyone at GitHub. The ebook covered the manager perspective: async delegation, running a fleet of agents, writing effective specs, and monitoring agent work.

Email 1's job is to deliver a piece of high-value editorial content that extends what the reader learned in the ebook — and earns the next two emails. It is not a conversion email. It plants a question the reader doesn't yet have a full answer to.

The angle: the ebook gave them the workflow. This email introduces the engineering layer underneath — why some multi-agent workflows succeed and others silently fail. The insight is that failure usually isn't the model. It's the structure.

## Target audience

Engineering managers and senior developers who are actively using or evaluating GitHub Copilot's coding agent for their team. They understand the concept of assigning work to AI agents. They are starting to run into inconsistency — sometimes agents do exactly what was asked, sometimes they go sideways — and they don't fully understand why yet.

## Format

Single nurture email. Short — under 300 words in the body. One CTA.

## The CTA

Link to this GitHub Blog post:
https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/

The post covers: why multi-agent workflows fail structurally (not at the model level), typed schemas for data consistency, action schemas for intent clarity, and MCP as an enforcement layer. It is written for engineers and is technically specific.

The CTA framing should connect the reader's ebook experience (manager workflow) to the engineering insight in the article. Something like: "You've assigned the work. Here's what's happening underneath."

## Key questions this email should answer

- Why do some agent runs go exactly as planned while others drift or hallucinate?
- Is this a prompting problem, or is there something structural happening?
- What should I actually care about if I want my team's agent workflows to be reliable at scale?

## Angle

The failure mode Matt Nigh described — agents "misreading intention" and hallucinating when integrations fail — isn't random. It's structural. The ebook reader has seen this happen. This email names it and points them toward the engineering layer that explains it.

Do not oversell the article. The email's job is to make the reader curious enough to click, not to summarize the article for them.

## Constraints

- Tone: peer-to-peer, not marketing. Written as if from someone who works on this every day.
- Do not use the word "unlock" or "leverage."
- No numbered list of tips. This is a short editorial email, not a listicle.
- The subject line should create curiosity without being clickbait.
- One CTA only. No secondary links.

## Knowledge store sources

This brief is directly supported by the Matt Nigh interview summary. Specifically:
- The failure modes section (misreading intention, hallucination on failed integrations)
- The parallel agent / merge conflict risks
- The monitoring philosophy (5-minute kickoff window)

The orchestrator and draft agent should draw on those sections for the email body. The GitHub Blog article above is the CTA destination — do not summarize it in the email, but use it to inform the editorial angle.
