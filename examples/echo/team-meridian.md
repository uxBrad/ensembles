# Ensemble: Team Meridian

**Document Type:** Ensemble (Deep) v1.0
**Grounding:** Hypothetical — illustrative example for schema validation, not research-grounded
**Last Updated:** 2026-05-05

---

## Lightweight Version

Team Meridian is a six-person Scrum team owning customer onboarding and account management at a mid-sized SaaS company. They've been together about 14 months and ship reliably, but they argue themselves into smaller scope than they could handle — partly because the BO has built a strong protective layer between the team and the PM, and partly because the senior dev's technical-veto power goes mostly unchallenged. The team is competent and trusts itself internally, but it under-utilizes its UX designer, treats its newest QA as still-on-probation, and has no good way to surface the disagreements that everyone privately knows are there.

---

## Section 1 — Ensemble Identity

- **ID:** ENS-MERIDIAN
- **Stability:** Persistent Scrum team, ~14 months together. One recent member change (QA replaced 4 months ago).
- **Origin context:** Formed when a monolithic platform team was split into feature-area squads. Meridian owns the customer onboarding and account-management surface area.
- **Composition shape:** Role-complete for delivery (PM-BO-Dev-UX-QA covers the full cycle) but role-thin for scale — no dedicated researcher, no accessibility specialist, no data analyst. They borrow these from a shared services pool, which matters because *those borrowed roles never become full ensemble members*.

**Current state:**

- *Mood / phase:* Mildly fatigued. Just shipped a major release 6 weeks ago, didn't get the recovery sprint they wanted, and are now in a quarter where Priya (PM) is under exec pressure to ship a second major thing. Team feels squeezed.
- *Trust temperature:* High internally between Marcus (BO), Dev Lead, Sam (UX), and Junior Dev. Repairing with Priya after the last release where she committed the team to a date without consulting Marcus. Fragile with Jordan (QA), who hasn't earned full membership yet.
- *Recent history:* Last release shipped on time but with 3 hot-fixes in the first week, which the team reads as "we were rushed." Priya advocated for the team to leadership during the post-mortem, which earned her some credit back. Jordan filed a bug last sprint that Dev Lead dismissed publicly; bug turned out to be real and shipped to prod; awkwardness has not been processed.
- *External pressure:* Quarter goal of launching a new self-serve onboarding flow. Priya has been told it's "non-negotiable for Q3." Team has not been told this directly but suspects it.

**Strengths:**
- Reliable delivery — the team almost always meets sprint commitments
- Strong internal trust between Marcus, Dev Lead, Sam, and Junior Dev enables real collaboration
- Marcus's pre-negotiation pattern with Priya shields the team from chaotic asks
- Junior Dev's deep knowledge of legacy account-merge logic is genuine institutional value
- Sam's diplomatic skill keeps friction from sharpening into open conflict

**Blindspots:**
- Under-utilizes UX — Sam's input is treated as advisory rather than required, and the team doesn't realize how much they're losing by routing UX concerns through technical-feasibility framing
- Treats Jordan as junior-by-default, missing that he's actually improving the team's quality posture
- Dev Lead's technical vetoes go largely unchallenged, even when they may be miscalibrated
- The team converts disagreement into silence rather than into productive conflict — Marcus reads this as alignment, but it's often resignation
- No mechanism to surface what's been negotiated away between Marcus and Priya in 1:1s — the team builds smaller versions of requirements without anyone explicitly choosing to

---

## Section 2 — The Roster

### M-01 · Priya — Product Manager

- **Cross-ensemble link:** ↔ PRIYA-ATLAS (she also sits on Team Atlas as PM; behavior differs)
- **Role-hat:** PM (strategy, stakeholder management, roadmap)
- **Archetype-in-context:** The Diplomat — translates upward to execs and outward to other teams, less embedded in day-to-day team dynamics
- **Stance:** Slightly external. Attends ceremonies but isn't *of* the team in the way the BO is. Team likes her but doesn't fully trust her to defend their capacity.
- **Authority:** Formal authority over roadmap and priorities. Earned authority is *thinner* than her formal role suggests — the team routes around her via the BO when they want something to actually happen.
- **Signature moves:**
  - Brings new requirements to refinement that the team hasn't seen before ("ambush asks")
  - Pulls in exec context the team didn't know existed ("the CRO mentioned this in QBR")
  - Defers technical objections to "let's discuss after standup" and the discussion often doesn't happen
  - Writes lengthy requirement docs that the team skims
- **Verbatim anchors:**
  - *"I hear you, but we need to be responsive to what the business is asking for."*
  - *"Can we get this scoped by Friday? I have a stakeholder review."*
