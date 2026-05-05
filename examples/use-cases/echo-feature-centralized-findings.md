# Use Case: Echo Feature — Centralized Findings Dashboard

**Stimulus type:** Product feature concept
**Tested against:** Hartwell Group (`../echo/hartwell-group.md`)
**Date:** 2026-05-05

---

## Stimulus

Echo is considering a "Centralized Findings Dashboard" feature. The proposed value proposition: "All accessibility findings across all client engagements, in one searchable, filterable dashboard. Track status (open / in remediation / fixed / dismissed), see aging, identify patterns across teams, generate reports for leadership."

Question for the framework: How would the Hartwell Group react to this feature if Echo proposed it to them?

---

## Predicted Reaction

### Overall ensemble response: Mixed-positive, slow adoption, contested internally

The Hartwell Group would not react as a single voice. The feature would expose existing internal tensions (particularly between Diane's capacity-pragmatism and Marcus's enablement-orientation), and adoption would depend on which member's perspective wins out. Below, predictions per member:

### Diane (Team Lead) — Skeptical, gatekeeping

Diane's likely reaction: cautious-to-resistant. She'd evaluate the feature primarily through the lens of "does this add to our capacity problem or relieve it?" and on first glance it would look like more work — another tool to maintain, another dashboard to keep current, another thing for product teams to ask her about. Her promotion-miss-induced energy conservation makes her unlikely to champion new tooling.

She would ask whether the dashboard generates the kinds of reports leadership has been asking her for (which it could — this is a potential point of leverage). If yes, her resistance softens. If the feature is positioned around "team productivity" or "operational efficiency," she's likely to deflect.

### Marcus (Senior Auditor) — Champion

Marcus's likely reaction: enthusiastic. The feature directly addresses his existing frustrations — he's been pushing the team to track downstream remediation and getting pushback from Diane on capacity grounds. A tool that makes tracking trivially easy removes Diane's main objection to his agenda.

He would likely become Echo's internal champion at Hartwell. He'd be the one to schedule the demo, advocate to Diane, and onboard the team. Critically, he'd want to bring it to product teams (like Meridian) as part of the engagement, not just use it internally.

His enthusiasm has a wrinkle: if Echo is positioned as competing with how the team currently delivers findings rather than augmenting it, Marcus's diplomatic instincts would surface. He'd want to present it as "additional infrastructure" rather than "replacement workflow."

### Sasha (Code-Side Specialist) — Conditional

Sasha's likely reaction: depends entirely on whether the dashboard preserves technical precision. She maintains her own scripts and browser extensions; she's not anti-tool. But if the dashboard's data model loses information her current workflow captures (specific WCAG violations, code-level context, severity nuance), she'll dismiss it as "another product team tool."

She wouldn't object publicly. She'd just continue using her own tools and not feed data into the dashboard, which would silently undermine its value for the rest of the team. This is a real risk — Sasha's quiet non-adoption could make the dashboard feel half-empty even if Marcus and Priya actively use it.

### Priya (Junior Auditor) — Eager early adopter

Priya's likely reaction: most enthusiastic of the team. She's been asking the question "why don't we have a way to measure if anything we do actually gets fixed?" The dashboard answers exactly that question. She'd likely be the team's most active user from day one.

Her advocacy has limited weight — she doesn't have the authority to drive team adoption. But Marcus has been timing his support for her ideas to moments when Diane is more receptive, suggesting a coalition that could push the dashboard through.

### Net adoption prediction

Adoption is *possible but contingent*. The feature aligns with the team's emerging direction (the Marcus-Priya coalition's enablement-orientation) and against the team's current direction (Diane's capacity-pragmatism). Whether it lands depends on:

1. Whether Echo can position the feature as relieving Diane's capacity problem rather than adding to it
2. Whether Sasha's technical precision concerns are addressed
3. Whether Marcus is given enough institutional support to drive internal adoption
4. Whether the feature surfaces the kind of leadership-facing reports that would help Diane in resourcing conversations

If 1-4 land: meaningful adoption within 2-3 months.
If only 1-2 land: limited adoption, becomes "Marcus's tool."
If only 3-4 land: contested adoption with ongoing internal friction.
If none land: brief evaluation, polite decline.

