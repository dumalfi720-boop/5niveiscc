# Each level of Claude explained

This guide details the five stages of Claude mastery, from casual use to autonomous infrastructure. Each level describes the defining characteristics, the ceiling that stops people from advancing, and the exact "secret code" to get to the next stage.

\---

## I. Level 1: The Enthusiast

This is the starting point. You open Claude, ask a question, receive an answer and close the tab. Maybe you draft an email, write a quick script, or ask Claude to explain something he read. You save about 30 minutes a day on small tasks.

### 1\. The quick improvement most people ignore

Paste screenshots. Claude can read images. Half the people stuck on this level are typing what a screenshot would show in two seconds.

### 2\. Why do most people get stuck here

They don't realize that Claude can:

* Maintain context between conversations
* Organize work on projects
* Connect to the tools they already use every day

They continue to treat Claude like a search bar that happens to return paragraphs.

### 3\. Secret code for Level 2

Create your first project. Choose something you keep coming back to, like your business, a side project, or a recurring type of work. Put in some reference documents, write a quick system prompt about who you are and how you want Claude to respond. Now, every chat within this project starts preloaded.

\---

##II. Level 2: The Beginner

Projects are the backbone of Level 2. All other resources feed into a project or build on top of it. Open a new chat next Tuesday within your project, ask "What was that decision we made about launching Q2 last week?" and Claude retrieves the information with quotes.

### 1\. The six defining features

|Resource|What it does|Observations|
|-|-|-|
|Memory and search in previous chats|Claude remembers your role, preferences and decisions between conversations|Memory is free on all plans; the search in previous chats is paid |
|Connectors|Connects more than 50 tools, such as Slack, Google Drive, Gmail, GitHub, Notion and Calendar, via the plus button|Log in with OAuth and ask Claude to pull threads, documents or events directly|
|File creation|Generates real Excel files with functional formulas, PowerPoint presentations, Word documents and PDFs|Free for everyone; Includes customer-ready downloadable deliverables|
|Artifacts with persistent storage|Create applications that remember data between sessions, call the Claude API directly and can be published via public link|People without programming can create working tools without Lovable, Bolt or custom development|
|Embedded visuals|Graphs and diagrams created within the chat; temporary and interactive|Free on all plans; also available on Cowork|
|Native Office Add-ins|Claude lives inside Excel, PowerPoint, and Word as native add-ons|In April 2026, all three share context across applications|

### 2\. Division between free and paid

* Free for everyone: memory, file creation, built-in visuals
* Pro or higher: search past chats, persistent storage for artifacts, Office add-ons

### 3\. Where are you now

Level 1 was a brilliant intern with no memory. Level 2 is the same intern with a folder of project documents, all conversations remembered, and the ability to pull information from any tool without asking. You can save more than 5 hours a week. This is where Claude starts to pay for himself.

### 4\. The ceiling

Claude still can't really do anything on his machine. You keep copying outputs to other tools, making changes manually, and running certain things on your own. Claude's chat is the conversational surface, and you're about to surpass it.

### 5\. Secret code for Level 3

Stop trying to make chat solve everything. Open Claude Desktop and click on the Cowork tab.

\---

##III. Level 3: The Intermediate
This is where Claude stops telling you how to do something and just goes out there and does it. Point to your downloads folder, with three months of PDFs, screenshots, random files, old invoices, and pure chaos, and tell Claude: organize everything by type, rename it consistently, and write a summary for me. Go make a coffee; When you come back, you'll be ready.

Warning: Cowork is paid only. It comes with any Pro, Max, Team, or Enterprise plan.

### 1\. The five defining features

