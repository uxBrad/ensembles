# Schema v1.0

This document defines the structure of an ensemble. It is the authoritative reference. The template ([../templates/ensemble-template.md](../templates/ensemble-template.md)) implements this schema; examples ([../examples/](../examples/)) are populated instances of it.

## Document conventions

Every ensemble document begins with metadata:

- **Document Type:** Ensemble (Deep) v1.0
- **Grounding:** Statement of research basis (or "Hypothetical" for examples)
- **Last Updated:** Date

Followed by a lightweight version (see below) and then the five main sections.

## Lightweight version

A 2-3 sentence prose paragraph that captures the team's character. Not a structured summary — a *paragraph*. Should give a reader who doesn't have time for the full doc a usable mental model in 30 seconds.

Bad: "A four-person team that does accessibility audits."
Good: "The Hartwell Group is a four-person centralized accessibility team inside a mid-sized financial services company, where they serve as internal consultants to ~30 product teams. They're respected, chronically over-capacity, and quietly cynical about how much of their work actually changes shipped products — but the team holds together because they genuinely like each other and share a sense that the work matters."

## Section 1 — Ensemble Identity

The ensemble's basic context, current state, and meta-properties. This section is metadata-shaped — short fields, factual where possible.

**Required fields:**

- **ID** — A unique identifier (e.g., `ENS-HARTWELL`)
- **Stability** — How long has this configuration existed? Any recent membership changes?
- **Origin context** — How and why this ensemble formed
- **Composition shape** — Whether the ensemble is role-complete, role-redundant, has gaps, etc.

**Current state (sub-section):**

- **Mood / phase** — What state is the team in *right now*? (Crisis, fatigue, momentum, post-incident, etc.)
- **Trust temperature** — Internal trust dynamics, current state
- **Recent history** — Last 1-3 events that still shape behavior
- **External pressure** — What the group is collectively reacting to

**Strengths and Blindspots (sub-section):**

- **Strengths** — What this ensemble does well, often as a function of its specific configuration
- **Blindspots** — What this ensemble systematically misses or under-weights

Strengths and Blindspots are not optional. They are where the doc becomes useful for product decisions — they make the doc *generative*, not just descriptive.

## Section 2 — The Roster

For each member of the ensemble, a sub-block with the following fields:

- **Member ID** — Unique within the ensemble (e.g., `M-01`)
- **Cross-ensemble link** — If this person also appears in another ensemble doc, mark it (e.g., `↔ SAM-PHOENIX`)
- **Role-hat** — Their role(s) and any hat-combinations (e.g., "UX + Frontend")
- **Archetype-in-context** — How they show up *in this ensemble specifically*. Not their general personality.
- **Stance** — How they occupy this room. Engaged, withdrawn, performative, defensive, etc.
- **Authority** — Formal authority vs. earned authority, on what topics
- **Signature moves** — 3-5 things they reliably do
- **Verbatim anchors** — 1-2 quotes from research, where possible
- **What modulates them** — What conditions make them more or less of how they typically are *within this ensemble*

The "What modulates them" field is load-bearing. It's what makes the doc capture contextual instantiation rather than static traits.

## Section 3 — Topology

The connective tissue between members. How influence actually flows.

- **Power graph** — Who defers to whom, on what topics
- **Trust graph** — Who takes whom seriously, who they discount
- **Coalition patterns** — Predictable alliances, including tactical ones
- **Friction pairs** — Who reliably clashes, on what
- **Silence map** — Who doesn't speak up, when, why
- **Decision-making mode** — How convergence actually happens, distinguishing stated from actual

Topology is what makes the doc capture group-level dynamics rather than just a list of individuals.

## Section 4 — Repertoire

Recurring scenes that this ensemble plays out. Each scene is a *behavioral template*, not a script.

For each scene (typically 3-6):

- **Trigger** — What initiates the pattern
- **Sequence** — Who does what, in what order
- **Outcome** — Predictable result
- **Variation** — What conditions change the outcome

Scenes are the most directly research-grounded section — you've probably literally observed them. They're also the most useful for simulation, because they give the AI concrete behavioral templates to draw on.

## Section 5 — Stimulus-Response Spec

How the ensemble metabolizes inputs. This is the section that makes the doc *operational* rather than just descriptive.

**Sub-section: Input types this ensemble receives**

A list of the kinds of inputs that arrive (requirements, escalations, incidents, etc.) — typically 4-6 types.

**For each significant input type:**

- **First-touch** — Who sees it first, what they do
- **Pre-meeting layer** — What happens in DMs and informal channels before the input becomes a group conversation
- **Surfacing pattern** — When and how the input becomes a group topic
- **Objection map** — Who raises which type of objection, predictably
- **Translation layer** — What the input said vs. what the team heard
- **Output format** — What the ensemble produces in response

The translation layer is often where the most actionable insight lives. It's the gap between what the input meant and what got received, and that gap is where adoption succeeds or fails.

## Optional: Tooling Posture

For ensembles that are customers for software products, an additional sub-section in Section 1 is recommended:

- **Existing tools** — What they currently use
- **History with new tools** — Past adoption patterns, exhaustion levels, skepticisms
- **Champions and gatekeepers** — Who advocates for new tools, who blocks them
- **Adoption posture** — Eager / cautious / skeptical / hostile to new tools, and why

This isn't part of the core schema (it's domain-specific), but it's useful enough for software-customer modeling that it deserves recognition.

## What's *not* in the schema

A few deliberate omissions:

- **Demographics** — Age, gender, location, etc. The framework treats demographics as either irrelevant (most cases) or worth noting as context within the relevant fields, not as their own structured data.
- **Pain points / goals** in traditional persona format — These collapse into Strengths/Blindspots, Signature Moves, and Stimulus-Response, where they're more actionable.
- **A "primary goal" or "key motivation" field** — Goals are plural and contextual. The doc captures them where they manifest (in moves, in objections, in repertoire) rather than reducing them to a single statement.
- **A "scenarios" section** — Scenarios are inputs you run *against* the doc, not parts of the doc itself. They live in the use-cases folder.

## Versioning

The schema is at v1.0 (locked). Future changes will follow semantic versioning:

- **Patch (v1.0.x):** Clarifications, examples, wording fixes
- **Minor (v1.x.0):** Additive changes — new optional fields, new sub-sections
- **Major (v2.0.0):** Breaking changes that require existing docs to be updated

Documents should declare which schema version they conform to in their header.
