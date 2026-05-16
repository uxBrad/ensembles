# Skills

AI skills for operating on ensemble persona documents. Each skill is a platform-agnostic markdown specification that can be implemented as a Claude skill, Cursor rule, GPT custom instruction, or equivalent.

**Status:** v1.0 — both skills built and available.

---

## Skills

### Population skill

**File:** `population-skill.md`

Populate an ensemble persona template from research artifacts through a structured, citation-tracked workflow. Every field is either evidenced (with citation), inferred (tagged), or explicitly empty — never fabricated.

Use this when you have research artifacts (transcripts, notes, tickets, analytics) and want to build an ensemble document from them.

### Simulation skill

**File:** `simulation-skill.md`

Run a stimulus against a populated ensemble document and produce a structured prediction report: per-member predictions, an evidence trail linking every claim to the document, a confidence map (high/medium/low), and research gaps.

Use this when you want to ask "how would [ensemble] react to [feature/scenario/change]?"

---

## The pipeline

These skills handle two of the three stages in the ensemble workflow:

1. **Identification** — researcher-only, no AI. Decide who the ensemble members are and what context bounds this group. Clustering from research requires UX judgment that AI cannot reliably substitute.

2. **Population** (population skill) — fill the template from research artifacts with full citation tracking.

3. **Simulation** (simulation skill) — run stimuli against the populated document and produce predictions.

Don't skip population. Running simulation against a fabricated or hypothetical ensemble produces hypothetical predictions — which the framework is explicit about, but which undermines the value of running the simulation in the first place.

---

## Manual equivalents

Both skills can be run manually without AI:

- **Manual population:** Read research artifacts, fill in the template, cite evidence per field, leave gaps as [insufficient research]. Slower but produces equivalent output with discipline.
- **Manual simulation:** Read a populated ensemble document with a stimulus in mind. Work through each member's Roster entry, reason through their likely reaction, trace each claim to the document, and note where the document is thin.

The skills accelerate both workflows and enforce consistency. They are not prerequisites for using the framework.
