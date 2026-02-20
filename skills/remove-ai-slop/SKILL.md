---
name: remove-ai-slop
description: Use when writing, editing, or reviewing text to detect and eliminate AI writing patterns — overused vocabulary, puffery, superficial analyses, formulaic structures, and other tells catalogued by Wikipedia's Signs of AI Writing.
---

# Remove AI Slop

## Overview

AI writing is statistically predictable. Language models trained on human text learn which words and structures cluster together — and then over-apply them, producing prose that feels polished but reads as generic. The result: text that sounds like it was written by a model, because it was.

This skill systematically identifies and removes those tells.

## Words to Avoid

These appear in AI writing at frequencies far above human baselines. Replace with specific, concrete alternatives.

| Flag | Replace with |
|------|--------------|
| additionally | also, and, [restructure the sentence] |
| align with | match, fit, suit, follow |
| crucial | [delete it — just say what it does] |
| delve | explore, examine, look at |
| emphasizing | [rewrite to show, not tell] |
| enduring | lasting, persistent, [be specific] |
| enhance | improve, sharpen, add, strengthen |
| fostering | building, encouraging, creating |
| garner | earn, attract, collect, get |
| highlight (verb) | show, point to, note |
| interplay | interaction, tension, relationship |
| intricate/intricacies | [describe what's actually complex] |
| key (adjective) | [delete or name the actual importance] |
| landscape (abstract) | [name the actual thing: market, field, situation] |
| pivotal | [delete — say what changed] |
| showcase | show, demonstrate, display |
| tapestry (abstract) | [delete — name the actual thing] |
| testament | evidence, proof, sign |
| underscore (verb) | show, confirm, reinforce |
| valuable | useful, [delete if filler] |
| vibrant | active, lively, [delete if decorative] |

## Structural Patterns to Eliminate

### Superficial -ing Analyses

Using a gerund to describe effects without explaining mechanisms.

- Bad: *The policy succeeded, **strengthening** public trust.*
- Bad: *The update shipped, **improving** performance.*
- Fix: State what actually happened. "Public trust rose 12 points after the policy was implemented" beats the gerund version every time.

### The Challenges/Future Formula

AI summaries almost always end with:
> "Despite these achievements, [subject] faces challenges. Despite these challenges, [subject] has a bright future."

Cut both sentences. They add no information.

### The Rule of Three

AI defaults to three parallel points. When you notice three bullet points, three adjectives, three examples — check whether two would be sharper.

### Not-Only-But Parallelism

"Not only... but also..." constructions appear at AI-baseline rates. Replace with direct statements.

- Bad: *The tool is not only fast but also accurate.*
- Fix: *The tool is fast and accurate.*

### Is/Are Avoidance

AI often replaces a simple "is" with a more elaborate construction:

- Bad: *The bridge **stands as** a symbol of progress.*
- Bad: *The report **serves as** a foundation for...*
- Fix: *The bridge **is** a symbol of progress.* Or better: say what the bridge actually does.

### False Ranges

Vague quantifiers that avoid committing to a number:

- Bad: *between 50 and 100* (when you could just say 73, or "about 75")
- Bad: *various*, *numerous*, *a number of*
- Fix: use the actual number, or "several" (≈3–7) or "many" (larger, vague but honest).

### Title Case Headings

AI uses Title Case For Every Heading. Use sentence case unless proper nouns are involved.

- Bad: **Key Takeaways From The Report**
- Fix: **Key takeaways from the report**

### Em Dash Overuse

Em dashes used for emphasis every few sentences — like this — signal AI authorship. Use sparingly: once per page at most.

## Content Patterns to Eliminate

### Significance Puffery

- *marks a pivotal moment in*
- *underscores its importance*
- *plays a vital role in*
- *is a testament to*
- *reflects broader [trends/questions/concerns]*
- *setting the stage for*

Delete these. State the fact directly. If the significance is real, the reader will feel it.

### Promotional Language

- *nestled in the heart of*
- *rich cultural heritage*
- *breathtaking [views/scenery/etc.]*
- *world-class*
- *cutting-edge*

All of these are advertising copy. Delete or replace with specific, verifiable claims.

### Vague Attributions

- *experts say*
- *studies show*
- *research suggests*

Name the expert. Cite the study. If you can't, don't make the claim.

### Section Summaries

"In summary", "In conclusion", "Overall" followed by a restatement of what was just written. Delete. The reader just read it.

## Quick Fix Checklist

Run this before finalising any text:

- [ ] Searched for every word in the "Words to Avoid" table and replaced or deleted
- [ ] Removed all significance puffery phrases
- [ ] Cut the challenges/future formula from endings
- [ ] Converted title-case headings to sentence case
- [ ] Replaced vague attributions with named sources or deleted the claim
- [ ] Cut section summaries ("In conclusion", "Overall")
- [ ] Checked for em dash density — max one per page
- [ ] Verified all -ing clauses describe a real causal mechanism, not just correlation
- [ ] Replaced false ranges with actual numbers where available
- [ ] Read the final text aloud — if it sounds like a press release, revise

## Common Mistakes

Things agents (and humans) tell themselves to skip this cleanup:

- *"The reader won't notice."* — Readers notice. They just can't always name what's wrong.
- *"It's not that bad."* — AI slop compounds. One "pivotal" is fine; six is a pattern.
- *"Removing it changes the tone."* — Correct. That's the goal.
- *"I need it for flow."* — Connective tissue words rarely add flow; they add length.
- *"This was written by a human."* — The patterns are still present. Remove them.
