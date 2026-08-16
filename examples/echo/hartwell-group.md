# Ensemble: The Hartwell Group

**Document Type:** Ensemble (Deep) v1.0
**Grounding:** Hypothetical — illustrative example, not research-grounded
**Last Updated:** 2026-05-05

---

## Lightweight Version

The Hartwell Group is a four-person centralized accessibility team inside a mid-sized financial services company, where they serve as internal consultants to ~30 product teams. They're respected, chronically over-capacity, and quietly cynical about how much of their work actually changes shipped products — but the team holds together because they genuinely like each other and share a sense that the work matters even when the org doesn't fully act on it.

---

## Section 1 — Ensemble Identity

- **ID:** ENS-HARTWELL
- **Stability:** Persistent team, ~3 years in current configuration. Team lead has been there 5 years (predates current structure). One member joined 8 months ago.
- **Origin context:** Formed after a 2022 ADA lawsuit settlement that required the company to establish a dedicated accessibility function. Reports into Design Ops, which reports into the CDO. Funding is "lawsuit-protected" — the team's existence is non-negotiable, but its growth is hard to justify.
- **Composition shape:** A specialist team with internal role differentiation (lead, senior auditor, mid-level auditor, technical specialist). Role-complete for what they're scoped to do; role-thin for what the org actually needs from them.

**Current state:**

- *Mood / phase:* Steady-state weariness. Not crisis, not burnout — a chronic sense of "we're holding the line." Recently lost a budget request for a fifth headcount, which the team is still processing.
- *Trust temperature:* High internally. Cautious externally — they've been disappointed enough by product teams that they enter new engagements with low expectations.
- *Recent history:* Team lead was passed over for a promotion 4 months ago; she's stayed, but the team noticed. Newest member is still in calibration, performing well technically but hasn't yet been "tested" by a difficult product team.
- *External pressure:* The company is preparing for a SOC2-adjacent compliance audit that includes accessibility components, which has spiked demand for the team's work without any commensurate capacity increase.

**Strengths:**
- Deep technical competence; their findings are almost never wrong on the merits
- Strong internal trust enables candid disagreement and fast iteration
- Institutional memory — they remember which product teams burned them and adjust accordingly
- Genuinely good at the *audit* part of accessibility auditing

**Blindspots:**
- Underweight the *political* work of getting findings adopted. They optimize for being right, not for being acted on.
- Treat product teams as adversaries by default, which becomes self-fulfilling
- Internal cynicism leaks into external interactions in ways the team doesn't fully see
- The team's identity is built around being *gatekeepers and remediators* rather than *enablers and educators*, which limits the kinds of value they can produce
- Almost no measurement of their own impact downstream. They count audits delivered, not issues actually fixed in production.

---

## Section 2 — The Roster

### M-01 · Diane — Team Lead, Senior Accessibility Specialist

- **Cross-ensemble link:** None currently (Hartwell-only)
- **Role-hat:** Team management, senior auditing, executive-facing accessibility advocate
- **Archetype-in-context:** The Battle-Tired Veteran — competent, principled, increasingly conserving energy
- **Stance:** Engaged with her team, performatively patient with the org, privately disillusioned. The promotion miss has sharpened this; she's reportedly considering external roles but hasn't told the team.
- **Authority:** High formal (team lead). High earned within the team. Moderate-and-declining earned with the broader org — she was more influential 2 years ago than she is now, and she knows it.
- **Signature moves:**
  - Triages incoming requests with implicit prioritization the team understands but isn't documented
  - Goes to bat for the team in resourcing conversations, then comes back drained
  - Speaks last in team discussions; her position usually carries
  - Increasingly delegates external-facing work to Marcus (M-02) — partly mentorship, partly conservation
- **Verbatim anchors:**
  - *"We can do that audit, but I want to be clear about what happens next: nothing, probably."*
  - *"I'm not going to write that finding any softer. They can read it or not."*
- **What modulates her:** Sharper and more incisive when working on technical audits. More withdrawn and political-tax-aware in stakeholder meetings. Significantly more present and warm when mentoring Priya (M-04, the newcomer).

### M-02 · Marcus — Senior Auditor, Informal Deputy

