# remove-ai-slop

A Claude Code skill that detects and eliminates AI writing patterns — the statistical tells that mark text as machine-generated.

## What is AI slop?

Language models learn statistical associations between words. When generating text, they pull from the center of the distribution: the words and structures that most commonly appear together in their training data. The result is prose that is technically correct, often fluent, but recognisably generic.

Wikipedia calls this [Signs of AI writing](https://en.wikipedia.org/wiki/Signs_of_AI_writing). Researchers, editors, and readers have documented the patterns. This skill encodes them into an actionable checklist.

The problem is not that individual words are "bad". The problem is that AI-generated text uses them at frequencies that deviate measurably from human writing — both in how often they appear and in what combinations.

## Source

The vocabulary list and structural patterns in this skill are drawn primarily from:

**Wikipedia — [Signs of AI writing](https://en.wikipedia.org/wiki/Signs_of_AI_writing)**

That article aggregates findings from academic research, journalism, and community observation. It is a living document; this skill will need updates as AI writing patterns evolve.

## Vocabulary: annotated list

### Why these words?

Each word below appears in AI-generated text at statistically elevated rates compared to human-written text at similar quality levels. Some (like *delve*) were rare in human writing before LLMs became widespread. Others (like *crucial*, *key*) are simply overused to the point of meaninglessness.

| Word | Why it's flagged | Human alternative |
|------|-----------------|-------------------|
| **additionally** | AI's default conjunction; humans vary their connectives | *also*, *and*, restructure |
| **align with** | Corporate-speak for "match" or "fit" | *match*, *fit*, *follow* |
| **crucial** | Emphasis without content | Delete it; let the noun carry the weight |
| **delve** | Extremely rare in pre-LLM human writing | *explore*, *examine*, *look at* |
| **emphasizing** | Tells without showing | Rewrite to demonstrate the emphasis |
| **enduring** | AI's generic durability word | *lasting*, *persistent*, or be specific |
| **enhance** | Vague improvement | *improve*, *sharpen*, *add to*, *strengthen* |
| **fostering** | AI's default community/growth word | *building*, *encouraging*, *creating* |
| **garner** | Elevated diction for "get" | *earn*, *attract*, *collect* |
| **highlight** (verb) | Used where *show* or *note* would be clearer | *show*, *point to*, *note* |
| **interplay** | Abstract noun replacing a description | Describe the actual interaction |
| **intricate/intricacies** | Signals complexity without describing it | Describe what's actually complex |
| **key** (adj.) | Meaningless emphasis | Delete, or name why it matters |
| **landscape** (abstract) | *The landscape of X* = *X* | Name the actual thing |
| **pivotal** | Like *crucial*, emphasis without content | Delete; say what changed |
| **showcase** | Promotional framing | *show*, *demonstrate*, *display* |
| **tapestry** (abstract) | Poetic filler | Delete; name what you mean |
| **testament** | *Is a testament to* = *shows* | *shows*, *proves*, *demonstrates* |
| **underscore** (verb) | AI's favourite emphasis verb | *show*, *confirm*, *reinforce* |
| **valuable** | Vague positive | *useful*, or delete |
| **vibrant** | Decorative adjective | *active*, *lively*, or delete |

### Before/after examples

**Before:**
> The vibrant tapestry of influences that shaped the movement is a testament to the enduring interplay between tradition and innovation, fostering a landscape of creativity that continues to garner international attention.

**After:**
> The movement drew on folk music, protest poetry, and industrial labour traditions. By the 1970s it had audiences across Europe and South America.

---

**Before:**
> It is crucial to delve into the intricacies of the system to highlight the pivotal role that alignment plays in enhancing performance.

**After:**
> Understanding how the alignment system works explains the performance gains.

---

## Structural patterns

### The -ing causation trap

AI frequently appends a gerund clause to imply causation without demonstrating it.

**Before:**
> The team released the update, improving stability and reducing error rates.

**After:**
> The team released the update. Stability improved; error rates fell from 4.2% to 1.1%.

The after version makes the same claim with evidence. The before version implies it happened without saying how.

### The challenges/future formula

Almost every AI-generated summary ends with a version of this:

> *"Despite these achievements, [subject] faces challenges. Despite these challenges, the future looks promising."*

This formula appears because models are trained on encyclopedic and journalistic text that conventionally ends with forward-looking statements. It adds no information.

**Fix:** End on the last substantive fact. Let the reader draw their own conclusions.

### Significance inflation

AI adds significance markers to statements that should speak for themselves.

**Before:**
> The discovery marks a pivotal moment in our understanding of the disease, underscoring the importance of continued research and setting the stage for new treatments.

**After:**
> Researchers can now identify the protein responsible for cell death. This opens a path to drugs that block it.

### The "stands as" / "serves as" construction

AI avoids the verb *is* by using elaborate substitutes:

- *stands as* → *is*
- *serves as* → *is*, *acts as*
- *remains as* → *remains*, *is*
- *functions as* → *works as*, *is*

**Before:**
> The monument stands as a symbol of the city's resilience.

**After:**
> The monument is a symbol of the city's resilience.

Or better: describe what the monument actually is and why it was built.

## How to invoke this skill

Once installed (see the root README for installation steps):

```
Use the remove-ai-slop skill to review this draft.
```

Or:

```
/remove-ai-slop
```

Claude Code will load the skill and run the full checklist against your text.

## Limitations

- This skill catches patterns, not quality. Text can pass every check and still be bad.
- Some flagged words are appropriate in context. Use judgement.
- AI writing patterns evolve. The vocabulary list reflects patterns documented through 2025.
- The skill does not automatically rewrite text. It produces a structured review; you implement the changes.

## Contributing

If you find a pattern that should be added:

1. Check [Wikipedia's Signs of AI writing](https://en.wikipedia.org/wiki/Signs_of_AI_writing) — if it's documented there, cite it
2. Provide at least one before/after example
3. Open a PR against this repository
4. Read [CLAUDE.md](../../CLAUDE.md) before editing the `SKILL.md`
