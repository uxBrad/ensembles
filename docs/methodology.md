# Methodology

How to use this framework: identifying ensembles from your research, populating documents, and maintaining epistemic honesty.

## Step 1: Identifying ensembles from research

This step is the core UX research work, and it doesn't delegate well to AI. Looking at a body of research and recognizing what ensembles exist requires holding ambiguous evidence in mind, noticing patterns that don't map to surface features, judging which differences are meaningful, and tolerating uncertainty about boundaries. It's affinity mapping, applied to group dynamics rather than to user needs.

**What you're looking for:**

- *Configurations that recur* across multiple research artifacts. If three different research participants describe a similar team shape, you may have an ensemble type.
- *Behavioral patterns that distinguish one configuration from another.* "All accessibility teams" is too broad. "Mature centralized accessibility teams that report through Design Ops" might be a real ensemble type.
- *Variation that surprises you.* If the same role behaves very differently in two contexts, that's evidence of contextual instantiation — and the contexts may be distinct ensembles worth modeling separately.

**What you're NOT looking for:**

- Demographic or organizational clustering as ends in themselves. Company size, industry, or org-chart shape are *features* of ensembles, not the basis for ensemble identity.
- Smooth, equal-sized clusters. Real ensemble distributions are messy. You may have one common type and several rare variants. Forcing neat clusters is a known failure mode.

**Practical approach:**

1. Pull together your research artifacts (interviews, observations, tickets, analytics, support data).
2. Affinity-map *team configurations* you observe — group by composition, dynamics, decision patterns, recurring scenes.
3. For each cluster, ask: is this distinct enough to model as its own ensemble, or is it a variant of another?
4. Name your ensembles. Specific names (Hartwell, Meridian) are better than generic ones (Team A, Team B).
5. Document why each ensemble is distinct from the others — this is your basis for treating them as separate.

You should expect to identify 2-5 ensemble types from a typical research repository, with the distribution skewed (one common type, several rarer ones). If you find 10+, you're probably over-fitting. If you find only 1, you may be under-fitting.

## Step 2: Populating an ensemble document

Once you've identified an ensemble, copy the template ([../templates/ensemble-template.md](../templates/ensemble-template.md)) and start filling it in.

**Order of filling:**

The template is organized for reading; the natural order for *filling* it is different. We suggest:

1. **Lightweight version first.** Write the 2-3 sentence prose paragraph. This forces you to articulate the ensemble's character before getting into details. If you can't write this paragraph, you don't yet understand the ensemble well enough.
2. **Roster (Section 2).** Identify the members, give them IDs, write each sub-block. The Roster is concrete and grounded in specific people from your research.
3. **Repertoire (Section 4).** Recurring scenes are the most directly research-derived section. You've probably observed them. Document 3-6 of them.
4. **Topology (Section 3).** Now that you have members and scenes, the relationships between them are easier to articulate.
5. **Stimulus-Response (Section 5).** This synthesizes the rest. What inputs does the team receive, and how do roster + topology + repertoire combine to metabolize each?
6. **Identity (Section 1).** Counter-intuitively, this comes last. Once you've written the rest, the identity-level summary writes itself: who they are, what state they're in, what they're good and bad at.

**Per-field discipline:**

For every field, ask yourself: *what evidence supports this?* Concretely, can you cite an interview, an observation, a ticket, a quote? If yes, fill in the field with a brief evidence note (e.g., "[from interviews INT-03, INT-07]"). If no, leave the field empty or marked `[insufficient research]`.

The temptation will be to fill empty fields with plausible-sounding content. Resist this. An empty field is a research prompt; a fabricated field is fiction that contaminates everything downstream.

## Step 3: Identifying gaps

When you've filled in everything you have evidence for, scan the document for empty or weakly-supported fields. These are your research gaps.

For each gap, ask:

- *Is this gap material?* Some fields can stay empty without affecting the doc's usefulness. Others are load-bearing.
- *What research would close it?* A specific interview question? An observation session? A review of ticket history?
- *Is it worth closing?* Cost-benefit varies by field and use case.

Track gaps explicitly. They're a research backlog, not a quality problem.

## Step 4: Running stimuli against the document

Once an ensemble document is populated to the point where you'd trust it, you can use it to predict reactions to inputs. This is the *simulation* step.

A well-designed simulation should produce:

1. **A prediction.** What this ensemble will likely do with this input.
2. **An evidence trail.** Which fields in the document support which parts of the prediction.
3. **A confidence map.** Where the prediction is well-grounded, where it's extrapolating, where the document is insufficient.

The simulation skill (forthcoming — see [../skills/simulation.md](../skills/simulation.md)) is designed to produce all three. You can also run simulations manually by reading through the document with a stimulus in mind and reasoning through how the team would respond.

## Step 5: Updating documents over time

Ensemble documents are not write-once artifacts. Teams change. Research deepens. Predictions get tested against reality.

Plan for periodic refresh:

- **Trigger-based refresh:** Major team changes (key member leaves, new member joins, restructure) should trigger an update.
- **Time-based refresh:** Even without specific triggers, documents should be reviewed annually. Teams drift.
- **Prediction-based refresh:** When a simulation predicts something and reality contradicts it, that's a signal. Either the document is stale, or the prediction logic is flawed. Investigate.

Each document should declare its version and last-updated date. Maintain a brief changelog at the bottom of the document for major revisions.

## Maintaining epistemic honesty

The framework's value depends entirely on documents being grounded in research. A few practices that protect against drift:

**Cite your evidence.** Light citations per field are sufficient — interview IDs, observation dates, ticket numbers. The point isn't bibliographic rigor; it's traceability.

**Mark inferences as inferences.** Some claims are reasonable inferences from research, not direct evidence. Mark these explicitly (e.g., `[inferred]`). They're useful, but they're not the same as evidence-backed claims.

**Don't fill empty fields under pressure.** If a stakeholder asks for a "complete" document and you're missing data, the right answer is "this section is sparse because our research doesn't support it; here's what we'd need to fill it in" — not fabrication.

**Check simulations against reality.** When you run a simulation that predicts a specific reaction, and you have a chance to observe the actual reaction, *observe*. Compare. Update the document if it was wrong. This is the empirical loop that distinguishes the framework from elaborate fiction.

**Be honest about scope.** This framework predicts behavior to the extent that the documents are well-grounded. It does not predict things that are out of scope of the underlying research. A doc grounded in 2024 research can't reliably predict reactions to 2026 organizational changes.

## A note on AI assistance

AI can help with several parts of this methodology:

- **Document population** (forthcoming skill): structured interview-style population from research artifacts, with explicit gap-flagging
- **Simulation** (forthcoming skill): running stimuli against populated documents with transparent evidence trails
- **Consistency checks**: comparing claims across sections, flagging contradictions
- **Cross-ensemble comparison**: surfacing where the same person appears in multiple ensembles and noting differences

AI is *not* good at:

- The core ensemble identification work (clustering from research)
- Judging when an inference is justified vs. fabrication
- Knowing when to stop adding fields and accept gaps
- Recognizing when the framework is the wrong tool for a question

Treat AI as an executor, not an analyst. Your judgment stays in the loop.
