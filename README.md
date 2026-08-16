# Ensemble Personas

**An experimental framework for modeling how groups of people, not individuals, metabolize change.**

Traditional personas describe individual users. Ensemble personas describe the social configurations that decide whether your product, feature, or change actually gets adopted. Same person behaves differently on different teams; same feature lands differently in different ensembles. This framework is built around that observation.

## What this is

A structured way to document teams (or other group configurations) in enough detail that AI can simulate how they'd react to inputs like feature concepts, requirements, organizational changes, and product launches. The output isn't "what would Sarah-the-PM think?" It's "what would *this team configuration* do with this, given how they're structured and what problems they actually have?"

Three things make this different from traditional personas:

- **The unit of analysis is the group, not the individual.** Topology, coalitions, decision-making patterns, and group state are first-class concerns.
- **Behavior is contextual.** The same person on two different teams is modeled as two different persona instances. Context, not character, drives a lot of variation.
- **Documents are operational, not descriptive.** They're built to be *run*, not just read. You drop a stimulus in and observe a predicted reaction.

## What this is not

- A replacement for talking to real users. The framework's value comes from grounding it in research, not from generating plausible-sounding fiction.
- A finished system. This is in active development. The schema, methodology, and skills are evolving as the framework gets used in real product contexts.
- A general-purpose AI persona tool. This is specifically designed for B2B contexts where teams (not individuals) are the meaningful unit of decision-making.

## How this differs from existing approaches

The conceptual starting point for this framework is the **digital twin** concept from engineering and manufacturing: building a model of a real system with enough fidelity to simulate its behavior under new conditions. A digital twin isn't a description of a machine. It's a queryable model you can run scenarios against. Ensemble personas try to apply that idea to teams: not just describe them, but model them operationally so you can ask "what would happen if I dropped this change on this group right now?"

The most directly adjacent class of approaches is AI-consultable or "virtual" persona frameworks, which make research repositories queryable through AI. These solve a *research distribution* problem: getting existing user research into the hands of stakeholders making decisions. That's a real and important problem.

Ensemble personas solve a different problem: *predicting how groups will react to changes*. Where AI-consultable persona frameworks are built for retrieval and synthesis, this framework is built for simulation. They're complementary; you could use both. See [docs/comparison.md](docs/comparison.md) for a fuller treatment.

## Quick example

A lightweight ensemble description (the "poster" version):

> The Hartwell Group is a four-person centralized accessibility team inside a mid-sized financial services company, where they serve as internal consultants to ~30 product teams. They're respected, chronically over-capacity, and quietly cynical about how much of their work actually changes shipped products, but the team holds together because they genuinely like each other and share a sense that the work matters even when the org doesn't fully act on it.

That paragraph is the surface. Underneath it sits a ~1500-word ensemble document that captures roster, topology, repertoire, and stimulus-response patterns in enough detail that you can ask: *if I drop a new feature concept on this team, how do they react?*

See [examples/echo/hartwell-group.md](examples/echo/hartwell-group.md) for the full document.

## How to use this framework

1. **Read [docs/concepts.md](docs/concepts.md)** to understand what ensembles are and why this approach exists.
2. **Read [docs/methodology.md](docs/methodology.md)** to learn how to apply the framework.
3. **Read [docs/research-methodology.md](docs/research-methodology.md)** when you're ready to do the research that grounds your ensembles. Includes a reusable interview script and synthesis guide.
4. **Copy [templates/ensemble-template.md](templates/ensemble-template.md)** and populate it for one of your ensembles.
5. **Use the AI skills** (see [skills/](skills/), Claude Code implementations in [skills/claude/](skills/claude/)) to synthesize research, populate documents, and run simulations against populated ensembles.

The framework requires a UX researcher (or similarly trained synthesizer) to do the ensemble identification work. AI can help populate documents and run simulations, but the work of looking at research and recognizing what ensembles exist is judgment work that doesn't delegate well.

## Repository structure

```
ensemble-personas/
├── docs/                        Concepts, schema, methodology, comparison, research methodology
├── templates/                   Blank templates ready to fill in
├── skills/                      AI skills for population, simulation, and synthesis (built, see skills/claude/)
└── examples/
    ├── echo/                    Reference ensembles for Echo, an accessibility audit tool
    └── use-cases/               Worked examples of running stimuli against ensembles
```

## Status

This framework is in active development. Current state:

- Schema: v1.0 (locked)
- Templates: v1.0
- Research methodology: v1.0 (interview script, synthesis guide, reflection template)
- Skills: v1.0. Population, simulation, and synthesis skills are specified and built for Claude Code; other platforms not yet implemented
- Examples: two ensembles (Hartwell, Meridian), one use-case walkthrough

Versioning follows the schema. Breaking changes to the schema will trigger major version bumps; additive changes will be minor.

## License

Released under [CC BY 4.0](LICENSE). You're free to use, adapt, and build on this framework, including commercially, with attribution.

## Contributing

This is a personal project at the moment. If you're using the framework or want to suggest improvements, please open an issue rather than a pull request. I want to keep the framework coherent while it's still finding its shape.

If you've used the methodology to populate ensembles of your own and have feedback on what worked and what didn't, that's especially valuable. The methodology gets better as more researchers use it across more domains.

## Acknowledgments

The conceptual move from "personas as descriptions" to "personas as simulations" draws on the digital twin tradition in engineering. A model is most valuable not when it describes a system, but when it can be run against new conditions. The group dynamics framing owes a debt to agent-based modeling traditions in social science. The "Character Bible" framing borrows from screenwriting, where ensemble dynamics have been formally modeled for decades.