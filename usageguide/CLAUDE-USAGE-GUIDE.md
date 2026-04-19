# Claude Code Usage Guide for This Project

This project is a markdown-based content skill graph designed to work especially well with Claude Projects or Claude Code workflows.

## What You Built

You now have a reusable content engine with:
- platform playbooks
- voice system files
- hook library
- repurposing workflow
- scheduling rules
- audience segmentation

## Best Way to Use in Claude

### Option 1: Claude Project
1. Create a new Claude Project.
2. Upload the full `content-skill-graph` folder.
3. Keep `index.md` as the starting instruction source.
4. Add one topic per prompt.
5. Ask Claude to follow the node links before generating content.

Suggested prompt:

```text
Use the uploaded content skill graph.
Start from index.md.
Follow all relevant linked nodes.
Create platform-native content for this topic: [YOUR TOPIC].
Do not reformat the same post for every platform.
Rethink the angle, hook, tone, and structure for each platform.
Return outputs for X, LinkedIn, Instagram, TikTok, YouTube, Threads, Facebook, and Newsletter.
```

### Option 2: Claude Code
If you're using Claude Code against a local repo:

```bash
cd content-skill-graph-project
```

Then prompt Claude Code like this:

```text
Read content-skill-graph/index.md first.
Then traverse all linked markdown files that matter for the topic "[YOUR TOPIC]".
Generate 8 platform-native content assets using the repurpose chain.
Save the outputs in a new folder called outputs/[topic-slug]/
Create one markdown file per platform.
```

## Recommended Workflow

### Weekly batch workflow
1. Pick 2-3 content topics.
2. Run Claude once per topic.
3. Save outputs into topic-specific folders.
4. Review hooks first.
5. Edit brand voice examples based on best performers.
6. Update `hooks.md` every week.

## Example Claude Code Tasks

### Generate one full batch
```text
Read the content skill graph and generate a full weekly batch for these topics:
1. how to automate lead gen with AI
2. why most creators fail at repurposing
3. building a solo content engine
Save each topic to outputs/ with separate files per platform.
```

### Improve voice
```text
Review brand-voice.md and platform-tone.md.
Strengthen them for a founder audience in AI automation.
Keep the tone practical, direct, and proof-driven.
Rewrite only where needed.
```

### Add a new platform
```text
Create a new platform node for Reddit.
Match the existing folder style.
Then update index.md, repurpose.md, and scheduling.md to include it.
```

## Suggested Repo Structure After You Start Using It

```text
content-skill-graph-project/
├── content-skill-graph/
├── outputs/
│   ├── ai-lead-gen-system/
│   │   ├── x.md
│   │   ├── linkedin.md
│   │   ├── instagram.md
│   │   └── ...
│   └── creator-repurpose-engine/
└── CLAUDE-USAGE-GUIDE.md
```

## Important Tips
- Keep `index.md` as your orchestration file.
- Keep examples inside each file realistic and niche-specific.
- Do not overstuff every markdown file with too much theory.
- Add real winning hooks to `hooks.md` from your own account data.
- Refine `brand-voice.md` after seeing 10-20 generated batches.
- Keep the graph modular: one idea per file.

## Fast Start Prompt

```text
Read content-skill-graph/index.md.
Use it as the control center.
Follow the linked markdown files needed for this topic: "[YOUR TOPIC]".
Generate unique, native content for each platform in the repurposing chain.
Use the brand voice and audience rules.
Make every platform version feel original.
```