- **Cross-ensemble link:** None
- **Role-hat:** Senior auditing, increasingly the team's external-relationship lead, technical specialist on screen reader testing
- **Archetype-in-context:** The Diplomat-Specialist — technically rigorous and politically aware in equal measure
- **Stance:** Fully engaged. Has been positioning (deliberately or not) as Diane's successor; the dynamic is healthy because Diane has been mentoring him into it.
- **Authority:** High earned within the team, second only to Diane. Higher external earned authority than Diane *with younger product teams* — they find him easier to work with. Lower with senior stakeholders, who default to Diane.
- **Signature moves:**
  - Reframes findings into language product teams can actually act on
  - Builds informal relationships with specific PMs and devs across the org, which short-circuits political friction
  - Pushes the team to track downstream remediation, gets gentle pushback from Diane ("we don't have the bandwidth")
  - Quietly disagrees with Diane on team strategy but doesn't surface it; the team senses this and waits to see if it surfaces
- **Verbatim anchors:**
  - *"Let me rewrite this finding before we send it. It's right, but it'll bounce off them."*
  - *"I don't want us to be the team that's just always saying no."*
- **What modulates him:** More directive when Diane isn't in the meeting. More deferential when she is. More frustrated than usual lately, post-promotion-miss — he's read the situation and is calibrating his next move.

### M-03 · Sasha — Mid-level Auditor, Code-Side Specialist

- **Cross-ensemble link:** None
- **Role-hat:** Technical auditing with strong frontend dev background — does code-level audits, not just behavioral testing
- **Archetype-in-context:** The Quiet Technical Authority — speaks rarely, definitively when she does
- **Stance:** Engaged with the work, low-engagement with team politics. Doesn't go to lunch with the team often. Respected but not socially central.
- **Authority:** Moderate earned within the team — high on technical questions, deferred-to on code-level findings. Low influence on team strategy or external-facing work; doesn't seek it.
- **Signature moves:**
  - Takes on the most technically complex audits without being asked
  - Pushes back on findings she considers technically imprecise, including from Marcus
  - Maintains her own internal tooling (scripts, browser extensions) that she shares with the team but hasn't formally productized
  - Disengages from meetings she considers non-technical; will literally pick up her laptop and leave
- **Verbatim anchors:**
  - *"That's not what the spec says."*
  - *"I'll handle the code-level pass. The behavioral pass is yours."*
- **What modulates her:** Significantly more engaged when working alongside a competent dev on the product team side. Will deeply collaborate with respected devs and disappear from teams she considers technically weak.

### M-04 · Priya — Junior Auditor, Newest Member (8 months)

- **Cross-ensemble link:** None
- **Role-hat:** Auditing (still ramping), accessibility documentation, training material development
- **Archetype-in-context:** The Eager Apprentice — high-energy, high-output, still calibrating
- **Stance:** Highly engaged, slightly miscalibrated about which battles to pick. Genuinely loves the work in a way the rest of the team has somewhat lost.
- **Authority:** Low formal, growing earned. Diane is investing heavily in her, which gives Priya implicit air cover. Hasn't yet been "tested" by a hostile product team.
- **Signature moves:**
  - Volunteers for the audits no one else wants
  - Asks questions in team meetings that the senior members find either refreshing or naive depending on the day
  - Has started building accessibility training material for product teams, which is genuinely useful but isn't part of her formal scope
  - Looks up to Marcus more than Diane — a dynamic Diane has noticed
- **Verbatim anchors:**
  - *"What if we just... showed them how to fix it?"*
  - *"Why don't we have a way to measure if anything we do actually gets fixed?"*
- **What modulates her:** Significantly more confident when she has a finding she's certain about. Withdraws after she's been wrong publicly (which has happened twice in 8 months and she remembers both). More herself with Marcus than with Diane, which is mildly distorting her development.

---

## Section 3 — Topology

**Power graph:**

- Team → Diane on team strategy and external-facing positioning
- Diane → Marcus on younger-PM relationships and "how should we say this"
- Diane → Sasha on technical questions she's not deep on
- Marcus → Sasha on code-level findings
- Priya → everyone, currently
- *Notably:* No one defers to Priya yet on anything, including her own training-material work, which she'd benefit from owning more authoritatively

**Trust graph:**

- Diane ↔ Marcus: high mutual trust, the team's spine
- Diane ↔ Sasha: high trust on work, low engagement socially — they respect each other but don't need each other emotionally
- Marcus ↔ Sasha: collegial, technically aligned, slight friction over Marcus's diplomatic reframings (Sasha thinks they soften too much)
- Diane → Priya: warm, mentorship-shaped
- Marcus → Priya: collegial, becoming more central than Diane realizes
- Sasha → Priya: distant but not hostile; Sasha doesn't engage much with anyone socially
- Priya → all: high trust, possibly higher than warranted

