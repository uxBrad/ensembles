# Skills

This folder will contain AI skills designed to operate on ensemble persona documents. Skills are platform-agnostic markdown files describing structured workflows that can be implemented as Claude skills, Cursor rules, GPT custom instructions, or any equivalent.

**Status:** In design. Implementations forthcoming.

## Planned skills

### Population skill (coming soon)

**Purpose:** Help a UX researcher populate an ensemble document from research artifacts through a structured interview-style workflow.

**How it will work:**

The researcher provides:
- A blank or partially-filled ensemble template
- Access to (or copies of) relevant research artifacts — interview transcripts, observation notes, support tickets, analytics, etc.
- The name and basic context of the ensemble being modeled

The skill then:
1. Reads through the research artifacts looking for evidence relevant to each field in the template
2. Populates fields where evidence is direct and traceable, citing the source per field
3. Marks fields as `[inferred]` where the conclusion is reasonable but indirect
4. Marks fields as `[insufficient research]` where there isn't supporting evidence
5. Produces an explicit gap report: which sections are sparse, what kinds of research would close the gaps, suggested interview questions

**Why this is valuable:**

The bookkeeping work of going through research, finding evidence, populating the right fields, and tracking what's missing is mechanical and tedious. AI does this well. The *interpretation* of what evidence means and *whether the inference is justified* stays with the researcher — they review the populated document before committing to it.

**Critical design constraints:**

- The skill must never silently fabricate. Every populated field cites evidence; missing evidence produces an explicit gap, not a plausible-sounding fill.
- The skill defers to the researcher on ambiguous cases. When evidence could support multiple interpretations, the skill surfaces the ambiguity rather than picking one.
- The skill respects the methodology — it doesn't try to do ensemble identification (which requires UX judgment), only population of an already-identified ensemble.

### Simulation skill (coming soon)

**Purpose:** Run a stimulus (feature concept, requirement, scenario) against a populated ensemble document and produce a transparent prediction of how the ensemble will react.

**How it will work:**

The user provides:
- A populated ensemble document
- A stimulus to test — typically a feature description, a requirements doc, a scenario description, or a change description

The skill then produces:

1. **A prediction.** What this ensemble is likely to do with this input. Specific to the ensemble — references named members, named scenes, specific topology features.

2. **An evidence trail.** For each significant claim in the prediction, a citation back to which fields in the ensemble document support it.

3. **A confidence map.** Three layers:
   - *High confidence:* directly supported by the document
   - *Medium confidence:* reasonable inference from documented patterns
   - *Low confidence / cannot predict:* where the document doesn't have enough information

4. **Suggested research.** Where the prediction is low-confidence, what additional research would close the gap.

**Why this is valuable:**

This is the operational payoff of the entire framework. The reason to build ensemble documents is so you can ask "how will Team X react to Y?" and get a useful, evidence-grounded answer. The simulation skill is what turns the document from a description into a tool.

**Critical design constraints:**

- The skill must show its work. Every prediction is traceable to specific document content.
- The skill must distinguish prediction from speculation. It is honest when the document doesn't support a confident answer.
- The skill respects the document's grounding. If the document is sparse, the prediction is appropriately hedged.
- The skill doesn't substitute its own intuitions for the document's content. If the document says X and the AI's general intuition says Y, the document wins.

## Why skills are described here before being built

Two reasons:

1. **The skill design is part of the framework's design.** Building good skills requires the schema and methodology to be settled first. By documenting what the skills *will* do, the framework's intended use becomes clearer, which feeds back into schema and template design.

2. **Skills are platform-specific in implementation but platform-agnostic in concept.** What goes in this folder is the conceptual specification. The actual implementations (Claude skill folders, Cursor rules, system prompts) may live elsewhere or be developed iteratively as the framework matures.

## Manual workflows in the meantime

While these skills are in development, both jobs can be done manually:

- **Manual population:** Read through your research artifacts, fill in the template, cite evidence per field, leave gaps explicit. Slower but produces equivalent output if done with discipline.
- **Manual simulation:** Read through a populated ensemble document with a stimulus in mind. Reason through how the team would react, citing which sections support each claim. Note where the document doesn't have enough information.

Both are tractable for a researcher who knows the framework. The skills will accelerate them and enforce consistency, but they're not prerequisites for using the framework.
