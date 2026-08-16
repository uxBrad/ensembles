Run a stimulus against a populated ensemble document and produce a structured prediction report.

## When to Use

- User says "simulate", "run a simulation", "test [feature/scenario] against [ensemble]", "how would [ensemble] react to [X]"
- User provides a stimulus and references an ensemble by name or path

---

## Inputs Required

Before running, confirm you have both:

1. **Ensemble doc** — a populated ensemble document (v1.0 schema). Example ensembles ship with this repo:
   - Hartwell Group: `examples/echo/hartwell-group.md`
   - Team Meridian: `examples/echo/team-meridian.md`
2. **Stimulus** — a description of what's being tested: a feature concept, a scenario, a requirement, a change, a message, a decision

If either is missing, ask for it before proceeding. Do not simulate against a sparse or hypothetical ensemble without flagging that confidence will be low.

---

## Step 1: Read the ensemble

Read the full ensemble document. Extract and hold:

- **Identity** — mood/phase, current pressures, strengths, blindspots
- **Roster** — every member: archetype, stance, authority, signature moves, verbatim anchors, what modulates them
- **Topology** — power graph, trust graph, coalition patterns, friction pairs, silence map, actual decision-making mode
- **Repertoire** — the recurring scenes (these are your behavioral reference points)
- **Stimulus-Response spec** — input types and how this ensemble metabolizes them

Note the document's grounding status (research-based or hypothetical). Hypothetical = all predictions move to medium/low confidence by default.

---

## Step 2: Classify the stimulus

Before predicting, classify what type of stimulus this is:

- Product feature concept
- Requirement or constraint
- Organizational change
- External event (regulation, lawsuit, market shift)
- A message or communication
- A process/workflow change
- Other

This determines which parts of the Stimulus-Response spec apply most directly.

---

## Step 3: Generate the report

Produce the simulation report in this exact format:

---

```
# [Stimulus name] × [Ensemble name] — Simulation Report

**Stimulus type:** [classification from Step 2]
**Tested against:** [ensemble name] (`[path to doc]`)
**Ensemble grounding:** [Research-based / Hypothetical / Partially research-grounded]

---

## Stimulus

[Full description of what's being tested — either the user's words or a clear paraphrase.]

---

## Predicted Reaction

### Overall ensemble response: [2–5 word tone label]

[2–3 sentences on how the ensemble as a whole will respond. Reference ensemble-level dynamics from Identity and Topology — not just individual reactions.]

### [Member name] ([role]) — [1–3 word stance]

[3–6 sentences. Reference their archetype, signature moves, verbatim anchors, and what modulates them. Be specific — name the tension or mechanism, not just the surface outcome. If a member's behavior is genuinely hard to predict from the doc, say so explicitly rather than guessing.]

[Repeat for each member in the Roster, in order.]

### Net response prediction

[Describe the likely collective outcome. Is this stimulus adopted, resisted, contested, ignored? Under what conditions does the outcome shift? If there are tipping points — positions, framings, or sequencing choices that change the result — name them explicitly.]

---

## Evidence Trail

| Claim | Supported by |
|---|---|
| [Each significant claim from the prediction above] | [Section and specific field/scene in the ensemble doc that supports it] |

Every significant claim in the prediction must appear in this table. If you made a claim that can't be traced to the doc, either remove it or flag it explicitly as an inference not supported by the document.

---

## Confidence Map

**High confidence** — directly supported by the document:
- [bullet per item]

**Medium confidence** — reasonable inference from documented patterns:
- [bullet per item]

**Low confidence / cannot predict** — where the document lacks sufficient information:
- [bullet per item]

If the document is sparse or hypothetical, most predictions will land in medium or low. Say so upfront rather than inflating confidence.

---

## Research Gaps

What additional research would close the low-confidence predictions:
- [bullet per gap — be specific about what type of research would help]

---

## Implications

[3–5 bullets on what this simulation means for the user's work — product strategy, design decisions, messaging, sales motion, positioning, or whatever domain they're operating in. These are inferences from the simulation, not predictions from the doc — label them as such.]
```

---

## Step 4: Offer a cross-ensemble run

After the report, ask: "Want me to run this same stimulus against [other available ensemble name]?" Cross-ensemble comparison often surfaces the most useful strategic insights.

---

## Rules

- **Show your work.** Every prediction must be traceable to specific document content. The evidence trail is not optional.
- **Distinguish prediction from speculation.** When the document doesn't support a confident prediction, say so. Don't fill gaps with intuition.
- **The document wins over your intuitions.** If the doc says X and your general intuition says Y, the doc wins. Your job is to read the doc, not to override it.
- **Don't fabricate member behavior.** If a member isn't documented well enough to predict, flag the gap rather than inventing a plausible reaction.
- **Grounding affects confidence.** A hypothetical ensemble produces hypothetical predictions. Be honest about this in the confidence map.