|Resource|What it does|
|-|-|
|File system access|Cowork runs code in an isolated VM with read and write access to the folders you grant. He can totally take over anything you allow him to touch|
|Skills|Reusable workflows defined as simple Markdown files. Create once, for example, "weekly customer report", and run anywhere. More than 100 already published, more than 16 official Anthropic, as well as a complete community marketplace|
|Scheduled tasks|Enter`/schedule`in any Cowork conversation. Daily 8am standups, weekly competitor briefs, monthly reports. Requires your computer to be turned on and the desktop app open |
|Mobile Control|Pair your phone to your desktop using Dispatch. Trigger tasks from anywhere, Claude works while you're away and notifies you when you're done |
|Claude Design|Anthropic Labs product included in Pro. Describe a prototype, presentation or landing page in natural language and Claude creates the design|

### 2\. What makes Claude Design different

Two things separate it from generic AI design tools:

* **Brand Awareness:** Submit a GitHub repository, codebase, design files, or brand guidelines. Claude creates a design system from your colors, fonts, and typography, then applies it to each project so the output looks like your brand, not some generic AI.
* **Handoff package:** When finished, Claude packages everything to Claude Code, Canva or a zip file. A person without programming can design a working frontend and push it to production via Claude Code without writing a line of code.

### 3\. Two more resources worth knowing

* **Plugins:** pre-created packages of skills, connectors, hooks and agents that you install with one click. Full marketplace available.
* **Computer Use:** For applications without connectors, Claude navigates visually by clicking, typing, switching tabs, and submitting forms. Available for Mac and Windows.

### 4\. Why do people get stuck here

* Some are scared by anything that seems technical, which is fair, but the desktop app doesn't require a terminal.
* Others hit the Cowork ceiling. It is safe and user-friendly, but less accurate than the next stage. When you need real version control, engineering rigor, or systems that customers pay $5,000+ for, you've got it.

This is the first level where you save more than 10 hours a week, and the first where people without programming can sell automation as a service. If you run an AI automation business, this is the minimum threshold.

### 5\. Secret code for Level 4

Set up a folder structure that Claude can trust:

* An archive about me
* A folder of templates
* A folder of projects
* A folder of outputs

Tell Cowork: "Read the about me file first. Never edit my templates. Always deliver to the outputs folder." This structure is what makes Cowork feel like a real coworker rather than an unpredictable assistant.

\---

##IV. Level 4: Advanced

Boris Cherny, the engineer who built Claude Code at Anthropic, runs five Claude sessions in parallel every day. Numbered terminal tabs, each in its own isolated workspace, without file conflicts. It triggers the sessions, exits, and returns to multiple pull requests completed and ready for review. This is not parallel productivity; is another category of work.

Note for non-programmers: the Code tab within Claude Desktop has the same engine as the terminal version. You don't need to use the CLI, but the terminal is faster once you get used to it.

### 1\. The five core features

#### A. The file`claude.md`A Markdown file in your project folder that Claude reads at the start of each session. Include:

* Its technical stack and naming conventions
* Who you are and what is the objective of the project
* Negative instructions, such as "never do X" or "never write with dashes"

Rules:

* Keep it below about 200 lines, as Claude reads it in every conversation, so excess costs tokens constantly.
* Put deeper details in separate files and reference with`@nome-do-arquivo`, so that Claude only reads them when necessary.
* The move that separates Level 4 users from everyone else: every time Claude makes a mistake, ask him to update the`claude.md`so as not to repeat the error. After a few weeks, he trains himself in how you work. The Anthropic team itself does this.

#### B. Planning mode

Press Shift + Tab twice. Claude reads your code, comes up with a plan, asks questions, and waits for approval.

Hidden configuration: Opus Plan. Opus does the planning, Sonnet does the execution. Smart model where it counts, cheap model for the heavy lifting. Reduces the cost by half without losing quality.

#### C. Subagents

Specialized Claudes for specialized jobs. One for testing, one for security review, one for documentation. Each one runs in its own context window, so that noise does not contaminate the main session, nor vice versa. Several subagents can run in parallel. In practice, it is a small engineering team that communicates through the main session.

#### D. Worktrees

