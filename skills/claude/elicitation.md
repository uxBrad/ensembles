Interview the researcher directly, section by section, to build an ensemble document from what's in their head, not from pre-existing artifacts.

## When to Use

- User says "help me build an ensemble", "interview me about this team", "I know this team but haven't written anything up", "walk me through building an ensemble"
- User wants to construct an ensemble collaboratively through conversation, and doesn't have transcripts, notes, or other artifacts to hand over

If the user already has research artifacts (transcripts, notes, tickets), use the **synthesis** or **population** skills instead — those work from evidence already captured, which produces a more reliably grounded document than live recall. Elicitation is for when the researcher's own observation and memory is the only source available right now. It's a faster way to get a first draft down, not a replacement for grounding the document in real research over time.

---

## Inputs Required

Before starting, confirm:

1. **Which ensemble** — the researcher has already identified who the members are and what context bounds this group. This skill does not do identification. If they haven't identified it yet, help them think through who belongs and why before starting the interview.
2. **That the researcher has direct knowledge of this team** — they've worked with, observed, or closely studied this group. If they're guessing or working from secondhand impressions, say so upfront: the document that comes out of this will be weaker than one built from real research, and should be marked accordingly.

---

## Step 0: Set expectations

Before starting, tell the researcher:

- This will go section by section through the ensemble schema (Identity, Roster, Topology, Repertoire, Stimulus-Response).
- Answer "I don't know" or "not sure" whenever that's true. Those become explicit gaps, not guesses.
- The output is a first-draft ensemble document, sourced from your own recall rather than transcripts or notes. It's real research (you observed this team), but it's weaker grounding than a synthesized document, and the output will say so.

---

## Step 1: Interview section by section

Work through one schema section at a time, in this order: Identity, Roster, Topology, Repertoire, Stimulus-Response. Don't dump the whole schema as a giant form — ask a few focused questions per section, listen to the answer, and follow up before moving on.

Per section, a rough question set:

**Identity:** Who is this group, how long have they worked together, what's their current state (mood, pressure, momentum), what are they good at, where are they weak?

**Roster:** For each member — what's their role and authority (formal and earned)? What's their signature move — the thing they reliably do in a given situation? What changes their behavior (pressure, audience, topic)? Any specific things they've said or done that stick in your memory (verbatim anchors)?

**Topology:** Who defers to whom, and on what? Who forms coalitions? Who clashes, and about what? Who goes quiet, and when? How do decisions actually get made here, versus how the org chart says they should get made?

**Repertoire:** Walk me through a time this team missed a deadline. A time a hard topic got raised. A time someone pushed back on scope. What actually happened, not what should have happened.

**Stimulus-Response:** When a new requirement or ask lands on this team, who sees it first? What happens informally (DMs, hallway conversations) before it hits the group? Who objects, and to what? What tends to get lost in translation between what's asked and what the team hears?

For each answer, ask yourself: is this specific and confident, or vague and hedged? Note that distinction — it determines the confidence tag in Step 2.

---

## Step 2: Populate as you go, with the same evidence discipline as population

After each section, draft the corresponding part of the template using these treatments:

**Confident, specific recall:**
```
[Field content] (Source: researcher's direct observation)
```

**Hedged or uncertain recall:**
```
[Field content] [inferred — researcher was uncertain: "[their hedge, e.g. 'I think, but I'm not sure']"]
```

**No answer / researcher doesn't know:**
```
[insufficient research]
```

Show the researcher the drafted section before moving to the next one. Let them correct it. Don't silently carry a misreading forward into later sections.

---

## Step 3: Write the populated document

After all five sections are interviewed and confirmed, assemble the full ensemble document using the standard template structure, same as the population skill:

- Section 1: Ensemble Identity (including Lightweight Version, written last, as a summary)
- Section 2: The Roster
- Section 3: Topology
- Section 4: Repertoire
- Section 5: Stimulus-Response Spec

Add a grounding note at the top:

```
**Grounding:** Built via elicitation interview, not from artifacts — [N] fields from direct recall, [N] hedged, [N] gaps. Treat as a first draft; strengthen with real research artifacts (interviews, observation notes) where possible before relying on simulations against it.
```

---

## Step 4: Produce the gap report

Same format as the population skill's gap report — sparse sections, what research would close each gap (this time, likely: "conduct an actual interview using the script in docs/research-methodology.md," since elicitation draws only on one person's memory), confidence summary, and whether the document is ready to simulate against.

---

## Rules

- **Never fabricate.** If the researcher doesn't know, the field stays empty. Don't smooth over a shrug into a plausible-sounding answer.
- **Never do ensemble identification.** This skill interviews about an already-identified ensemble.
- **One researcher's recall is one source.** Say this explicitly in the grounding note. A document built this way is weaker than one built from multiple research artifacts or multiple people's input, and should be flagged as lower-confidence than a synthesized document by default.
- **Confirm before moving on.** Show each section back to the researcher before proceeding to the next. Interviews drift; catch it early.
- **This is a bootstrapping tool, not an endpoint.** The gap report should actively point back toward doing real research (the interview script in `docs/research-methodology.md`) to strengthen the document, not treat elicitation as sufficient on its own.
