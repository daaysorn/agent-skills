# Install on a new machine

Clone this archive, then copy (or symlink) the skill packs you want into each tool’s skills directory.

```bash
git clone https://github.com/daaysorn/agent-skills.git
cd agent-skills
```

## Recommended (avoid duplicates)

Copy these two packs first:

```bash
mkdir -p ~/.agents/skills ~/.grok/skills ~/.codex/skills ~/.cursor/skills-cursor

# Shared ecosystem skills (Convex, Resend, HeroUI, GSAP, etc.)
cp -R sources/agents/* ~/.agents/skills/

# One superpowers set (Claude marketplace naming)
cp -R sources/claude-marketplace-superpowers/* ~/.claude/plugins/marketplaces/superpowers-dev/skills/ 2>/dev/null || \
  mkdir -p ~/.agents/skills && cp -R sources/claude-marketplace-superpowers/*/ ~/.agents/skills/ 2>/dev/null || true
```

Prefer installing **superpowers** via the official Cursor/Claude plugin or marketplace when available, instead of copying every `*superpowers*` folder.

## Per-tool destinations

| Tool | Copy from | Into |
|------|-----------|------|
| Shared / Claude | `sources/agents/` | `~/.agents/skills/` |
| Cursor built-in style | `sources/cursor-builtin/` | `~/.cursor/skills-cursor/` |
| Grok | `sources/grok/` | `~/.grok/skills/` |
| Codex | `sources/codex-superpowers/` | `~/.codex/skills/` |
| Codex system | `sources/codex-system/` | `~/.codex/skills/.system/` |
| Motion (Cursor plugin) | `sources/cursor-plugin-motion/` | your Cursor Motion plugin skills dir |

Example — Grok only:

```bash
mkdir -p ~/.grok/skills
cp -R sources/grok/* ~/.grok/skills/
```

Example — Cursor built-ins:

```bash
mkdir -p ~/.cursor/skills-cursor
cp -R sources/cursor-builtin/* ~/.cursor/skills-cursor/
```

Restart Cursor / Claude / Grok / Codex after copying.

## Skills CLI (ecosystem packages)

Many skills under `sources/agents/` also install via:

```bash
npx skills find [query]
npx skills add <owner/repo>
npx skills check
npx skills update
```

Browse: https://skills.sh/

## Notes

- Folders like `grok/`, `codex-superpowers/`, and `cursor-plugin-superpowers/` overlap. Pick **one** superpowers source.
- See `meta/skill-index.json` for the full inventory from collection time.
- Third-party licenses stay with the original skill folders; this repo is an archive, not a relicense.