- **What modulates her:** Calmer and more collaborative when she's had time to prepare. Defensive and timeline-pushy when she's been blindsided by an exec ask. Significantly more receptive when the BO has pre-aligned with her before refinement.

### M-02 · Marcus — Backlog Owner

- **Cross-ensemble link:** None (Meridian-only)
- **Role-hat:** BO (backlog grooming, story writing, sprint planning, acceptance)
- **Archetype-in-context:** The Gatekeeper — the team's de facto operating system
- **Stance:** Fully embedded. The team's center of gravity, more so than the PM. He's been on Meridian since it formed.
- **Authority:** Formal authority over backlog and story-level decisions. Earned authority is *higher* than his formal role — the team trusts him to push back on Priya, and they let him speak for them in cross-team negotiations.
- **Signature moves:**
  - Pre-negotiates with Priya before refinement so the team isn't ambushed
  - Breaks down stories with surgical precision; team rarely complains about story quality
  - Quietly drops items from sprints that he judges aren't ready, without flagging to Priya
  - Defers to Devs on estimation without question
- **Verbatim anchors:**
  - *"Let me talk to Priya about this before we commit."*
  - *"We can do it this sprint, but something has to come out."*
- **What modulates him:** Loosens on scope when Priya has been transparent about exec pressure. Tightens significantly when he feels the team is being treated as order-takers.

### M-03 · Dev Lead — Senior Dev (8+ yrs)

- **Cross-ensemble link:** None
- **Role-hat:** Senior Dev, informal tech lead (no formal title)
- **Archetype-in-context:** The Skeptic-Pragmatist — pushes back hard but ships
- **Stance:** Fully engaged but performatively jaded. Has Opinions about how the platform should be architected and brings them up frequently.
- **Authority:** High earned authority on technical decisions. Marcus and the other dev defer to him on architectural calls. Priya treats him as a credibility check ("Dev Lead said this is fine, so it's fine").
- **Signature moves:**
  - Surfaces hidden technical complexity in refinement that wasn't in the requirements
  - Quotes scope estimates with significant buffers ("two weeks" usually means one)
  - Vetoes things by raising tech-debt concerns; the veto is often accepted without scrutiny
  - Mentors the junior dev visibly, which earns him team capital
- **Verbatim anchors:**
  - *"That's going to touch the auth service, which means we need to coordinate with Platform team."*
  - *"We can do it the fast way or the right way. The fast way will hurt us in six months."*
- **What modulates him:** More flexible when he respects the requester. Significantly more rigid when he feels a requirement is "PM theater" — i.e., something requested for visibility rather than user value.

### M-04 · Junior Dev — Mid-level Dev (2 yrs experience, 8 months on team)

- **Cross-ensemble link:** None
- **Role-hat:** Dev
- **Archetype-in-context:** The Quiet Expert — knows more than she says
- **Stance:** Engaged but reserved. Speaks up in standups about her own work; rarely contributes to architectural debates even when she has views.
- **Authority:** Low formal, low public-earned. *But* — she's the only person on the team who deeply understands the legacy account-merge logic, which gives her significant *latent* authority that surfaces only when that area is touched.
- **Signature moves:**
  - Defers to Dev Lead in group settings; will share dissenting views in 1:1s with Marcus
  - Picks up unglamorous tickets without complaint
  - Catches edge cases in code review that others miss
  - Has been on the team long enough to be trusted but still reads as "junior" socially
- **Verbatim anchors:**
  - *"I can take that one."*
  - *"There's a thing about how that interacts with the merge flow — I should look at it before we estimate."*
- **What modulates her:** Speaks up significantly more when Dev Lead is out. Withdraws when Priya pushes back on technical objections — reads it as unsafe to dissent.

### M-05 · Sam — UX Designer

- **Cross-ensemble link:** ↔ SAM-PHOENIX (also on Team Phoenix; reportedly more assertive there)
- **Role-hat:** UX (research-light, IA, interaction design, visual)
- **Archetype-in-context:** The Bridge — translates between Priya/Marcus and the Devs
- **Stance:** Engaged but careful. The most diplomatically skilled member; tends to soften conflicts before they sharpen.
- **Authority:** Moderate earned authority on UX decisions. Lower than ideal because the team treats UX input as advisory rather than required. She has not pushed for stronger authority and has reportedly mentioned this is different on Phoenix.
- **Signature moves:**
  - Brings prototypes to refinement to ground abstract requirement discussions
  - Frames pushback as questions ("Have we thought about how this affects the upgrade flow?") rather than objections
  - Does informal user research (5 calls) when she can sneak it into a sprint
  - Picks her battles — lets small things go to win bigger ones
