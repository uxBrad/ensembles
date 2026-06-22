# Synthesis Skill Specification

**Status:** Design phase. Specification documented, implementation not yet built.

This document specifies an AI skill that assists researchers in synthesizing raw research data into populated ensemble persona documents. The skill is designed to help with the mechanical parts of synthesis (evidence tracking, gap identification, contradiction surfacing) while leaving the judgment work to the researcher.

This is the highest-risk skill in the framework. Synthesis is inherently inferential work, and the temptation to fabricate plausible content is enormous. The skill described here is intentionally conservative. It will produce documents with explicit gaps rather than documents that look complete. This trade-off is deliberate and important.

## Purpose

The skill takes raw research data (interview transcripts, observation notes, support tickets, other artifacts) and produces a populated ensemble document, with per-field evidence trails, explicit gaps, and surfaced contradictions.

Critically, the skill does not "complete" the document. It produces whatever the evidence supports and stops there. The researcher decides whether to gather more evidence or accept the gaps.

## What the skill does

The skill operates in four phases. Each phase has specific outputs and explicit constraints.

### Phase 1: Read and segment

**Input:** Raw research data (one or more documents) and the ensemble schema template.

**Process:** Read through each piece of research data. For each section of the schema (Identity, Roster, Topology, Repertoire, Stimulus-Response), identify which parts of the research are relevant.

The skill does not yet produce claims at this stage. It just maps research content to schema sections.

**Output:** A structured map showing, for each schema field, which research artifacts contain relevant content. References are by document and approximate location (e.g., "INT-03, around the question about decision-making").

### Phase 2: Extract evidence

**Input:** The segmentation map from Phase 1.

**Process:** For each schema field, extract the specific evidence from research artifacts. This is direct extraction, not inference. Quote where appropriate. Note participant attributions.

The skill does not yet make claims about the team at this stage. It just gathers the evidence that could support claims.

**Output:** For each schema field, a structured list of evidence items with attributions. Some fields will have many evidence items; some will have few or none.

### Phase 3: Synthesize with epistemic discipline

**Input:** The evidence collection from Phase 2.

**Process:** For each schema field, evaluate what claims the evidence supports. Apply the following discipline:

- **Strong evidence (multiple sources, consistent):** Make the claim directly, with evidence trail.
- **Moderate evidence (single source or partial):** Make the claim, marked as `[inferred]` with note about what supports the inference.
- **Weak evidence (suggestive but thin):** Make a hedged claim, marked as `[low confidence]`, or note as gap.
- **No evidence:** Leave the field empty, marked as `[insufficient research]`.

The skill must not produce claims that don't have evidence behind them. This is the constraint that prevents fabrication.

The skill also surfaces contradictions. When two pieces of evidence support different claims for the same field, the skill does not pick one. It notes the contradiction and presents both perspectives.

**Output:** A populated ensemble document with per-field evidence trails, confidence markers, surfaced contradictions, and explicit gaps.

### Phase 4: Generate gap report and follow-up suggestions

**Input:** The populated document from Phase 3.

**Process:** Identify the gaps and assess their importance. For each significant gap, propose specific follow-up actions:

- What question would close this gap?
- Who could the researcher ask?
- Is there an existing artifact (a ticket, a document, a record) that might contain the answer?
- Could a brief follow-up email to a previous interviewee close it?

The skill prioritizes gaps by likely impact on the document's usefulness, not by completeness for its own sake.

**Output:** A structured gap report with prioritized follow-up suggestions.

## What the skill does not do

This is as important as what it does. The skill's design depends on these constraints.

**The skill does not identify ensembles from raw research.** That clustering work is judgment-heavy and requires a trained researcher. If the input research doesn't yet have ensembles identified, the skill cannot operate. It assumes the researcher has already decided which ensemble they're populating.

**The skill does not extrapolate beyond evidence.** If the research doesn't support a claim, the skill does not invent one. This is the core epistemic constraint.

**The skill does not smooth over contradictions.** When evidence conflicts, the conflict gets surfaced. The skill does not average, pick one, or hide the disagreement.

**The skill does not assess truth.** When research participants disagree about a fact, the skill notes the disagreement. It does not adjudicate which participant is right. That's the researcher's call, often informed by additional research.

**The skill does not produce final documents.** The output is a draft that requires researcher review. The skill is an assistant, not an author.

## Critical design constraints

A few constraints that shape how the skill must be implemented.

### The skill is structured around evidence, not output

The skill's prompts and processing logic should be organized around evidence first. The flow should be: "What evidence do you have? What does that evidence support? What claims follow?" Not: "What's the right answer for this field? What evidence can we find to support it?"

This sounds like a small distinction but it's the difference between honest synthesis and motivated reasoning. The order of operations matters.

### Empty fields are correct outputs

If a schema field has no supporting evidence, leaving it empty is the correct output, not a failure mode. The skill should treat empty fields as normal and not try to populate them creatively.

### Inference is allowed but must be marked

