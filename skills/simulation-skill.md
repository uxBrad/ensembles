# Skill: Ensemble Simulation

**Status:** Built (v1.0)
**Schema compatibility:** Ensemble Personas v1.0
**Platform:** Platform-agnostic spec. Reference implementation: Claude (via Claude Code skill)

Run a stimulus against a populated ensemble persona document and produce a structured prediction report with per-member predictions, an evidence trail, a confidence map, and research gaps.

---

## What this skill does

You provide a populated ensemble document and a stimulus to test against it. The skill produces a simulation report that predicts how the ensemble will react — broken down by member, supported by citations from the document, and honest about where the document doesn't support a confident prediction.

This is the operational payoff of building ensemble documents. Without this skill (or equivalent manual work), an ensemble is a description. With it, an ensemble is a predictive tool.

---

## Inputs

1. **A populated ensemble document** — following the v1.0 schema (Identity, Roster, Topology, Repertoire, Stimulus-Response). The richer and more research-grounded the document, the more confident the predictions.

2. **A stimulus** — what you're testing. Can be:
   - A product feature description
   - A requirements or constraint document
   - An organizational change
   - An external event (regulation, market shift, lawsuit)
   - A message or communication
   - A process or workflow change

---

## Output format

The simulation report has six sections:

### 1. Stimulus
The description of what's being tested, clearly stated.

### 2. Predicted Reaction
- **Overall ensemble response** — 2–3 sentences on how the ensemble as a whole will respond, drawing on topology and identity.
- **Per-member predictions** — for each member in the Roster: their likely stance, the mechanism driving it (archetype, signature moves, what modulates them), and any verbatim anchors that apply. 3–6 sentences per member.
- **Net response prediction** — the likely collective outcome. Whether the stimulus is adopted, resisted, contested, or ignored. Tipping points named explicitly.

### 3. Evidence Trail
A table linking every significant prediction claim to the specific field or scene in the ensemble document that supports it. Every claim must be traceable. Claims that can't be traced must be either removed or explicitly flagged as inferences not supported by the document.

### 4. Confidence Map
Three layers:
- **High confidence** — directly supported by the document
- **Medium confidence** — reasonable inference from documented patterns
- **Low confidence / cannot predict** — where the document lacks sufficient information

If the document is hypothetical or lightly populated, most predictions will fall in medium or low. The skill is honest about this rather than inflating confidence.

### 5. Research Gaps
What additional research would close the low-confidence predictions. Specific about what type of research would help.

### 6. Implications
3–5 bullets on what the simulation means for the user's domain — product strategy, design decisions, messaging, sales motion, positioning. These are inferences from the simulation results, labeled as such.

---

## Implementation constraints

These constraints are non-negotiable for any implementation of this skill:

1. **Show the work.** Every prediction is traceable to specific document content. The evidence trail is not optional.

2. **Distinguish prediction from speculation.** When the document doesn't support a confident prediction, say so. Do not fill gaps with AI intuition or general knowledge about similar teams.

3. **The document wins.** If the ensemble document says X and the AI's general knowledge suggests Y, the document wins. The skill reads the document; it does not override it.

4. **Don't fabricate member behavior.** If a member isn't documented well enough to predict, flag the gap rather than generating a plausible-sounding reaction.

5. **Grounding affects confidence.** A hypothetical ensemble produces hypothetical predictions. This must be stated explicitly in the confidence map.

6. **Respect document version.** If the ensemble document version doesn't match the current schema version, flag the discrepancy before running.

---

## Manual equivalent

If you're not using an AI skill, you can run this simulation manually:

1. Read the ensemble document with the stimulus in mind.
2. Work through each member's Roster entry and ask: given their archetype, stance, signature moves, and what modulates them, how would they react to this stimulus?
3. Build the evidence table as you go — write down what you're drawing on for each claim.
4. After per-member analysis, characterize the net collective response.
5. Be honest about where the document is thin. Mark those claims accordingly.

The skill accelerates this and enforces consistency. It's not a prerequisite for using the framework.

---

## Example

See `examples/use-cases/echo-feature-centralized-findings.md` for a worked simulation of the Echo Centralized Findings Dashboard feature tested against the Hartwell Group ensemble.

---

## Version history

| Version | Date | Notes |
|---|---|---|
| 1.0 | 2026-05-16 | Initial release |
