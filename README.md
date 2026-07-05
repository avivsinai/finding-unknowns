# finding-unknowns

An agent skill that codifies [Thariq Shihipar's](https://x.com/trq212) process from *A Field Guide to Fable: Finding Your Unknowns* — discovering and resolving your unknowns before, during, and after implementation.

> The map is not the territory. The map is your prompts and context; the territory is the codebase and the real world. The difference is your unknowns — and the quality of long-horizon agentic work is bottlenecked by your ability to clarify them.

## What it does

The skill classifies your unknowns into four quadrants and routes each to the cheapest technique that converts it into a known:

| Quadrant | Technique |
|---|---|
| Known knowns (already in your prompt) | Restate scope |
| Known unknowns (you know the question) | **Interview** / **Reference hunt** |
| Unknown knowns (tacit — taste, house style, "I'd recognize it if I saw it") | **Directions & prototypes** / examples to compare |
| Unknown unknowns (unfamiliar territory) | **Blind-spot pass** |

Then it carries the loop through implementation (**change-led plan**, `implementation-notes.md` **deviations log**) and past it (**explainer/pitch** for buy-in, **quiz gate** before merge).

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

## Credits

Process by [Thariq Shihipar](https://x.com/trq212) (Anthropic). Skill packaging by [Aviv Sinai](https://github.com/avivsinai).

## License

MIT
