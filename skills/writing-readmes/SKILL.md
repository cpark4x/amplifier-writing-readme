---
name: writing-readmes
description: Use when writing or rewriting a project README, or when a README draft feels generic, reads like a feature list, or fails the 30-second test — reader can't tell what it does or whether it's relevant to them.
---

# writing-readmes

A README is for humans. But increasingly, AI reads it first — someone pastes a repo link and says "explain this to me" or "should I use this?" The AI becomes the reader, the interpreter, and the recommender.

This doesn't mean you write for AI. It means the bar for clarity just went up. Vague descriptions that a human might skim past will cause an AI to misrepresent your project. A README that's clear enough for AI to explain correctly is a README that's clear enough for anyone.

## Before You Rewrite

Run the quality tests on the existing README first. If it passes, don't rewrite — suggest the 1-2 specific improvements that would make it better. A precise edit beats a rewrite every time.

**Look for buried gold.** Scan the project's docs, vision files, and design briefs for lines that are sharper than what's in the README. The best improvement is often pulling one compelling detail from a deeper document into the opening — a concrete number, a vivid example, a positioning line the author already wrote but didn't surface.

**Compress Built By.** One line: name, affiliation, motivation. Multi-line bios with degree and years of experience belong on LinkedIn, not in a README.

**Spike repos are fine as-is.** Learning projects, explorations, and failed experiments don't need the full treatment. A 4/10 README on a weekend spike is appropriate — don't over-engineer it.

**Preserve voice.** If the existing README has personality — humor, directness, a distinctive tone — that's a feature, not a bug. A rewrite that's more "correct" but less human is a downgrade. Match the author's voice, don't flatten it.

**Not every project needs the same README.** A consumer product paints a picture of the experience. A developer tool explains architecture. A library lets the code talk. Adjust your approach to the project, not the other way around.

## Five Principles

**1. Problem before solution.** Open with pain, not product. The reader should feel the problem before they see your name. A feature list is not an opening.

**2. Show, don't describe.** A before/after example is the most persuasive element in a README. For tools: show output. For libraries: show code. For visual projects: show a screenshot. For consumer products: paint the experience. The medium changes; the principle doesn't.

**3. Timing is respect.** Tell people how long things take — to install, to get a first result, to run the full pipeline. People make adoption decisions based on time investment.

**4. Honest about limits.** Name what you can't do yet. Credibility comes from specificity and honesty, not from silence.

**5. README pitches, usage guide teaches.** The README answers "why should I care?" in 60 seconds. The usage guide answers "how do I do this." If you're explaining configuration flags, you've crossed the line.

## Structure

Adapt weight by project type. Not every section needs equal depth.

| Section | What it covers | Weight by type |
|---|---|---|
| **Opening** | Problem → solution → what's different | Heavy for tools/products. Light for libraries (the code speaks). Skip the pitch for internal tools — go straight to usage. Consumer products: paint the experience, not the architecture. |
| **What it looks like** | Before/after, screenshot, code example, demo GIF | Heavy for visual projects and tools with output. A code snippet for libraries. Consumer products: describe the experience. **Keep examples under 10 lines.** Show the minimum that communicates the shape -- full format specs belong in docs, not here. |
| **Components** | What's in the box, user-facing only | Only if there are multiple components. Skip for single-purpose libraries and consumer products. |
| **Quick start** | Install → first result → "that's it" | Always heavy. This is the one section every README needs to nail. Lead with the simplest path (Docker one-liner > multi-step manual setup). |
| **Opening for bundles/plugins** | Problem → capability → install | Always start with the problem sentence before the capability description. "Sessions fill up and you lose your work" before "automatic session scope management." |
| **How it works** | User-perspective explanation of what happens | Medium for tools with pipelines or modes. Light or skip for simple libraries. Consumer products: keep it to 3 steps max. |
| **Built by** | Person, affiliation, motivation | One line. Always. |

### Opening

3-5 short paragraphs for tools and products. For libraries, 1-2 sentences plus a code example is often better — the code IS the pitch. For consumer products, paint a moment the reader recognizes — "You have a 45-minute commute and 12 tabs you'll never read" works because everyone's been there.

**Anti-patterns:**
- Starting with "[Project] is a..." or "A tool that..."
- Feature lists disguised as prose
- Buzzwords: "revolutionary", "cutting-edge", "next-generation"
- Implementation details before establishing why anyone should care

### Opening Patterns