**Coalition patterns:**

- *Diane + Marcus* (the strategic coalition): aligns on most external-facing decisions, with Diane increasingly delegating
- *Marcus + Priya* (the emerging coalition): around questions of team direction — measuring impact, training product teams, becoming more enabling and less gatekeeping. Diane is not part of this coalition and may not realize it's forming.
- *Sasha as independent operator:* doesn't coalition with anyone, which the team treats as fine

**Friction pairs:**

- Marcus ↔ Sasha: latent, around finding-language. Marcus softens; Sasha thinks softening is intellectual cowardice. Has not surfaced.
- Diane ↔ Marcus: emerging, around team direction. Marcus wants to invest in enablement; Diane has decided that's not realistic given capacity. Has not fully surfaced.
- *Notably absent:* No friction with Priya yet, but the team will eventually need to decide what role she grows into, and that's a decision Marcus and Diane disagree about implicitly.

**Silence map:**

- Sasha: silent in non-technical conversations, by choice
- Marcus: silent on his disagreements with Diane's strategy, by political calculation
- Priya: silent when she senses she might be wrong, increasingly so after each incident
- *Diane:* silent on her own career considerations, which is having ripple effects she doesn't see

**Decision-making mode:**
**Stated:** Collaborative team decisions, Diane has final call.
**Actual:** Diane sets direction, Marcus shapes execution, Sasha is consulted on technical questions, Priya is informed. Most decisions don't reach formal discussion — they emerge from Diane-Marcus 1:1s and are presented to the team as proposals. Team rarely pushes back, which Diane reads as alignment but Marcus reads as resignation.

---

## Section 4 — Repertoire

**Scene 1: The Audit Intake**

- *Trigger:* A product team requests an accessibility audit (via internal ticket queue)
- *Sequence:* Diane triages → assigns based on her implicit prioritization (technical complexity, political weight, team capacity) → Marcus or Sasha picks up most complex; Priya picks up "training opportunity" audits → assigned auditor schedules kickoff with product team → finding patterns vary wildly by who's leading
- *Outcome:* Audit gets done, on a timeline determined more by team capacity than product team urgency
- *Variation:* If the request comes through executive escalation, normal triage is bypassed and Diane handles personally. This is happening more often as the compliance audit approaches.

**Scene 2: The Findings Handoff**

- *Trigger:* Audit complete, findings ready to be delivered to product team
- *Sequence:* Auditor drafts report → if Marcus: he'll workshop the language; if Sasha: she'll send as-is; if Priya: she'll over-explain and Diane will edit; if Diane: precise and uncompromising → report sent → meeting scheduled with product team → meeting either goes well (rare, when product team has prepared) or becomes a defensive product-team-pushback session (common)
- *Outcome:* Report is delivered. ~30% of findings are addressed within 90 days. ~40% are addressed eventually. ~30% are never addressed and the team usually doesn't know which is which.
- *Variation:* When Marcus runs the meeting, the engagement rate is meaningfully higher. The team has noticed but hasn't formalized it.

**Scene 3: The Internal Critique**

- *Trigger:* Sasha thinks Marcus has softened a finding too much
- *Sequence:* Sasha raises it in their shared review → Marcus defends the reframing on grounds of "it'll actually get acted on" → Sasha disengages rather than escalating → finding goes out as Marcus wrote it → Sasha logs the disagreement internally and moves on
- *Outcome:* Finding ships in Marcus's voice. Sasha's pattern of disengagement is becoming a team pattern that Diane hasn't addressed.
- *Variation:* When Diane is in the review, she'll usually side with Sasha on the technical content but with Marcus on the language. This compromise satisfies neither but holds the team together.

**Scene 4: The Capacity Conversation**

- *Trigger:* New audit request arrives when team is already at capacity (which is most of the time)
- *Sequence:* Diane evaluates → if politically weighted (executive sponsor, lawsuit-adjacent, compliance-relevant): accepts and re-prioritizes existing work → if not: pushes back on timeline, sometimes declines → Marcus has started privately advocating for a more systematic intake process → Diane has not adopted his suggestion
- *Outcome:* Team continues to operate at over-capacity, with prioritization opaque to the org
- *Variation:* When the requesting team has a senior accessibility-aware advocate (rare), the conversation is more collaborative. When the requesting team is hostile or dismissive, Diane will sometimes accept anyway as a "make the audit show them what's wrong" move, which is its own pattern.

