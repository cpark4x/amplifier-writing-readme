---
name: writing-readmes
description: Use when writing or rewriting a README for any project. Covers dual-audience structure (humans scanning GitHub + AI agents parsing for capabilities), problem-first opening, concrete output examples, and quality criteria.
---

# Writing READMEs

## Overview

A README serves two audiences simultaneously: a human deciding whether to try your project, and an AI agent parsing to understand capabilities and routing decisions. Every sentence should serve at least one, ideally both.

## Principles

**Problem before solution.** Start with pain the reader recognizes. The reader should feel uncomfortable before you offer relief. A feature list is not an opening.

**Show, don't describe.** One before/after example is worth more than three paragraphs of explanation. Show actual output.

**Timing is respect.** Tell people how long things take. If your tool has different speed modes, name them with times.

**Honest about limits.** Name what the tool doesn't do and where it's improving. Credibility comes from specificity and honesty, not from silence.

**README pitches, usage guide teaches.** The README answers "why should I care?" in 60 seconds. The usage guide answers "how do I do this?" Don't mix them.

## Structure

Six sections, each earning its place:

### 1. Opening (most important)

3-5 short paragraphs. No bullet lists, no headers. Must:

- Start with a visceral problem, not a feature description
- Make the reader feel the pain before offering relief
- Explain what's architecturally different, not just "better"
- Mention speed/timing naturally
- Include a concrete quality or credibility signal

**Test:** Replace your project name with [PROJECT]. If the opening still works, it's too generic.

**Anti-patterns:**
- Starting with "[Project] is a..." or "A tool that..."
- Feature lists disguised as prose
- Buzzwords: "revolutionary", "cutting-edge", "next-generation"
- Implementation details before establishing why anyone should care

### 2. What the output looks like

Before/after side by side. The naive/typical approach vs your project's output. The contrast should be visceral — no explanation needed. Close with a single line reinforcing what the example proved.

### 3. Components table

Split into primary and secondary if many. Two columns: Name and What it does. Drop internal components users don't invoke. Cut status columns unless versions differ.

### 4. Quick start

Simplest path to a first result:
1. Install (one code block)
2. Use it (one concrete example with a real-sounding request, not placeholder text)
3. "That's it."

Link to full usage guide for everything else.

### 5. How it works

Explain what happens from the user's perspective, not how it's built. If multiple modes exist, describe each: what triggers it, what happens, how long, what you get. End with the stability contract.

### 6. Built by

Real person. Real affiliation. One line about why this exists. Skip inflated titles.

## Quality Checklist

Rate each dimension 1-10. Target 8+ on all:

| Dimension | Question |
|---|---|
| Problem clarity | Does the reader feel the pain in the first paragraph? |
| Solution clarity | Can they explain what your project does after 30 seconds? |
| Concreteness | Is there at least one before/after example? |
| Dual-audience | Would both a human and an AI agent get what they need? |
| Timing | Does the reader know how long things take? |
| Honesty | Are limitations named? |
| Scannability | Can someone get the gist from bold text and headers alone? |
| Length | Is every section earning its place? |

## Common Mistakes

**Writing for developers only.** AI agents need capability signals, invocation patterns, and routing boundaries — not just human-readable prose.

**Burying the quick start.** If someone scrolls past philosophy and architecture to find the install command, they leave.

**Repeating across README and usage guide.** If both say the same thing, one is redundant. README pitches; usage guide teaches.

**Feature lists instead of outcomes.** "Source tiering, per-claim confidence, evidence gaps" is a feature list. "Output you can stake your reputation on" is an outcome. Lead with outcomes.

**No timing information.** A 15-minute pipeline feels different from a 15-second API call. Name it.

## For AI Agents

When writing a README using this skill:
1. Read the project's code/docs to understand what it does
2. Identify the core problem it solves — what pain does the user have today?
3. Find or create a concrete before/after example
4. Draft using the six-section structure
5. Self-rate against the quality checklist
6. Revise any dimension below 8
7. Present to the user for review — don't apply without confirmation