Enter`claude-worktree nome-da-feature`. Claude creates an isolated Git workspace on his own branch. Open another terminal and do it again. Now you have two, three or four Claudes working simultaneously without overwriting each other's files. Three to four is the comfortable spot. Implement a feature in one, fix a bug in another, write tests in a third.

#### E. MCP, with a big asterisk

MCP, or Model Context Protocol, allows you to connect external tools to Claude, but Anthropic's documentation says: when there is a CLI tool for the job, use the CLI instead of MCP. Examples include GitHub, AWS, and Google Workspace. The CLI uses 60% to 70% fewer tokens because nothing enters context until you actually execute.

When you use MCP, the tool fetch feature, released in January 2026, automatically defers tool loading when MCP overhead passes 10% of the window, reducing overhead by 85% without configuration.

Tool priority order:

1. CLI first
2. API Endpoints Second
3. Third Skills
4. MCP only when nothing else fits

### 2\. High impact movements

|Movement|What it does|
|-|-|
|Master Your Context Window|The 1 million token window in Opus 4.7 is still fuzzy after 50% capacity. Use`/compact`to summarize old history proactively, not when warnings appear, because by then it's too late. Use`/context`to see where the tokens are going. With automatic prompt caching, costs drop by 60% to 90% in long sessions |
|Auto mode + focus|Stop pressing yes 30 times per session. Shift + Tab switches to automatic mode, in which Claude routes secure commands through a classifier. Enter`/focus`to hide intermediate steps and see only the final result. This is how Boris runs five parallel sessions |
|The checking cycle|According to Boris, this is the most important habit in Level 4. Give Claude a way to check his own work. Combine Claude Code with a Chrome extension so he can open a browser, test the interface, take screenshots, and iterate. He says this habit alone multiplied the quality of the output by 2 to 3 times |
|Custom slash commands|If you type the same prompt twice, make it a slash command. Boris uses`/commit-push-pr`dozens of times a day. The commandos live in`.claude/commands/`. Are shareable across teams and organizations|

### 3\. Side tools and slash commands

|Command|Purpose|
|-|-|
|`/rewind`or Esc twice|Removes a failed attempt from context completely, rather than contaminating the session with corrections; reverts to a previous message|
|`/btw`|Ask Claude something quick in the middle of the task without breaking the flow or adding noise to the main session|
|`/branch`, before`/fork`|Forks the current conversation at that exact point. Try one approach, come back, try another. Git for conversations. Combines with worktrees: one for parallel files, one for parallel reasoning |
|`/insights`|Reads your last month of Claude usage and generates a report on your patterns: repetitive tasks, wasted tokens, prompts to convert to skills, additions to`claude.md`. Run monthly|
|`/output style new`|Changes Claude Code's personality. Built-in modes include standard, explanatory, and learning. Create custom modes for code reviewer, direct mode or documentation writer|

### 4\. Where are you now

If Claude Chat was your intern and Cowork was your assistant, Claude Code is your engineering team. Each member can be specialized, work in parallel, and report to you. This is where freelance and agency jobs turn into $5,000 to $15,000 projects because you're building real systems and software, not just automations.

### 5\. Why do people get stuck here

They manage parallel work manually and become the bottleneck themselves. They fire Claudes, observe, switch contexts, and it just becomes AI babysitting.

### 6\. Secret code for Level 5

Find the most repetitive thing you do every week in Claude Code, like reviews, dependency checks, or manually executing the same skills and commands. This is your first cloud automation.

\---

## V. Level 5: The Architect

You close the laptop. The power goes out. You're at dinner, at the gym, sleeping. Someone opens a pull request on your repository. Claude sees, launches in the cloud, reviews the code, and posts detailed feedback with suggestions. When you look at your cell phone, everything is already done and you haven't touched anything.

### 1\. The three things that make it real

#### A. Cloud Routines

Claude Code saved configurations that run in the Anthropic cloud. Your machine remains turned off.

They are activated in three ways:

