# Content Skill Graph

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

## Quick Start

### Option 1: Claude Project

1. Create a new Claude Project
2. Upload this entire folder
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

### Option 2: Claude Code (local)

```bash
cd content-skill-graph
```

Then prompt:

```
Read index.md first.
Traverse all linked markdown files relevant to the topic "[YOUR TOPIC]".
Generate 8 platform-native content assets using the repurpose chain.
Save outputs in outputs/[topic-slug]/ with one markdown file per platform.
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
