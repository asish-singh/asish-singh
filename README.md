# Asish Singh

**Project management for AI delivery.** I write the specifications, definitions of done, and acceptance criteria that turn AI assistants into something that reliably ships, and I publish the measurements behind every claim I make about it.

My working thesis is one sentence. AI teammates are only as reliable as the definition of done they are given, and writing that definition is a project management skill.

### AI enablement

Most discussion of AI at work argues about model capability. I think the binding constraint is elsewhere, in how the work is specified, delegated, reviewed, and accepted. So I test that directly.

[**ai-pm-benchmark**](https://github.com/asish-singh/ai-pm-benchmark) asks a question nobody had measured publicly. Models are benchmarked heavily on coding and mathematics, but how good are they at project management itself? Eight freely available models are scored on scheduling and critical path, estimation, prioritization, risk identification, and stakeholder communication. Objective tasks are graded by code against hand verified answer keys. Subjective tasks go to a blind judge working from anchored rubrics. A GitHub Actions job runs it daily and commits the raw responses, so the repository is both the database and the audit trail. Results stay labeled preliminary until each model reaches 30 scored repetitions.

[**shipped-without-engineers**](https://github.com/asish-singh/shipped-without-engineers) is the method itself, written for people who delegate to AI rather than for engineers. Discovery interview, written sign off, a checkable definition of done, cheap models doing the labor, an expensive model doing the judgment, cross model review, and acceptance only against the definition. Every handoff from one real build is saved unedited, including the rejections and the rework, because evidence that only shows successes is not evidence.

### Selected work

| Project | What it is | Result |
|---|---|---|
| [agentic-erp-demo](https://github.com/asish-singh/agentic-erp-demo) | Can an AI agent operate ERP business processes? An agent loop against SAP's public sandbox APIs, every model response and API call logged | Four of five tasks succeeded. Creating a purchase order returned HTTP 405, so the public evaluation surface of the largest ERP vendor lets an agent look but not act |
| [agent-safety-scanner](https://github.com/asish-singh/agent-safety-scanner) | Measurement study of hidden text aimed at AI agents, sampled from the Tranco top million ranking | Across roughly 3,000 reachable sites and more than 180,000 pieces of hidden text, the count of instructions aimed at agents was zero. A clear negative result, published as one |
| [agent-readiness-auditor](https://github.com/asish-singh/agent-readiness-auditor) | Command line tool scoring any website on nine checks for how well it works with, and defends against, AI agents | Published on npm under MIT, and it ships as an MCP server so an assistant can run the audit itself |
| [code-as-harness-whitepaper](https://github.com/asish-singh/code-as-harness-whitepaper) | Controlled experiment isolating a single variable, whether the model may execute code | 96 graded sessions. Accuracy moved from 83 percent to 100 percent where an executable ground truth exists, and the advantage measured exactly zero where none does, which locates the boundary of the mechanism |
| [telephone-game](https://github.com/asish-singh/telephone-game) | A traced case study of how an instruction drifts from human intent through an orchestrating AI down to coding subagents | 7 of 9 requirements survived intact. Both mutations happened at the very first hop, where intent became instructions, and neither was ever revisited |
| [agentic-web-index](https://github.com/asish-singh/agentic-web-index) | Quarterly benchmark ranking a panel of 200 sites across twelve sectors on agent readiness | Panel, raw results, and the audit service are all public, so any figure can be recomputed rather than taken on trust |
| [freeyoutubetranscribe.com](https://freeyoutubetranscribe.com) ([source](https://github.com/asish-singh/freeyoutubetranscribe.com)) | A free YouTube transcript tool built in 2026 without a server fetching anything, the visitor's own browser reads the public captions, and every transcript anyone reads becomes a public page in a library that now holds about ten thousand videos in nearly sixty languages. Transcripts can be translated into any language YouTube offers, summarised on the device with Chrome's built in model, and, for videos without captions, transcribed live on the device with an open source speech model | Shipped and operated as a project management exercise, specification first, implementation by AI coding agents, acceptance by measurement. Right to left support for Arabic, Persian and Urdu, a Telegram bot, and a weekly measured report are part of the build |

### How I work

Specify before building. A discovery interview first, then a written specification signed off before work starts, because ambiguity discovered late is the expensive kind.

Make done checkable. Acceptance runs against a definition written in advance, so it is a test rather than an opinion.

Match the model to the job. Cheap models do the labor, an expensive model does the judgment, and a second model reviews the first one's output before I see it.

Trace every number. Any figure that reaches a published claim traces back to a raw log or dataset committed in the repository. Where a result is preliminary, it says so.

Publish negatives. The scanner study found nothing, and that is the finding. A method that can only produce exciting results is not a method.

### Contact

[asishsingh.in](https://asishsingh.in) · asish.singh@alumni.ashoka.edu.in