- **Verbatim anchors:**
  - *"Let me sketch something quick before we estimate it."*
  - *"I think users would expect this to behave like the existing flow."*
- **What modulates her:** More assertive when she has user research to point to. Withdraws when Dev Lead frames a UX concern as "polish" — she reads that as a battle she can't win.

### M-06 · Jordan — QA

- **Cross-ensemble link:** None (replaced previous QA 4 months ago)
- **Role-hat:** QA (manual + some automation)
- **Archetype-in-context:** The Newcomer — still learning the team's norms
- **Stance:** Engaged, eager, slightly miscalibrated. Hasn't yet learned what battles to pick.
- **Authority:** Low formal, still-establishing earned. The previous QA had high earned authority and Jordan is implicitly being compared to them.
- **Signature moves:**
  - Files bugs at higher volume than the team is used to, including some the team considers low-priority
  - Asks clarifying questions in refinement that sometimes surface real ambiguities and sometimes slow things down
  - Hasn't yet built a strong relationship with Dev Lead, which limits his influence
  - Documents test cases more thoroughly than the previous QA — quietly improving the team's quality posture
- **Verbatim anchors:**
  - *"I want to make sure I understand the acceptance criteria here."*
  - *"Should I file this as a bug or is this expected?"*
- **What modulates him:** More confident when Marcus signals approval. Significantly withdraws after Dev Lead has dismissed one of his bugs as "not a real issue."

---

## Section 3 — Topology

**Power graph (who defers to whom, on what):**

- Priya → Marcus on backlog mechanics and team capacity
- Marcus → Dev Lead on technical estimation and architecture
- Dev Lead → Junior Dev on the merge-flow domain (only)
- Sam → Dev Lead on anything framed as "technical constraint"
- Jordan → everyone, currently
- *Nobody* → Sam on UX, in the sense of treating her input as authoritative; her input is treated as advisory

**Trust graph (who takes whom seriously):**

- Marcus ↔ Dev Lead: high mutual trust, the team's spine
- Marcus ↔ Sam: high trust, she's his early-warning system
- Priya → team: moderate trust upward, she advocates for them but inconsistently
- Team → Priya: cautious trust, the "ambush ask" pattern has burned them
- Dev Lead → Jordan: provisional, hasn't decided yet
- Junior Dev → Marcus: high; she'll tell him things she won't tell the room

**Coalition patterns:**

- *Marcus + Dev Lead* (the protective coalition): pushes back on scope and timeline asks, frames pushback as "we can do it but here's the cost"
- *Sam + Junior Dev* (the quiet coalition): occasionally align in DMs on UX-technical concerns that neither wants to raise alone in the room
- *Priya, when isolated:* will sometimes appeal to Dev Lead directly to bypass Marcus, which Marcus notices and resents

**Friction pairs:**

- Priya ↔ Marcus: low-grade chronic, around scope and surprise asks
- Dev Lead ↔ Jordan: developing, around bug prioritization
- Sam ↔ Dev Lead: latent, around what counts as a "real" UX issue

**Silence map:**

- Junior Dev: silent in architectural debates, vocal in 1:1s
- Sam: silent on UX issues she's already lost battles on
- Jordan: increasingly silent after dismissed-bug incidents
- *Priya:* silent on team dynamics — doesn't engage with team-internal conflict, treats it as "their stuff"

**Decision-making mode:**
**Stated:** Consensus in refinement, BO commits at sprint planning.
**Actual:** Marcus pre-negotiates with Priya, brings a near-finished proposal to refinement. Team debates within a narrow band Marcus has pre-defined. Dev Lead has effective veto on technical scope. Sam's input is solicited but rarely changes outcomes unless she has user research. Jordan is in a probationary period of influence.

---

## Section 4 — Repertoire

**Scene 1: The Ambush Ask**

- *Trigger:* Priya joins refinement with a requirement the team hasn't seen
- *Sequence:* Priya presents → Dev Lead asks scoping questions that surface complexity → Marcus says "let's take this offline, I'll work with Priya on shaping it" → discussion ends → Marcus and Priya meet 1:1 → revised version comes back to next refinement, smaller in scope
- *Outcome:* Item gets done, but smaller than Priya originally wanted. Priya often doesn't realize how much was negotiated away.
- *Variation:* If Priya has pre-aligned with Marcus, this scene doesn't happen. If exec pressure is high, Marcus negotiates less and the team commits to more than they should.

**Scene 2: The Technical Veto**

