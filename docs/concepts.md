# Concepts

## The core idea

People behave differently in different groups. The same product manager is assertive on one team and deferential on another. The same accessibility auditor is a respected senior on one engagement and a dismissed consultant on another. The same engineer ships fearlessly in one configuration and gets stuck in cycles of doubt in another.

This is not new information. Every UX researcher who has done team observation knows this. The problem is that traditional persona work systematically loses it. Personas abstract toward "the typical user," which strips out the contextual variation. The persona for "Senior Accessibility Auditor" treats the role as a stable type, when in practice the role's behavior depends heavily on the team configuration the auditor is operating in.

Ensembles treat that contextual variation as the primary signal, not as noise to be averaged away.

## What an ensemble is

An ensemble is a *configuration of people who interact with each other in patterned ways over time, producing collective behavior that is more than the sum of individual behaviors.*

Three things matter in that definition:

**1. Configuration.** An ensemble is not a list of people. It's a structured arrangement — who has authority, who defers to whom, who forms coalitions, who stays silent. Two teams with identical roles can be different ensembles if the configurations differ.

**2. Patterned interaction over time.** Ensembles have history. They've had conflicts and resolved them (or not). They've developed shorthand. They've learned what to expect from each other. A group of people meeting for the first time isn't an ensemble yet — it's a potential one.

**3. Emergent collective behavior.** The team produces outcomes no single member would produce alone. The team's mood is not the average of individual moods. The team's decisions are not the most common individual preference. Something happens at the group level that requires modeling at the group level.

Ensembles can be:

- **Bounded teams** — a Scrum team, a department, a working group with stable membership
- **Persistent specialist teams** — an accessibility group, a security team, a research team
- **Solo practitioners** — yes, a single person can be an "ensemble of one." See [the team-of-one section below](#teams-of-one).
- **Cross-team configurations** — the recurring set of people who participate in particular kinds of decisions, even if they're spread across formal teams

## Why model groups, not individuals

Two reasons.

First: in B2B contexts, the meaningful decision-making unit is almost never an individual. Whether your software gets adopted depends on how a team metabolizes it — who champions it, who resists it, who does the IT review, who actually clicks the buttons day-to-day. Modeling individual users tells you something about UX. Modeling the ensemble tells you about adoption.

Second: individual personas can't capture the patterns that determine outcomes. "Sarah the PM is data-driven" is true and useful, but doesn't tell you that on Team A her data arguments win, on Team B they get filtered through a senior dev's veto, and on Team C she doesn't even bother making them anymore because she's learned the team won't engage. The behavioral pattern is in the *interaction*, not in Sarah.

## Contextual instantiation

A core commitment of this framework is that the same person on different teams should be modeled as different persona instances. This is sometimes called *contextual instantiation*.

Concretely: if you're modeling Team Atlas and Team Phoenix, and the same designer (Sam) is on both teams, the framework treats "Sam-on-Atlas" and "Sam-on-Phoenix" as separate documents with potentially very different content. They share an underlying identity (they're the same human, with the same skills and history) but the behavior the framework cares about is contextual.

This has practical consequences:

- You don't write "individual personas" that get reused across ensembles. The persona work happens *inside* each ensemble document.
- You may want to maintain a registry that tracks which persona-instances refer to the same underlying person, so you can see how someone's behavior varies across configurations.
- Variation between Sam-on-Atlas and Sam-on-Phoenix is signal, not noise. It often points to something interesting about the ensembles — what's different about Atlas that makes Sam withdraw there?

## Teams of one

Solo practitioners — independent consultants, one-person teams, individual contributors operating in isolation — fit naturally into this framework as "ensembles of one."

This sounds like a degenerate case, but it isn't. A solo consultant has:

- A composition (just them, but with their full context)
- State variables (energy, recent wins/losses, current obsessions)
- A repertoire (how they handle hostile clients, how they break bad news, how they pitch new work)
- Stimulus-response patterns (how they metabolize a difficult brief, an unexpected scope change, a payment delay)

Some sections of the schema collapse for ensembles of one (topology, coalitions), and that's fine — the schema is meant to flex.

What's interesting is that *the same person* can show up in multiple ensembles: as a member of a multi-person team, as a solo consultant on a different engagement, as part of a community of practice. Each is a different persona-instance, modeled separately.

## Engagement patterns (cross-ensemble interactions)

When two ensembles interact regularly — a consulting team and a client team, a design team and an engineering team, a sales team and a customer ensemble — the interaction itself becomes worth modeling. This isn't quite an ensemble (the two groups don't merge), but it has its own dynamics: who from each side meets, what gets translated, what gets lost, what the typical outcome is.

Engagement patterns are a sibling artifact to ensembles. They use a related but different schema. They're particularly relevant for B2B SaaS contexts where your software mediates between two ensembles (a vendor team and a client team, an internal services group and a product team).

The framework includes engagement patterns as a planned artifact type, but the current focus is on getting ensembles right first. Engagement pattern documentation is forthcoming.

## What this framework is good for

- Modeling B2B customers where teams (not individuals) decide on adoption
- Predicting how organizational changes will affect different parts of an org
- Designing software whose value depends on team dynamics, not just individual workflow
- Surfacing where research is thin and additional fieldwork would help
- Generating distinct value propositions for different customer segments
- Stress-testing feature concepts before committing to them

## What this framework is not good for

- Modeling B2C contexts where individual user behavior dominates
- Replacing real research — the framework is a way to *encode* research, not generate it
- Quick answers — populating a useful ensemble doc takes time and judgment
- Universal personas — each ensemble is its own thing; there's no "average team"
- Predicting things the underlying research doesn't support — see the methodology doc on epistemic honesty

## A note on epistemic discipline

It's tempting to fill in ensemble docs with plausible-sounding details from imagination. AI-assisted population makes this even easier. The framework's whole claim — that documents can predict behavior under stimuli — collapses if the documents are partially fictional.

The discipline this framework asks of you:

- Every claim in an ensemble doc should trace back to a research source (interview, observation, ticket, artifact).
- Where research is thin, the field stays empty or marked low-confidence — not filled in with extrapolation.
- Simulation outputs should cite which fields supported each prediction. Predictions that can't be traced back to specific evidence in the doc should be flagged.

This is harder than it sounds and it's the difference between a useful framework and elaborate fiction.