**Scene 5: Priya's Initiative**

- *Trigger:* Priya identifies an opportunity to be more enabling — a training program, a self-serve toolkit, an embedded model
- *Sequence:* Priya pitches in a team meeting → Marcus responds with measured enthusiasm → Diane responds with capacity-pragmatism ("we don't have bandwidth") → Sasha is silent → Priya adjusts her ambition downward → idea either dies or becomes a side project Priya does on her own time
- *Outcome:* Currently dysfunctional. The team is losing options it doesn't realize it's losing. Priya is at risk of either burning out on side projects or becoming cynical like the rest of the team.
- *Variation:* When Diane is in a particularly weary phase, she's slightly more open to delegation. Marcus has started timing his support for Priya's ideas to those moments — a coalition tactic Diane hasn't named.

---

## Section 5 — Stimulus-Response Spec

**Input types this ensemble receives:**

- Audit requests from product teams (most common)
- Executive escalations (compliance-driven, lawsuit-driven, customer-complaint-driven)
- Cross-team consultations (someone wants 30 minutes of accessibility input, not a full audit)
- New tooling/process proposals (internal — what the team should adopt)
- Industry-wide updates (WCAG version changes, new lawsuit precedents, regulatory shifts)

**For "audit request from a product team" specifically:**

- **First-touch:** Diane sees it within 24 hours. She does silent triage before assigning.
- **Pre-meeting layer:** Diane DMs Marcus with context if it's a politically weighted request. If it's a team Hartwell has worked with before, Diane checks the team's internal memory ("are these the people who never fixed the form errors?").
- **Surfacing pattern:** Reaches the team as an assignment, not a discussion. Team rarely debates intake decisions; they trust Diane's triage even when they disagree with it.
- **Objection map:**
  - "Is this a real priority?" → Diane (evaluates politically)
  - "Is the request scoped correctly?" → Marcus (will reshape if needed)
  - "Is the team ready for the kind of findings we'll produce?" → mostly unasked, which is itself a problem
  - Technical scope objections → Sasha (rare, only when request is technically incoherent)
- **Translation layer:**
  - Product team writes "we want an accessibility audit" → Hartwell hears "they need a compliance check before launch and probably won't fix most of what we find"
  - Product team writes "we're committed to accessibility" → Hartwell hears "they will be committed for ~2 sprints, then fall back to baseline"
  - Product team writes "can we partner with you on this?" → Hartwell hears "they want our credibility without the work"; Marcus hears "this might be the rare team that actually means it" and has a higher hit rate than the rest of the team on identifying which is which
- **Output format:** A formal audit report, a debrief meeting, a list of findings in the org's tracking system. *No systematic followup.* The team rarely sees what happens after delivery, and this gap is the team's biggest blindspot.

---

## Product Implications (notes for software for accessibility auditors)

1. The team's biggest pain isn't the audit work — it's everything around it. Triage, prioritization, language-reframing, followup, measurement. A tool that just helps Sasha do code-level audits faster is solving the part of the job the team is *already good at*. The leverage is in the wrap-around work that's currently unmeasured.

2. Diane and Marcus are different users of the same tool. Diane wants triage support, capacity visibility, and political-context-tracking. Marcus wants relationship-tracking, finding-reframing assistance, and downstream remediation visibility. Building for one will misserve the other.

3. Sasha will resist any tool that softens her findings. If your tool has AI-assisted finding-language features, Sasha's archetype will read it as exactly what's wrong with the field. Design those features to feel like *precision augmentation*, not *softening*.

4. Priya is your wedge user. Newer auditors, less burned, more open to new tools, more interested in measurement and impact. They'll adopt your software first. They'll also have the least authority to drive team adoption — so the wedge has to be designed to *grow into* Diane and Marcus's workflows.

5. The team's blindspot — no measurement of downstream impact — is a product opportunity. A tool that makes the tracking trivially easy could shift the team's identity from gatekeepers to enablers, which is the strategic shift Marcus and Priya are already pulling toward.

6. The "consultant-to-team" gap is where the real product lives. Hartwell produces findings → findings travel into product teams → most die. The software is the medium of that travel.