Six shapes that problem openings take. Pick the one that fits your project:

| Pattern | Shape | Example | Best for |
|---|---|---|---|
| **The contradiction** | "X works but Y is broken" | "Your tests pass but the UI is broken." | Tools that fix a gap between what exists and what's needed |
| **The time bomb** | "You do X. Later, Y blows up" | "You build fast with AI. Three weeks later, no one can explain why any decision was made." | Tools that prevent future pain |
| **The relatable moment** | One sentence everyone's lived | "You have a 45-minute commute and 12 tabs you'll never read." | Consumer products, personal tools |
| **The mirror** | "Are you actually doing X?" | "You work with AI every day. Are you actually getting better at it, or just getting more done?" | Self-improvement, analytics, coaching tools |
| **The invisible cost** | "You spend X on Y" | "You spend 2 hours making 10 slides. Most of that time is formatting, not thinking." | Productivity tools, automation |
| **The honest failure** | "This didn't work. Here's what we learned." | "This project failed. That's the point." | Spikes, experiments, learning projects |

Don't force a pattern. Read the project, feel the problem, and the right shape usually emerges. If none fits, the project may not have a clear enough problem yet — and that's worth solving before writing the README.

### Quick start

The most important section for every project type. Must contain:
1. Install (one code block — lead with the simplest option)
2. First result (one concrete example — real-sounding, not placeholder text)
3. **Closure signal — "That's it" or equivalent.** This is the most underrated element in a README. The reader just followed your install steps and got a result. Tell them they've succeeded. Without it, they keep scrolling looking for more required steps. One sentence: "That's it -- you're running." Then link to the full guide for everything else.

## Quality Tests

Run all four before shipping. If the existing README passes, suggest targeted edits instead of rewriting.

**Substitution test.** Replace your project name with [PROJECT]. If the opening still works, it's too generic. Rewrite until removal of the name breaks the sentence.

**"So what?" test.** Read each sentence. If a reader could respond "so what?", you've described a feature instead of an outcome. "Uses advanced AI" → so what. "Zero fabricated claims on baseline evaluation" → specific, verifiable.

**30-second test.** Show the README to someone for 30 seconds. Can they tell you what it does and whether it's relevant to them? If not, it fails.

**Explain-it-back test.** Paste your README into an AI and ask "explain this project to me." If the AI gets it wrong or stays vague, your README isn't clear enough. This is the real-world test — it's what most people will actually do.

## The Tightening Pass

A README that passes all four quality tests can still be loose. Passing means the content is right. Tightening means the weight is right.

Run this after the quality tests pass, not before.

| Check | What to look for | Fix |
|-------|------------------|-----|
| **Opening paragraph count** | More than 2 paragraphs before the reader sees what the tool does? | Compress. Two paragraphs max: one for the problem, one for the solution. |
| **Example weight** | Code examples longer than 10 lines? | Trim to the minimum that communicates the format. Full reference examples belong in docs, not the README. |
| **Repeated pain** | The problem stated more than once in different words? | Pick the sharper version, delete the other. |
| **Closure signal** | Does Quick Start end with a clear "you're done" signal? | Add "That's it" or equivalent after the first result. The reader needs to know they've succeeded. |
| **Built By bloat** | More than one line? | One sentence. Motivation, not biography. |

**The test:** Read the README out loud. Every time you pause or lose energy, that's a section that's too long. Cut until the energy holds from top to bottom.

## What Bad Looks Like

> **MyTool** is a powerful, cutting-edge framework for automated research and analysis. It leverages state-of-the-art AI to produce comprehensive reports with advanced source verification capabilities.

Fails every test. Replace "MyTool" with anything — sentence still works. No problem stated. No specifics. Every adjective is doing the work a concrete claim should do.

## What Good Looks Like

**For a developer tool:**
> You ask an AI to research something and write it up. It reads well. Then someone asks "where did this number come from?" and you don't know. The document is fluent and completely unverifiable.

Pain first. Project name nowhere. The reader is nodding before you've introduced your solution.

**For a consumer product:**
> You have a 45-minute commute and 12 tabs you'll never read.

One sentence. You've been there. The product doesn't need to explain itself yet — the problem does.

**For a library:**
> ```python
> app = FastAPI()
>
> @app.get("/")
> def read_root():
>     return {"Hello": "World"}
> ```
> High performance, easy to learn, fast to code, ready for production.

Code first. Four claims, all testable. The code IS the pitch.
