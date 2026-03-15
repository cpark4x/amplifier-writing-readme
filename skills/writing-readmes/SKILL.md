---
name: writing-readmes
description: Use when writing or rewriting a project README, or when a README draft feels generic, reads like a feature list, or fails the 30-second test — reader can't tell what it does or whether it's relevant to them.
---

# writing-readmes

A README is for humans. But increasingly, AI reads it first — someone pastes a repo link and says "explain this to me" or "should I use this?" The AI becomes the reader, the interpreter, and the recommender.

This doesn't mean you write for AI. It means the bar for clarity just went up. Vague descriptions that a human might skim past will cause an AI to misrepresent your project. A README that's clear enough for AI to explain correctly is a README that's clear enough for anyone.

## Five Principles

**1. Problem before solution.** Open with pain, not product. The reader should feel the problem before they see your name. A feature list is not an opening.

**2. Show, don't describe.** A before/after example is the most persuasive element in a README. For tools: show output. For libraries: show code. For visual projects: show a screenshot. The medium changes; the principle doesn't.

**3. Timing is respect.** Tell people how long things take — to install, to get a first result, to run the full pipeline. People make adoption decisions based on time investment.

**4. Honest about limits.** Name what you can't do yet. Credibility comes from specificity and honesty, not from silence.

**5. README pitches, usage guide teaches.** The README answers "why should I care?" in 60 seconds. The usage guide answers "how do I do this." If you're explaining configuration flags, you've crossed the line.

## Structure

Adapt weight by project type. Not every section needs equal depth.

| Section | What it covers | Weight by type |
|---|---|---|
| **Opening** | Problem → solution → what's different | Heavy for tools/products. Light for libraries (the code speaks). Skip the pitch for internal tools — go straight to usage. |
| **What it looks like** | Before/after, screenshot, code example, demo GIF | Heavy for visual projects and tools with output. A code snippet for libraries. |
| **Components** | What's in the box, user-facing only | Only if there are multiple components. Skip for single-purpose libraries. |
| **Quick start** | Install → first result → "that's it" | Always heavy. This is the one section every README needs to nail. |
| **How it works** | User-perspective explanation of what happens | Medium for tools with pipelines or modes. Light or skip for simple libraries. |
| **Built by** | Person, affiliation, motivation | One line. Always. |

### Opening

3-5 short paragraphs for tools and products. For libraries, 1-2 sentences plus a code example is often better — the code IS the pitch.

**Anti-patterns:**
- Starting with "[Project] is a..." or "A tool that..."
- Feature lists disguised as prose
- Buzzwords: "revolutionary", "cutting-edge", "next-generation"
- Implementation details before establishing why anyone should care

### Quick start

The most important section for every project type. Must contain:
1. Install (one code block)
2. First result (one concrete example — real-sounding, not placeholder text)
3. "That's it." or equivalent signal that the reader is done
4. Link to full guide for everything else

## Quality Tests

Run all four before shipping:

**Substitution test.** Replace your project name with [PROJECT]. If the opening still works, it's too generic. Rewrite until removal of the name breaks the sentence.

**"So what?" test.** Read each sentence. If a reader could respond "so what?", you've described a feature instead of an outcome. "Uses advanced AI" → so what. "Zero fabricated claims on baseline evaluation" → specific, verifiable.

**30-second test.** Show the README to someone for 30 seconds. Can they tell you what it does and whether it's relevant to them? If not, it fails.

**Explain-it-back test.** Paste your README into an AI and ask "explain this project to me." If the AI gets it wrong or stays vague, your README isn't clear enough. This is the real-world test — it's what most people will actually do.

## What Bad Looks Like

> **MyTool** is a powerful, cutting-edge framework for automated research and analysis. It leverages state-of-the-art AI to produce comprehensive reports with advanced source verification capabilities.

Fails every test. Replace "MyTool" with anything — sentence still works. No problem stated. No specifics. Every adjective is doing the work a concrete claim should do.

## What Good Looks Like

**For a tool/product:**
> You ask an AI to research something and write it up. It reads well. Then someone asks "where did this number come from?" and you don't know. The document is fluent and completely unverifiable.

Pain first. Project name nowhere. The reader is nodding before you've introduced your solution.

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
