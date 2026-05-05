# Examples

This folder contains worked examples of the ensemble framework applied to real (or realistic) cases. Examples serve two purposes:

1. **Concrete reference** — show what a populated document looks like
2. **Calibration** — let users compare their output to known-good examples

## Echo

`echo/` contains ensemble documents related to Echo, an accessibility audit software product in development. These are the framework's primary worked examples.

Echo is a hypothetical product used here as a context for demonstrating the framework. The ensembles model realistic customer and stakeholder configurations Echo would encounter:

- **`hartwell-group.md`** — A specialist accessibility team (potential Echo customer)
- **`team-meridian.md`** — A receiving product team (where Echo's outputs land)

Solo consultant and other ensemble variants are planned but not yet documented.

The Echo ensembles are *hypothetical* — they're built to illustrate the framework rather than from primary research. In real practice, ensembles should be grounded in research. The methodology document explains how.

## Use cases

`use-cases/` contains worked examples of running stimuli against ensemble documents. Each use case demonstrates:

- A specific stimulus (feature concept, requirement, scenario)
- Predictions for one or more ensembles
- Evidence trails connecting predictions back to ensemble document content
- Confidence assessments and identified gaps

These are meant to demonstrate what good simulation output looks like, before the simulation skill is built.

## How to read these examples

If you're new to the framework:

1. Read the lightweight version at the top of an ensemble doc to get the sense of the team
2. Skim the schema sections to see how each is filled in
3. Read a use case to see what simulation output looks like
4. Compare to the schema and methodology docs to understand the conventions

If you're using the framework:

1. Use the examples as calibration — does your filled-in template have similar density, specificity, and evidence-grounding?
2. Notice the trade-offs in level of detail — some sections are brief, some are dense, depending on what the ensemble's behavior actually requires
3. Pay attention to the gaps and ambiguities — even these examples have them, and they're a feature not a bug