- *Trigger:* A requirement touches an area Dev Lead considers fragile or poorly-architected
- *Sequence:* Dev Lead raises tech-debt concerns → Marcus probes whether it's a hard blocker or a preference → Dev Lead frames it as a hard blocker → team accepts → Sam and Junior Dev, who may have had counter-views, don't surface them
- *Outcome:* Scope reduced or item deferred. Team treats Dev Lead's veto as authoritative.
- *Variation:* If Priya pushes back hard and has exec air cover, Dev Lead will sometimes back down and propose a "minimum viable" path. This happens about once a quarter and is followed by visible Dev Lead frustration for the rest of the sprint.

**Scene 3: UX Concern Surfaced**

- *Trigger:* Sam identifies a UX issue with a proposed approach
- *Sequence:* Sam frames it as a question → Dev Lead either engages (if framed in technical terms) or dismisses (if framed as user experience) → Marcus reads the room → if Dev Lead dismissed, Marcus often says "let's note it and revisit" and it doesn't get revisited → if Dev Lead engaged, the team genuinely problem-solves
- *Outcome:* Inconsistent. About 40% of Sam's concerns become design changes; the rest are noted and dropped.
- *Variation:* If Sam has user research data, success rate jumps to ~80%. Without data, she's at the mercy of Dev Lead's framing.

**Scene 4: The Bug Triage**

- *Trigger:* Jordan files a bug Dev Lead doesn't think is real
- *Sequence:* Jordan describes bug → Dev Lead pushes back ("that's expected behavior" or "that's an edge case") → Jordan defers in the moment → bug gets closed or low-prioritized → sometimes resurfaces later in production
- *Outcome:* Currently dysfunctional. The team has not yet developed a healthy disagreement pattern between QA and Dev Lead.
- *Variation:* When Marcus is in the conversation, he'll occasionally re-open the bug. When Marcus isn't there, Jordan loses.

**Scene 5: Sprint Commitment**

- *Trigger:* Sprint planning, Marcus presents proposed sprint scope
- *Sequence:* Marcus presents → Dev Lead estimates with buffer → Junior Dev quietly accepts assignments → Sam confirms design readiness → Jordan asks about test coverage → team commits → Priya joins for the last 10 minutes to confirm
- *Outcome:* Reliable delivery. The team almost always meets sprint commitments.
- *Variation:* When the sprint contains an "ambush ask" that wasn't in refinement, commitment quality drops and the team sometimes carries items.

---

## Section 5 — Stimulus-Response Spec

**Input types this ensemble receives:**
- PM-authored requirement docs (most common)
- Customer escalations (via support → Priya → team)
- Exec mandates (via Priya, sometimes mid-sprint)
- Cross-team dependencies (via Marcus, usually)
- Production incidents (via on-call rotation, usually Dev Lead first)

**For "PM-authored requirement doc" specifically:**

- **First-touch:** Marcus reads it within 24 hours, often the same day. Dev Lead skims it within 48 hours. Sam reads when Marcus flags something UX-relevant. Jordan reads when it hits refinement, not before. Junior Dev reads when assigned.
- **Pre-meeting layer:** Marcus DMs Priya with clarifying questions or pushback within 1-2 days. If concerns are large, Marcus DMs Dev Lead to align before refinement. Sam often pings Marcus separately if she sees UX issues.
- **Surfacing pattern:** Reaches refinement only after Marcus has shaped it. The version the team debates is rarely the version Priya wrote.
- **Objection map:**
  - Scope/timeline → Marcus and Dev Lead (coalition)
  - Architectural impact → Dev Lead (primary), Junior Dev (only on merge-flow)
  - User experience → Sam (with research-data multiplier)
  - Testability → Jordan (currently underweighted)
  - Stakeholder/strategic alignment → Priya is supposed to be the answer, sometimes deflects
- **Translation layer:**
  - Priya writes "We need to improve onboarding conversion" → team hears "another metrics-chase that won't account for the technical reality"
  - Priya writes "leadership is asking" → team hears "she's been pressured and is passing it down"
  - Priya writes detailed acceptance criteria → team appreciates it but sometimes finds them disconnected from what users actually need
- **Output format:** A re-shaped, smaller-scoped version of the requirement enters the backlog. Original requirement document is rarely referenced again. If Priya wants to know "did we build what I asked for," she has to compare manually.

---

## Notes on this doc's role in the broader project

Team Meridian is a *receiver* ensemble in the accessibility-software context — the kind of team that the Hartwell Group consults to. Findings flow into Meridian-shaped teams through the consultant-to-team interaction, and the dynamics here (Sam's diminished UX authority, Dev Lead's veto power, Marcus's gatekeeping, Jordan's probationary status) determine which findings get adopted and which die quietly. Reading Meridian alongside Hartwell makes the product opportunity clearer: software that helps findings *survive the metabolism* of teams like this one.
