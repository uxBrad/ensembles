# Use Cases

Worked examples of running stimuli against ensemble documents to predict reactions.

Each use case demonstrates:

- A specific stimulus (feature concept, requirement, scenario)
- Predictions for one or more ensembles
- Evidence trails connecting predictions to ensemble document content
- Confidence assessments and identified gaps

These examples show what good simulation output looks like. They serve as a reference for what to expect when the simulation skill is built, and as a guide for doing simulation manually in the meantime.

## Available use cases

### `echo-feature-centralized-findings.md`
Tests how Echo's proposed "centralized findings dashboard" feature would land with the Hartwell Group. Demonstrates evidence trails, confidence assessments, and how a single feature concept produces different implications for different members of the same ensemble.

## How to read a use case

1. Start with the **stimulus description** at the top — what's being tested
2. Read the **predicted reaction** for each ensemble
3. Notice the **evidence trail** — every claim cites which fields in the ensemble doc support it
4. Pay attention to the **confidence map** — what's well-supported, what's extrapolating, what can't be predicted
5. Note the **research gaps** — where additional research would close uncertainty

## Format conventions

Use cases follow this structure:

```
# Use Case: [Stimulus name]

## Stimulus
[Description of what's being tested]

## Predictions

### [Ensemble name]
[Predicted reaction with inline evidence trail]

**Evidence trail:**
- Claim 1 ← supported by [field reference]
- ...

**Confidence map:**
- High: ...
- Medium: ...
- Low / cannot predict: ...

**Research gaps:**
- ...
```

This format is designed to be both human-readable and parseable — the simulation skill will produce output in this shape.
