# No AI Design Slop

> **Now part of [Forge Skills](https://github.com/zyadhajaji/forge-skills).** This skill lives on as `slop-gate`, which adds a zero-dependency audit script that checks accessibility, motion, performance and taste in your code. Install the suite for the latest version. This repo stays available but will not be updated.

No AI Design Slop is an agent skill that acts as a passive design quality gate. While your coding agent builds or edits a website, app or mockup, it catches generic AI design defaults, incoherent visual choices and real UI defects before they compound, and it does this without flattening your art direction into a neutral template.

## How it works

Slop is not a color, a font, a gradient or a card. It is a choice made by reflex instead of for the product. This skill teaches your agent to tell the difference.

Before choosing a direction, the agent reads your local instructions, tokens, `DESIGN.md`, screenshots and existing components. It identifies the product, the audience, the primary action and one visual thesis for the surface. Then, every time it adds a section, a component, an effect or a state, it runs a set of compact quality gates: system, hierarchy, composition, typography, color and material, product truth, interaction, and motion and access.

When something looks suspect, it applies a removal test. Name the element precisely, state its job, remove it mentally, and delete it if clarity improves. Only if removing it causes a real loss does it make the smallest correction using the existing system.

For a narrow edit it stays narrow. For a full page, a redesign or an explicit anti-slop pass, it pulls in the full pattern library.

The skill triggers automatically during UI work, and on demand when you ask for a slop cleanup.

## Installation

### Claude Code (plugin marketplace)

```bash
/plugin marketplace add zyadhajaji/no-ai-design-slop
```

```bash
/plugin install no-ai-design-slop@no-ai-design-slop
```

### Claude Code (manual)

```bash
git clone https://github.com/zyadhajaji/no-ai-design-slop.git
cp -r no-ai-design-slop/skills/no-ai-design-slop ~/.claude/skills/
```

### Codex, Cursor and other agents

Copy `skills/no-ai-design-slop` into your agent's skills folder (for Codex, `~/.codex/skills/`), or point the agent at `skills/no-ai-design-slop/SKILL.md`.

### Verify installation

Ask your agent to "Do an anti-slop pass on this landing page". It should name concrete patterns, explain their job and report what it removed and why.

## What's inside

- `skills/no-ai-design-slop/SKILL.md`: core judgment, passive workflow, design principles, quality gates, the removal test, boundaries and verification.
- `skills/no-ai-design-slop/ARTICLE.md`: the pattern library, a heuristic inventory of slop patterns organized by area.
- `skills/no-ai-design-slop/REFERENCES.md`: sources, including WCAG 2.2, Nielsen Norman heuristics and platform typography guidance.

## Philosophy

- **Judge the result, not the author.** No guessing whether AI made it.
- **Taste is contextual.** A purple gradient can be right for one product and lazy for another.
- **Coherence beats decoration.** One strong idea carries a page; five unrelated ideas make noise.
- **Product truth.** No invented customers, metrics, testimonials, awards or screens.
- **Preserve character.** Useful density, edge, humor and expressive motion stay.

## Pairs well with

- [build-awwwards-quality-sites](https://github.com/zyadhajaji/build-awwwards-quality-sites)
- [editorial-portfolio-chapters](https://github.com/zyadhajaji/editorial-portfolio-chapters)
- [forge-genome](https://github.com/zyadhajaji/forge-genome)

## Updating

```bash
/plugin update no-ai-design-slop
```

## License

MIT License. See the [LICENSE](LICENSE) file for details.
