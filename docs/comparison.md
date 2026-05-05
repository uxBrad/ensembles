# How This Differs From Existing Persona Approaches

## Traditional personas

Traditional UX personas describe individual users with attributes like demographics, goals, pain points, and behaviors. They're typically a one-page or poster-format document, scannable, designed to fit in a stakeholder's mental model.

**Strengths:**
- Easy to share and reference
- Build empathy with users
- Anchor product decisions in something concrete
- Long history of use, well-understood by teams

**Limitations:**
- Static — they don't change once written
- Individual-focused — they miss group-level dynamics
- Get used in kickoff meetings then forgotten
- Often drift from reality without anyone noticing
- Don't predict behavior under specific stimuli

Ensemble personas address all of these limitations, but at meaningful cost: they're more expensive to create, harder to read at a glance, and require ongoing maintenance.

**When to use traditional personas:** B2C products, individual-user contexts, situations where the "team using this" question doesn't apply.

**When to use ensemble personas:** B2B contexts, situations where teams (not individuals) decide on adoption, products where group dynamics determine outcomes.

These approaches can complement each other. Traditional personas might describe the individual user's perspective; ensemble personas describe the team context that user operates in.

## Boag's virtual personas

Paul Boag's [Smashing Magazine article](https://www.smashingmagazine.com/2025/12/giving-users-voice-virtual-personas/) proposes "virtual personas" — making research repositories queryable through AI by giving stakeholders a way to consult personas as part of decision-making conversations. The framework includes multi-persona consultation, function-specific lenses, and protocols for when AI should defer to additional research.

**What Boag's framework solves:**

A *research distribution* problem. Research gets done, sits in a shared drive, and the people making decisions never see it. Boag's solution: make research conversational. A marketing manager can ask "what would users think of this campaign?" and get synthesized perspectives drawn from existing research artifacts.

**What ensemble personas solve:**

A *behavioral prediction* problem. Specifically: when groups encounter changes (new features, requirements, organizational shifts), how do they metabolize them? Outcomes vary substantially across groups in ways that single-user persona work doesn't capture.

**Where the frameworks differ:**

| Dimension | Boag's virtual personas | Ensemble personas |
|---|---|---|
| Unit of analysis | Individual user | Group configuration |
| Primary use | Stakeholder consultation | Behavioral simulation |
| AI role | Retrieval and synthesis | Simulation execution |
| Output | Multi-perspective feedback | Predicted group response with evidence trail |
| Persona format | Functional persona, made longer for AI | Structured ensemble doc with topology and repertoire |
| Ground truth | Research repository | Research repository, but encoded into structured docs |
| Validation | Stakeholder finds output useful | Predictions match observed reality |

**Where they could complement each other:**

A complete UX research stack might include both:

- Traditional personas for surface communication
- Boag-style virtual personas for stakeholder querying
- Ensemble personas for predicting group-level reactions to specific changes

Each is solving a different problem. None replaces another.

**A note on lineage:**

Ensemble personas were directly sparked by Boag's article. The conceptual move from "personas as static documents" to "personas as AI-consultable resources" came from him. Ensemble personas extend the move further — from consultation to simulation, from individual to group, from descriptive to predictive. Credit where it's due.

## Agent-based modeling

Outside UX, *agent-based modeling* (ABM) has been used in social science for decades to simulate group behavior. ABM defines individual agents with rules, places them in environments, and observes emergent behavior.

Ensemble personas borrow the *spirit* of ABM but operate at a different level of fidelity. ABM is rigorous, computational, and typically used for academic research. Ensemble personas are documentation-based, AI-consulted, and used for product decisions. They're roughly to ABM what UX personas are to demographic surveys: lower fidelity, more usable, designed for practical decision-making rather than academic publication.

If you want true behavioral simulation, ABM is the heavier-weight approach. Ensemble personas are calibrated to be useful at the cost of being less rigorous.

## Service blueprints

Service blueprints describe how multiple actors (customers, frontstage employees, backstage employees, systems) interact across a service experience. They share with ensemble personas a focus on *configurations* rather than individuals.

The difference is that service blueprints are *normative* (describing how a service should work) and ensemble personas are *descriptive* (capturing how a real ensemble actually works). A service blueprint might say "the receptionist greets the customer." An ensemble persona would describe a specific receptionist who often forgets to greet, a specific customer base that varies in expectations, and the resulting interaction patterns.

You'd use service blueprints to design or improve a service. You'd use ensemble personas to predict how a service team will react when the service design changes.

## Why have a new framework at all?

A reasonable question. The honest answer:

The existing frameworks each solve a real problem, and ensemble personas are designed for a problem they don't address well: *predicting how specific groups will react to specific changes, in B2B contexts where group dynamics determine outcomes*. If you're not solving that problem, you may not need this framework.

If you're building software for teams (rather than individuals), trying to predict adoption across different customer segments, or designing organizational changes — ensemble personas may give you something the existing tools don't.
