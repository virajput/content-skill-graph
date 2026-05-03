# skillgraph/

Standalone Obsidian vault and content production system for **The Neural Blueprint** brand. Converts one topic into 8–10 platform-native posts. Lives in its own git repo (separate `.git`). Does **not** share database tables, Python code, services, or Celery workers with the main SocialHub app.

## Vault Structure

| Path | Purpose |
|------|---------|
| `index.md` | Control center — start every session here |
| `platforms/` | Per-platform playbooks: `x.md`, `linkedin.md`, `instagram.md`, `tiktok.md`, `youtube.md`, `threads.md`, `facebook.md`, `substack.md` |
| `voice/brand-voice.md` | Core personality, tone markers, vocabulary — applies to ALL platforms |
| `voice/platform-tone.md` | How the core voice adapts per platform |
| `engine/hooks.md` | Scroll-stopping opener formulas by type — read before writing any post |
| `engine/repurpose.md` | 1 idea → 10 outputs production chain and platform order |
| `engine/scheduling.md` | Posting calendar, best times, batch workflow |
| `engine/content-types.md` | Format definitions per platform |
| `engine/humanizer.md` | Final QA pass — strips AI writing patterns before publishing |
| `engine/paper-to-content.md` | Research paper → platform content pipeline (separate flow) |
| `audience/builders.md` | Primary audience: indie hackers, AI engineers, SaaS founders |
| `audience/casual.md` | Secondary audience: AI-curious, not yet building |

## Execution Flow (standard topic)

1. Read `index.md` — follow all linked nodes relevant to the topic.
2. Check topic alignment with niche (AI architecture, builder focus). Reject if off-niche.
3. Read `voice/brand-voice.md`.
4. Read `engine/hooks.md` — select the strongest hook formula.
5. Read `engine/repurpose.md` — follow the platform chain order.
6. Write for the **first platform in the chain** (usually X). Then adapt — don't reformat, **rethink angle, hook, structure** per platform.
7. Apply `engine/humanizer.md` to every output as the final pass.

For a **research paper input**, follow `engine/paper-to-content.md` instead — Substack is the anchor output.

## Key Rules

- IMPORTANT: Outputs are NOT reformatted copies. Each platform gets a different angle, hook, tone, and structure on the same topic.
- IMPORTANT: Run `engine/humanizer.md` on every output — it is the mandatory final QA step.
- For paper inputs: only publish Substack if the rubric score ≥ 26/30 and hallucination check = Pass.

## Isolation

This is a pure-markdown Obsidian vault. There is no Python, no Flask, no Celery, and no shared Supabase tables. Changes here affect content generation only. Commit separately — this repo has its own `main` branch and remote.
