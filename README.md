# agent-skills

Personal archive of AI agent skills collected from local installs on this machine (Grok, Cursor, Claude/Agents, Codex, and related plugins).

## Layout

```
sources/
  grok/                              # Grok superpowers skills
  cursor-builtin/                    # Cursor built-in skills (~/.cursor/skills-cursor)
  cursor-plugin-superpowers/         # Cursor superpowers plugin cache
  cursor-plugin-motion/              # Motion plugin skill
  agents/                            # Shared agent skills (~/.agents/skills)
  claude-marketplace-superpowers/    # Claude marketplace superpowers-dev
  codex-superpowers/                 # Codex-installed superpowers copies
  codex-system/                      # Codex built-in system skills
  codex-plugin-superpowers/          # Codex plugin superpowers
  codex-plugin-creator/              # Codex plugin-creator skill
meta/
  skill-index.json                   # Generated inventory
  skills-lock.json                   # Local skills lockfile snapshot
```

Some sources overlap (especially **superpowers**). Copies are kept per install so you can compare versions.

## Counts

See `meta/skill-index.json` for the full list. Snapshot at collection time: **135** `SKILL.md` files across **10** source folders.

## Attribution

Skills retain whatever licenses and notices shipped with their originals (for example under `_package/` or per-skill `LICENSE*`). This repo is a local backup/collection, not a claim of ownership over third-party skill content.

## Usage

Point your agent at individual skill folders, or copy the ones you want into your tool’s skills directory.
