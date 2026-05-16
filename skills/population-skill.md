# Skill: Ensemble Population

**Status:** Built (v1.0)
**Schema compatibility:** Ensemble Personas v1.0
**Platform:** Platform-agnostic spec. Reference implementation: Claude (via Claude Code skill)

Populate an ensemble persona template from research artifacts through a structured, citation-tracked workflow. Every field is either evidenced (with citation), inferred (tagged), or empty — never fabricated.

---

## What this skill does

You provide research artifacts — transcripts, observation notes, surveys, support tickets, analytics — and the skill works through the ensemble template systematically, populating fields only where the research supports it. Where evidence is indirect, it tags the inference. Where evidence is absent, it leaves the field empty and surfaces the gap explicitly.

The output is a populated ensemble document and a gap report telling you what research would close the gaps.

---

## Inputs

1. **Ensemble name and context** — the name of the group being modeled, the product or project context, and what type of ensemble this is (specialist team, receiving product team, solo consultant, embedded auditor, etc.)

2. **Research artifacts** — any combination of:
   - Interview transcripts
   - Observation session notes
   - Survey results
   - Support tickets or user feedback
   - Analytics or behavioral data
   - Internal documents (org charts, meeting notes, retrospectives)

**Important:** This skill requires real research artifacts. If no research exists yet, the skill will not fabricate. The value of the framework depends entirely on documents being grounded in observation.

---

## Output

### 1. Pre-population summary
Before writing the document, the skill reports what it found in the research:
- Which members appear by name or role
- Recurring dynamics observed across multiple sources
- Which sections will be most and least confident
- Overall grounding quality assessment

This surfaces the AI's interpretation before it's embedded in the document, giving the researcher a chance to correct it.

### 2. Populated ensemble document
The full ensemble template populated field by field, using three treatments:

**Direct evidence:**
```
[Field content] (Source: [artifact name — direct quote or observation])
```

**Inferred from evidence:**
```
[Field content] [inferred — brief reasoning]
```

**No evidence:**
```
[insufficient research]
```

When evidence supports multiple interpretations, both are surfaced with a note on what would resolve the ambiguity — the researcher chooses, not the AI.

### 3. Gap report
Appended to the populated document:
- Which sections are sparse (more than half the fields are empty or inferred)
- What specific research would close each gap (interview questions, observation targets, document types)
- Confidence summary: N fields from direct evidence, N inferred, N gaps
- Whether the ensemble is ready to simulate against, or what minimum additional research is needed first

---

## Implementation constraints

These constraints are non-negotiable for any implementation of this skill:

1. **Never fabricate.** Every field is evidenced, inferred (tagged), or empty. Plausible-sounding content that isn't grounded in research is more dangerous than an empty field — it will be treated as evidence during simulations.

2. **Never do ensemble identification.** The skill populates a specific ensemble the researcher has already identified. Identification — deciding who the members are and what context bounds this group — requires UX judgment and researcher expertise. If the researcher hasn't done identification yet, stop and help them think through it before populating.

3. **Flag ambiguity.** When research could support multiple interpretations of a field, surface both options rather than choosing. Let the researcher decide.

4. **Respect the schema.** Populate fields as defined in `docs/schema.md` v1.0. Don't add fields without explicit researcher approval. Don't omit sections — mark them [insufficient research] if empty.

5. **Lightweight version last.** The lightweight prose paragraph in Section 1 summarizes the populated document — write it after the rest of the template is complete, not before.

6. **Debrief before populating.** The pre-population summary step is not optional. It's the check that catches misinterpretation before it gets embedded in the document.

---

## Manual equivalent

If you're not using an AI skill, you can populate manually:

1. Read all research artifacts before touching the template.
2. Work through the template section by section.
3. For each field: find the evidence, write what it supports, cite the source.
4. Mark inferences with [inferred] and brief reasoning.
5. Leave genuine gaps as [insufficient research] — don't fill them.
6. Write the lightweight prose version last.
7. Write the gap report after the template is complete.

The skill accelerates this and enforces discipline. It's not a prerequisite for using the framework.

---

## The identification / population / simulation pipeline

This skill handles the middle stage of a three-stage pipeline:

1. **Identification** (researcher only, no AI) — decide who the ensemble members are and what context bounds this group. Clustering from research requires UX judgment that AI cannot reliably substitute.

2. **Population** (this skill) — fill the template from research artifacts with full citation tracking.

3. **Simulation** (see `simulation-skill.md`) — run stimuli against the populated document and produce predictions.

Don't run simulation against an unpopulated or fabricated ensemble. The pipeline only works if population is honest.

---

## Version history

| Version | Date | Notes |
|---|---|---|
| 1.0 | 2026-05-16 | Initial release |
