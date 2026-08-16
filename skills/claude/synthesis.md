Turn raw research data into a populated ensemble document, with per-field evidence trails, explicit gaps, and surfaced contradictions.

This is the highest-risk skill in the framework. Synthesis is inferential work, and the temptation to fabricate plausible content is high. This skill is deliberately conservative: it produces documents with honest gaps rather than documents that look complete. Hold that conservatism as non-negotiable.

## When to Use

- User says "synthesize this research", "turn these interviews into an ensemble", "help me build an ensemble from raw notes/transcripts"
- User has raw, unsynthesized research (transcripts, observation notes, tickets, other artifacts) rather than already-organized findings

If the user already has synthesized findings and just needs them mapped onto the template, use the **population** skill instead — synthesis is for raw data, population is for already-synthesized evidence.

---

## Inputs Required

Before starting, confirm you have:

1. **Raw research data** — one or more transcripts, observation notes, tickets, or other artifacts
2. **Which ensemble this is** — the researcher must have already identified who the members are and what context bounds this group. This skill does not do ensemble identification; that clustering work requires UX judgment. If the researcher hasn't identified the ensemble yet, stop and help them think through identification before running synthesis.

---

## Step 1: Read and segment

Read through each piece of research data. For each section of the schema (Identity, Roster, Topology, Repertoire, Stimulus-Response), identify which parts of the research are relevant.

Don't produce any claims yet. Just map research content to schema sections.

Output a structured map: for each schema field, which artifacts contain relevant content, referenced by document and approximate location (e.g., "INT-03, around the question about decision-making").

---

## Step 2: Extract evidence

For each schema field, extract the specific evidence from the research artifacts. This is direct extraction, not inference. Quote where appropriate. Note participant attributions.

Still no claims about the team at this stage — just gather what could support claims.

Output: for each schema field, a structured list of evidence items with attributions. Some fields will have many; some will have few or none.

---

## Step 3: Synthesize with epistemic discipline

For each schema field, evaluate what claims the evidence supports, applying this discipline:

- **Strong evidence (multiple sources, consistent):** Make the claim directly, with evidence trail.
- **Moderate evidence (single source or partial):** Make the claim, marked `[inferred]`, with a note on what supports the inference.
- **Weak evidence (suggestive but thin):** Make a hedged claim marked `[low confidence]`, or note it as a gap instead.
- **No evidence:** Leave the field empty, marked `[insufficient research]`.

Never produce a claim that doesn't have evidence behind it. This is the constraint that prevents fabrication.

**Surface contradictions, don't resolve them.** When two pieces of evidence support different claims for the same field, don't pick one. Note the contradiction and present both perspectives. Don't assess which participant is "right" — that's the researcher's call.

Output: a populated ensemble document with per-field evidence trails, confidence markers, surfaced contradictions, and explicit gaps.

---

## Step 4: Generate the gap report

Identify the gaps from Step 3 and assess their importance. For each significant gap, propose specific follow-up actions:

- What question would close this gap?
- Who could the researcher ask?
- Is there an existing artifact (a ticket, a document, a record) that might already contain the answer?
- Could a brief follow-up message to a previous interviewee close it?

Prioritize gaps by likely impact on the document's usefulness, not by completeness for its own sake.

```
## Gap Report

### Contradictions surfaced
[Field: both perspectives, with attribution. No adjudication.]

### Sparse sections
[Sections where more than half the fields are empty or inferred.]

### Prioritized follow-ups
[Per significant gap: the question, who to ask, and any existing artifact that might already answer it.]

### Confidence summary
- Fields from direct evidence: [N]
- Fields tagged [inferred]: [N]
- Fields tagged [low confidence]: [N]
- Fields marked [insufficient research]: [N]
```

---

## Rules

- **Evidence first, claims second.** The flow is "what evidence do you have, what does it support, what claim follows" — never "what's the right answer, then find evidence for it." That ordering is the difference between synthesis and motivated reasoning.
- **Empty fields are correct outputs, not failures.** Don't try to populate them creatively. An empty field with no evidence is more honest than a plausible-sounding guess.
- **Inference is allowed, but must be marked.** Real synthesis requires drawing connections across multiple pieces of evidence. Mark every inference and say what it's based on.
- **Confidence is first-class, not buried metadata.** Every claim carries its confidence level visibly in the document itself.
- **Never do ensemble identification.** You synthesize a specific, already-identified ensemble. Don't decide who belongs in it.
- **Never assess truth between conflicting sources.** Surface the contradiction; let the researcher adjudicate.
- **This produces a draft, not a final document.** The researcher reviews every claim before the ensemble is considered done. Say this explicitly when you hand back the output.
- **Follow `docs/research-methodology.md`.** This skill operationalizes the synthesis principles there. If that document changes, defer to it over this skill's own phrasing.
