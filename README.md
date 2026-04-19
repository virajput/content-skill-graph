# Content Skill Graph

Based on: [https://x.com/DeRonin_/status/2042604279077237170?s=20]

A markdown-based content production system for **The Neural Blueprint** — turns one topic into 8 platform-native posts that each think about the topic differently.

## What It Does

Feed Claude one idea. Get back ready-to-publish content for X, LinkedIn, Instagram, TikTok, YouTube, Threads, Facebook, and Substack — each with its own angle, hook, tone, and structure. Not reformatted copies. Rethought originals.

## Vault Structure

```
content-skill-graph/
├── index.md              ← control center, start here
├── platforms/            ← per-platform playbooks (format, frequency, tone)
│   ├── x.md
│   ├── linkedin.md
│   ├── instagram.md
│   ├── tiktok.md
│   ├── youtube.md
│   ├── threads.md
│   ├── facebook.md
│   └── substack.md
├── voice/
│   ├── brand-voice.md    ← core personality, tone markers, vocabulary
│   └── platform-tone.md  ← how core voice adapts per platform
├── engine/
│   ├── hooks.md          ← scroll-stopping opener formulas by type
│   ├── repurpose.md      ← 1 idea → 10 outputs production chain
│   ├── scheduling.md     ← posting calendar, best times, batch workflow
│   └── content-types.md  ← format definitions per platform
├── audience/
│   ├── builders.md       ← primary: indie hackers, AI engineers, SaaS founders
│   └── casual.md         ← secondary: AI-curious, not yet building
└── usageguide/           ← how to use this with Claude Projects or Claude Code
```

## Installation

### Prerequisites

- [Obsidian](https://obsidian.md/) (free) — for browsing and editing the vault locally
- A Claude account — either [Claude.ai](https://claude.ai) (Projects) or [Claude Code](https://claude.ai/code) (CLI)

### Clone the repo

```bash
git clone https://github.com/virajput/content-skill-graph.git
cd content-skill-graph
```

### Open in Obsidian

1. Open Obsidian → **Open folder as vault**
2. Select the `content-skill-graph/` directory
3. Trust the plugins when prompted (Dataview, Templater, Calendar are pre-configured)

That's it — no build step, no dependencies to install. The vault is ready to use.

---

## Quick Start

### Option 1: Claude Project (recommended for beginners)

1. Create a new Claude Project at [claude.ai](https://claude.ai)
2. Upload this entire folder (or sync via Google Drive / Dropbox)
3. Use this prompt:

```
Use the uploaded content skill graph.
Start from index.md.
Follow all relevant linked nodes.
Create platform-native content for this topic: [YOUR TOPIC].
Do not reformat the same post for every platform.
Rethink the angle, hook, tone, and structure for each platform.
Return outputs for X, LinkedIn, Instagram, TikTok, YouTube, Threads, Facebook, and Newsletter.
```

### Option 2: Claude Code (local, most powerful)

Install Claude Code if you haven't:

```bash
npm install -g @anthropic-ai/claude-code
```

Then open the vault directory in your terminal:

```bash
cd content-skill-graph
claude
```

Paste this prompt:

```
Read index.md first.
Traverse all linked markdown files relevant to the topic "[YOUR TOPIC]".
Generate 8 platform-native content assets using the repurpose chain.
Save outputs in outputs/[topic-slug]/ with one markdown file per platform.
```

Outputs land in `outputs/[topic-slug]/` — one `.md` file per platform, ready to copy-paste.

### Option 3: Copy-paste into any Claude chat

No install needed. Open `index.md`, copy its contents, paste it into Claude with your topic appended:

```
[paste index.md contents here]

Topic: [YOUR TOPIC]
Generate platform-native content for all 8 platforms.
```

## Recommended Weekly Workflow

1. Pick 2–3 content topics
2. Run Claude once per topic
3. Save outputs into `outputs/[topic-slug]/`
4. Review and pick the strongest hooks
5. Update `engine/hooks.md` with winners from your actual account data
6. Refine `voice/brand-voice.md` after every 10–20 batches

## Brand Context

- **Brand:** The Neural Blueprint
- **Niche:** AI architecture for AI builders navigating expensive system decisions — told through the lens of failure, not success
- **Mission:** One topic, 10 platform-native posts, each thinking differently about the same idea

## Key Rules

- Every post must be platform-native — not a copy-paste with minor edits
- Check topic alignment with niche before generating
- Hook selection drives everything — read `engine/hooks.md` first
- Follow the repurpose chain order defined in `engine/repurpose.md`