The skill can make inferences across multiple pieces of evidence. But inferred claims must be marked as inferences, with a note about what supports the inference.

This allows the skill to do real synthesis work (inference is valuable; pure extraction would be too limited) while preserving honesty about the basis for each claim.

### Confidence is a first-class output

The skill produces three confidence levels: directly evidenced, inferred, low confidence. These appear in the output document itself, not buried in metadata.

Researchers and stakeholders should be able to read the document and immediately see what's well-grounded and what isn't. The framework's whole claim of epistemic honesty depends on this.

### The skill respects the framework's methodology

The skill operationalizes the principles in `docs/research-methodology.md`. It should not invent new synthesis principles or override the ones in the methodology document. If the methodology document is updated, the skill's behavior should be updated accordingly.

## Implementation approach

The skill is most naturally implemented as a structured prompt or chain for an AI model with access to the research data. It does not require custom code, though custom tooling could accelerate the work.

A reasonable implementation path:

1. **Prototype as a prompt.** Build the skill as a carefully constructed prompt that walks through the four phases. Test against known cases.

2. **Add structure as needed.** If the prompt produces inconsistent results, add structure (separate prompts per phase, intermediate state, etc.).

3. **Build tooling around the prompt.** Once the prompt works, build supporting tooling: a way to feed research data in cleanly, a way to format output consistently, a way to track which research artifacts have been processed.

4. **Test against ground truth.** Use research where you already know what the right ensemble looks like. See whether the skill produces that ensemble or something different. Fabrication shows up here; if it does, the implementation needs work.

The conservative bias of the skill should be obvious in testing. The skill should produce documents with more gaps than feel comfortable. That's the design working as intended, not a bug.

## How researchers should use the skill

When the skill exists, researchers should treat it as an assistant for the mechanical parts of synthesis, not as a replacement for synthesis judgment.

A reasonable workflow:

1. Researcher gathers research data and decides which ensemble they're populating.
2. Researcher runs the skill against the research data.
3. Skill produces a draft ensemble document with evidence trails, confidence markers, and gaps.
4. Researcher reviews the draft. Critically evaluates each claim. Disagrees with the skill where their judgment differs.
5. Researcher reviews the gap report. Decides which gaps to close with additional research and which to accept.
6. Researcher writes the final document, using the draft as scaffolding but exercising judgment throughout.

The researcher's review is not optional. The skill produces a defensible draft, but the researcher's judgment is what makes the document actually right.

## Failure modes to watch for

When the skill exists and gets used in production, watch for:

**Over-trust.** Researchers treating the skill's output as authoritative without critical review. The mitigation is education: the skill's documentation should emphasize that review is required, and the framework's methodology document should reinforce this.

**Pressure to reduce gaps.** Stakeholders or researchers wanting to "complete" the document by reducing gaps. The mitigation is to be honest about what gaps mean: they're research prompts, not quality problems.

**Domain mismatch.** The skill being applied in domains where the framework's schema is a poor fit. The mitigation is the methodology document's guidance on when ensemble personas are appropriate.

**Gradual prompt drift.** Over time, the skill's prompts being adjusted to produce "better looking" output, which often means more confident and less honest. The mitigation is version control on the prompts and explicit testing against known cases.

## Future enhancements

Some features that could be added once the basic skill works:

**Cross-ensemble comparison.** When the researcher has multiple ensembles, the skill could compare them and surface differences. "Diane on the Hartwell team and Sarah on the Phoenix team have similar archetypes but different stances. The difference is..."

**Refresh detection.** When new research is added to an existing ensemble, the skill could identify which claims in the existing document are now supported, contradicted, or unaddressed by the new research.

**Question generation.** Given a populated ensemble and a stimulus, the skill could generate follow-up questions to ask the team about how they'd actually react. This bridges from population to simulation.

These are not part of the initial design. They're noted here as plausible directions for future work, not as commitments.

## Relationship to other framework components

The skill connects several existing components:

- It operationalizes the **synthesis principles** in `docs/research-methodology.md`
- It populates documents that conform to the **schema** in `docs/schema.md`
- Its output is reviewed by researchers using the **template** in `templates/ensemble-template.md`
- Its limitations align with the **comparison** with other approaches in `docs/comparison.md`

The skill does not stand alone. It's part of a methodology that includes the script, the synthesis guide, the schema, and the researcher's judgment.

## A final note on conservatism

The skill described here is more conservative than feels comfortable. It will produce documents that look less complete than researchers may want. It will refuse to fill in gaps that seem fillable. It will surface contradictions rather than resolving them.

This conservatism is the design working correctly.

The framework's claim is that ensemble personas can predict team behavior because they're grounded in real research. If the synthesis step produces confident-looking documents from thin research, the framework's grounding claim becomes a marketing claim rather than a real property. The skill's conservatism is what protects the framework's integrity.

When you build the implementation, hold this conservatism as a non-negotiable constraint. Better to ship a skill that produces gaps honestly than one that produces complete documents dishonestly.