---

## Evidence Trail

| Claim | Supported by |
|---|---|
| Diane evaluates new things through capacity lens | Section 1, "Recently lost a budget request for a fifth headcount"; Section 4, Scene 4 (Capacity Conversation); Section 4, Scene 5 (Diane's response to Priya's initiatives) |
| Diane's energy conservation post-promotion-miss | Section 1, "Recent history"; Section 2, Diane's "What modulates her" |
| Marcus pushes for downstream tracking, Diane pushes back | Section 2, Marcus's signature moves; Section 3, Friction pairs (Diane ↔ Marcus emerging) |
| Marcus would champion the feature | Section 2, Marcus's archetype and stance; Section 3, Marcus + Priya coalition; Section 1, Strengths/Blindspots ("Marcus and Priya are already pulling toward enabling") |
| Sasha's reaction depends on technical precision | Section 2, Sasha's "What modulates her" ("Will deeply collaborate with respected devs and disappear from teams she considers technically weak"); Section 4, Scene 3 (Internal Critique) |
| Sasha's non-adoption pattern would be quiet | Section 3, Silence map (Sasha silent in non-technical conversations) |
| Priya is most enthusiastic about measurement | Section 2, Priya's verbatim anchor: "Why don't we have a way to measure if anything we do actually gets fixed?" |
| Marcus times support for Priya's ideas | Section 4, Scene 5 variation: "Marcus has started timing his support for Priya's ideas to those moments" |

---

## Confidence Map

**High confidence:**
- Diane's capacity-skepticism reaction
- Marcus's enthusiasm and championing role
- Priya's eager early adoption
- The Marcus-Priya coalition dynamics
- Sasha's risk of quiet non-adoption

**Medium confidence:**
- Specific positioning that would change Diane's stance (capacity-relief framing, leadership-facing reports) — these are inferences from her stated motivations, not direct evidence
- Whether the Marcus-Priya coalition can drive adoption against Diane's resistance — this dynamic is forming in the doc but its outcome is unresolved
- The 2-3 month timeline for adoption — this is a guess based on team rhythm, not evidenced

**Low confidence / cannot predict:**
- Sasha's specific data-model concerns — the doc says she values technical precision but doesn't specify what that means for an external tool
- Whether Diane is actively interviewing for external roles and might leave during evaluation period — referenced as a possibility but not confirmed
- How the feature would interact with Sasha's existing custom tooling
- Whether the team has tried similar dashboards before and bounced off

---

## Research Gaps Identified

To strengthen this prediction, additional research would help:

1. **Sasha-equivalents on technical tooling preferences.** What specifically makes a tool feel like it respects technical precision vs. one that softens for product teams? This is the difference between Sasha championing or quietly killing adoption.

2. **Hartwell's history with previous tooling proposals.** Have they evaluated similar dashboards before? What happened? The doc doesn't say.

3. **Diane's specific resourcing-conversation needs.** What reports does leadership actually ask her for? If the dashboard could generate exactly those, the conversation with her is much easier.

4. **The relationship between Echo (as a new tool) and the team's existing systems.** Does Echo replace something? Augment? Integrate? The reaction depends heavily on this and the doc doesn't address it.

---

## Implications for Echo product strategy

A few takeaways from this simulation:

1. **The wedge user is Priya, the champion is Marcus, the gatekeeper is Diane, the silent risk is Sasha.** Echo's adoption playbook needs to address all four roles, not just one.

2. **Positioning matters more than features.** The same feature framed as "team productivity" lands worse than the same feature framed as "leadership-reporting infrastructure." Marketing language is part of the product.

3. **Don't assume Sasha-types are anti-tool.** They're anti-imprecision. Designing for technical precision might unlock a meaningful customer segment that would otherwise reject Echo silently.

4. **Diane's post-promotion-miss state is a real product risk.** If she's actively considering external roles, Echo could lose its decision-maker mid-evaluation. Worth having a backup champion.

5. **The feature's value is partially political, not just operational.** It gives Marcus ammunition for an argument he's been losing internally. Echo should make this explicit in the sales motion.