* On a schedule, such as daily backlog screening at 8am or weekly dependency audit on Mondays
* By an API call
* In response to a GitHub event, such as PR review at the time a pull request is opened

That's when Claude becomes infrastructure, not just a tool.

#### B. Hooks

Safety rails. Custom logic triggered on lifecycle events.

* Tool pre-use hooks block dangerous commands before they run
* Post-edit hooks automatically format every file Claude plays
* Stop hooks notify you in Slack when a long session ends
* Response hooks send a notification whenever Claude responds, so you can return to the tab

These are the differences between a cool demo and a production system that you trust with real work.

#### C. Channels

Control sessions outside the terminal: Discord, Telegram, iMessage on Mac or custom webhooks.

Two formats:

* **One-way:** external events trigger Claude. For example, a booking on the calendar triggers a search agent who prepares a client brief.
* **Two-way:** message Claude on the phone and he works against your real codebase.

### 2\. Additional pieces worth combining

|Resource|What it does|
|-|-|
|Headless mode|Claude Code runs without a human session. Pass a prompt with`claude -p`, receive the output back and forward to Slack, Datadog or another agent Claude|
|Agent SDK|Python and TypeScript libraries to create your own product based on the Claude Code engine. You stop being a user and become a builder|
|Remote Control|Connects your local Claude Code session to the Claude mobile app or any browser. Run`/remote-control`, scan the QR code and program it on your phone while walking, with the session running on your machine|
|Memory consolidation, or autodream|Background agent that clears memory files between sessions. Removes contradictory facts, merges duplicates and converts "yesterday" to real dates. Like human memory compression. Needs to be activated |
|Task Budgets|Opus 4.7 Beta. Give the agent a target of tokens for an entire execution, including thinking, tool calls, and output. The model adjusts and closes elegantly, instead of hitting a wall in the middle of the task. Currently only via API |
|Agent teams|Experimental. Several specialized Claudes coordinated by a lead agent. Unlike sub-agents, they can talk to each other, share a to-do list, debate and challenge each other. Uses a lot of tokens|

### 3\. The highest leverage skill at this level

It's not building from scratch, but discovering what already exists. The community has already published:

* More than 5,000 skills
* More than 800 MCP servers
* More than 3,000 marketplaces

Check X, Reddit, and GitHub for specific use cases. Pull a public open source repository and customize.

### 4\. The real lock on Level 5

This is not technical. It's about trust. Almost everyone can set up a cloud routine, but they don't, because handing over the steering wheel to a system that runs while you sleep seems reckless if you don't know what's going on underneath.

The solution is the same as learning to drive. You don't start on the road; It starts in an empty parking lot.

* Choose a low-risk routine, like a daily standup roundup that goes just to you, with no external submission
* Watch it run for weeks without touching
* Once you trust her, you will learn to trust her in the next 10 runs

### 5\. Implant responsibly

Publishing a routine to the cloud doesn't mean you can set it and forget it, especially if it's agentic. But automations that just take data from one place and put it somewhere else are generally safe because they are deterministic. Agentic skills and flows are more powerful, but not deterministic.

\---

## VI. The five levels at a glance

|Level|Name|Surface|What you save|Main unlock|
|-|-|-|-|-|
|1|Enthusiast|Chat from Claude|30 min/day|Paste screenshots; create the first project|
|2|Beginner|Projects + chat|More than 5 hours/week|Memory, connectors, file creation, artifacts, built-in visuals, Office add-ons|
|3|Intermediate|Cowork + Claude Design|More than 10 hours/week|Access to file system, skills, scheduled tasks, mobile control, design pipeline|
|4|Advanced|Claude Code|Projects from US$5,000 to US$15,000|`claude.md`, planning mode, subagents, worktrees, parallel sessions|
|5|Architect|Cloud routines + hooks|Leverage at the infrastructure level|Autonomous routines, hooks, channels, agent teams|

\---