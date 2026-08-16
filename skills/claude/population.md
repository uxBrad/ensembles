Populate an ensemble persona template from research artifacts through a structured, citation-tracked workflow.

## When to Use

- User says "populate an ensemble", "build an ensemble from my research", "fill in the template", "help me document [team name]"
- User has research artifacts and wants to build an ensemble document from them

---

## Inputs Required

Before starting, confirm you have:

1. **Ensemble name and context** — the name of the team or group being modeled, what product/project they exist within, and what kind of ensemble this is (specialist team, receiving product team, solo consultant, etc.)
2. **Research artifacts** — interview transcripts, observation notes, survey responses, support tickets, analytics, or any research that surfaces how this group actually behaves

**Critical:** If no research artifacts are provided, do not proceed with fabricated content. Explain that the population skill requires real research — the framework's entire value depends on documents being grounded in observation. Offer to run the simulation skill on an existing ensemble instead, or wait until research is available.

---

## Step 1: Read and absorb all research

Read every provided research artifact fully before populating anything.

After reading, note mentally:
- Which ensemble members appear by name or role? What did you observe or hear about each?
- What recurring behaviors, tensions, or dynamics surfaced across multiple sources?
- What is the ensemble's organizational context — reporting structure, mission, current pressures, recent history?
- What is conspicuously absent — what would you expect from a group like this that the research doesn't address?

Do not begin populating until you've read everything. Partial reading produces partial documents that look complete.

---

## Step 2: State what you observed before populating

Before writing the populated template, briefly report what you found:

```
## Pre-population summary

**Members identified:** [names or roles that appear in the research]
**Recurring dynamics:** [2–3 patterns that appear across multiple sources]
**Strongest evidence:** [what sections of the template will be most confident]
**Biggest gaps:** [what sections are likely to be sparse]
**Grounding quality:** [strong / moderate / thin — based on artifact depth and coverage]
```

This surfaces your interpretation before it gets embedded in the document, giving the researcher a chance to correct it.

---

## Step 3: Populate section by section

Work through the full ensemble template (from `templates/ensemble-template.md`) one section at a time. For each field, apply exactly one of these treatments:

**Direct evidence — populate with citation:**
```
[Field content] (Source: [artifact name — direct quote or specific observation])
```

**Indirect evidence — populate with inference tag:**
```
[Field content] [inferred — [brief reasoning from the evidence]]
```

**No evidence — leave empty:**
```
[insufficient research]
```

Do not fill gaps with plausible-sounding content. An empty field is honest. A fabricated field is harmful — it will be treated as evidence during simulations and produce false predictions.

When evidence could support multiple interpretations, surface both options instead of picking one:
```
[Interpretation A] OR [Interpretation B] — [note what additional observation would resolve this]
```

---

## Step 4: Write the populated document

Produce the full populated ensemble using the standard template structure:

- Section 1: Ensemble Identity (including Lightweight Version, Current State, Strengths/Blindspots)
- Section 2: The Roster (one entry per member)
- Section 3: Topology (power graph, trust graph, coalitions, friction, silence map, decision mode)
- Section 4: Repertoire (3–6 recurring scenes)
- Section 5: Stimulus-Response Spec

At the top of the document, add a grounding note:

```
**Grounding:** Partially research-grounded — [N] fields from direct evidence, [N] inferred, [N] gaps. See Gap Report below.
```

---

## Step 5: Produce the gap report

After the populated template, append a gap report:

```
## Gap Report

### Sparse sections
[List any section where more than half the fields are [insufficient research] or [inferred]. Explain what's missing.]

### What research would close the gaps
[Per sparse section: specific interview questions to ask, what to observe in meetings, what documents to request, or what analytics would help.]

### Confidence summary
- Fields populated from direct evidence: [N]
- Fields tagged [inferred]: [N]
- Fields marked [insufficient research]: [N]
- Overall confidence: [High / Medium / Low]

### Recommended next steps
[Is this ensemble ready to simulate against? If so, say so. If not, what's the minimum additional research needed before running a simulation would be meaningful?]
```

---

## Rules

- **Never fabricate.** Every field is evidenced, inferred (tagged), or empty. No exceptions.
- **Never do ensemble identification.** You populate a specific ensemble the user has already identified. If they haven't identified it yet — meaning they don't know who the members are or what context bounds this group — stop and help them think through identification before populating. That work requires their UX judgment, not AI assistance.
- **Flag ambiguity explicitly.** When research supports multiple interpretations, surface both. Let the researcher choose.
- **Respect the schema.** Populate fields as defined in `docs/schema.md` v1.0. Don't add fields without the user's approval. Don't skip sections — mark them as [insufficient research] if empty.
- **Lightweight version last.** The lightweight prose paragraph in Section 1 should be written after the rest of the template is populated — it's a summary, not a starting point.
