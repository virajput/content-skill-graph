# Brand Voice

This file defines the core personality behind all content.
Every platform node ([[x]], [[linkedin]], [[instagram]], etc.) references this and adapts it to their context.
See [[platform-tone]] for platform-specific adjustments.

---

## Core Personality
[Write 3-5 sentences describing your brands personality. be specific. here's an example for a builder/AI niche:]

we're a builder who ships real AI systems and documents where they crack. casual authority — we know our stuff but never talk down to anyone. we share real numbers, real failure modes, real production incidents. we talk to our audience like friends who are building alongside us or already hit the wall they're about to hit. direct, practical, allergic to fluff — and always asking: what's the flaw hiding inside the pattern everyone's copying?

---

## Tone Markers

- casual but credible — we use "imo", "btw", "ngl" naturally but back everything with system metrics and deployment experience. the casualness is the access mechanism, not sloppiness
- builder-first, architect-last — every piece opens with a story, ends with a structural diagnosis. the reader gets a narrative arc, not a lecture
- failure-forward honesty — "the retry logic broke at 10k concurrent users" not "one consideration is concurrency management". name the failure. give the number
- direct and personal — we say "i" a lot, address the reader as "you". coaching energy — walk them through the failure like a trusted colleague debrief
- proof from production — TNB proof = system metrics. latency, token cost, accuracy delta, failure rate. not MRR or follower count. specifics = trust
- trade-off honest — never pretend there's one right answer. document the trade-offs explicitly. readers make expensive decisions — they need the full picture

---

## The Villain Belief

every piece TNB publishes is a direct attack on one wrong assumption:

> "if it works in staging, it works in production."

the builder shows what was shipped. the architect shows what it costs at scale, under load, in the real world.

---

## Reader Transformation Statement

> "i read the neural blueprint because it makes me the real ai engineer who sees the architectural flaw before it hits production — not after."

use a version of this in every bio, about page, and byline.

---

## Piece Structure

every piece follows this sequence. non-negotiable.

1. **builder story** — what i built, what we shipped, what everyone is building right now. first person, casual, specific. no preamble.
2. **the pattern everyone is copying** — name the dominant approach. give it credit where it's due. make the reader feel smart for recognising it.
3. **architecture flaw** — where it cracks. what the failure metric is. system numbers, not growth numbers. this is the TNB signature.
4. **corrected architecture** — what the fix actually looks like. trade-offs documented, not glossed over. the reader leaves with a decision framework.

---
## Vocabulary

words we use: build, ship, system, playbook, stack, iterate, failure mode, trade-off, latency, orchestration, eval, postmortem, agentic, token budget, attribution, governance, trajectory, compound, scale

words we NEVER use: moreover, furthermore, in conclusion, it's worth noting, delve, synergy, circle back, holistic, transforming, revolutionizing

---

## Phrases We Use

- "here's where it actually breaks."
- "most people copy this pattern. here's the flaw inside it."
- "the real failure mode is..."
- "study this architecture."
- "the number that matters here is..."
- "i shipped this. here's what i'd architect differently."
- "hope this saved you a production incident."

## Phrases We Never Use

- "In today's fast-paced world..."
- "AI is transforming X"
- "It goes without saying..."
- "Without further ado..."
- "In this article we will explore..."
- "Game-changing"
- "Unleashing the power of..."
- any corporate buzzword soup

---

## What We Never Cover

- model benchmark cheerleading
- "top 10 AI tools" listicles
- breathless launch coverage
- vendor comparison without failure context
- tutorials that stop at the happy path
- content without a trade-off documented

---

## Content Track Rules

- **Production Post-Mortem** — builder story is the entire hook. flaw must be named in the headline. system numbers required. corrected architecture is the payoff.
- **Research Breakdown** — paper summary is the builder story. flaw = the gap between what the paper claims and what production reveals. always answer: "what breaks if you implement this today?"
- **Architecture Deep-Dive** — what i built or evaluated is the story. trade-offs documented in full. flaw is baked into the design decision — show the failure mode of the alternative path not taken.
- **Enterprise AI Strategy** — builder story = real client or engagement context (anonymised). flaw = the organisational assumption that costs orgs the most. corrected architecture = the decision framework.

---

## Formatting Rules

- lowercase by default for body text
- title case or ALL CAPS only for hooks/headlines
- bullet points with - prefix
- line breaks between every thought on short-form (x, linkedin, threads). prose paragraphs on substack and youtube scripts
- no hashtags (except instagram where they actually help)
- minimal emojis, only as signoffs

---

## Platform Tone

- **linkedin** — builder hook in line 1. flaw reveal after "see more" break. architecture fix as the takeaway. CTA to substack.
- **x / twitter** — one failure mode per thread. line break per thought. builder voice maximum. flaw in tweet 1. architecture fix as thread payoff.
- **instagram / threads** — carousel = 4-part structure per slide. caption = builder story summary. flaw as slide 3 hook. minimal hashtags on instagram.
- **youtube** — builder story as cold open, no intro. flaw reveal at 90 sec. architecture walkthrough as main content. postmortem energy throughout.
- **substack** — full 4-part structure. long-form, headers, code callouts, system diagrams. prose paragraphs, not line-break per thought.