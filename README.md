# finding-unknowns

An agent skill that maps a task's unknowns with a staged **quadrant walk** — known knowns, known unknowns, unknown knowns, unknown unknowns — ending with a four-quadrant map in your hands, then carries the map through implementation notes, buy-in docs, quiz gates, and session handoffs.

> The map is not the territory. The prompt, the plan, and the context window are the map; the codebase, the domain, and your actual intent are the territory. The gap between them is the unknowns — and an unknown found before code is written costs minutes, while the same unknown found three PRs later costs the three PRs.

## What it does

Five stages, walked in order, one at a time, each behind a progressive-disclosure reference the agent loads on entry:

| Stage | Quadrant | What happens |
|---|---|---|
| 1 | Known knowns | Scan the territory (parallel subagents), open with the settled ground, cited |
| 2 | Known unknowns | Interview — one question per turn, blast-radius first, each with a recommendation; brainstorm interventions; map references before porting |
| 3 | Unknown knowns | Extract taste and tacit context via reactable artifacts: design directions, clickable mocks, vocabulary teaching, concrete samples |
| 4 | Unknown unknowns | Sweep for landmines: evidence cards, unwritten conventions, dead prior attempts |
| 5 | Hand over the map | The completed map artifact + a tweakable plan + a copyable implementation prompt |

After the walk: **implementation notes** (deviations log), the **buy-in doc**, the **quiz before merge**, and the **handoff** for fresh sessions.

Asked for one slice ("do a blindspot pass", "quiz me on this change")? It runs that slice and stops — no forced ceremony.

## Install

```bash
npx skills add avivsinai/finding-unknowns -g
```

Or via the [avivsinai marketplace](https://github.com/avivsinai/skills-marketplace) for Claude Code:

```
/plugin marketplace add avivsinai/skills-marketplace
/plugin install finding-unknowns@avivsinai-marketplace
```

## Example invocations

- "Do a **blindspot pass** — I'm adding an auth provider but know nothing about the auth modules here."
- "**What am I missing?** What should I be asking you?"
- "Give me 4 wildly different design directions to react to before you touch the real app."
- "Interview me one question at a time; prioritize answers that would change the architecture."
- "Keep an implementation-notes file; log deviations and keep going."
- "**Quiz me** on this change — I only merge after I pass."
- "Write the **handoff** — I'm continuing this in a fresh session tomorrow."

## Provenance

A best-of-breed synthesis:

- Base: [explore-unknowns](https://github.com/dzhng/skills) by [David Zhang](https://github.com/dzhng) (MIT), vendored and adapted with permission of its license.
- Process: [Thariq Shihipar](https://x.com/trq212)'s *A Field Guide to Fable: Finding Your Unknowns* (Anthropic).
- Extensions: operating-posture rules (stop-on-conflict, no-sycophancy, evidence-backed closure) distilled from [Addy Osmani's agent-skills](https://github.com/addyosmani/agent-skills); interview unordered-sets rule and the handoff move from [David Ondrej's skills](https://github.com/davidondrej/skills).
- Packaging and synthesis: [Aviv Sinai](https://github.com/avivsinai).

## License

MIT — see [LICENSE](LICENSE) (preserves upstream copyright).
