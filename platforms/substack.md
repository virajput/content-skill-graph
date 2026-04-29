# Substack

## Platform DNA
- Substack post app and email-based. you own the audience (no algorithm to fight)
- 1,000-2,000 words per issue. deep-dive format
- Vibe: direct, personal. like a letter from a friend whos also your mentor. most personal of all platforms

## Content Rules
- Subject line = your hook. use [[hooks]] adapted for email. "The system that replaced my $8k/mo content team" not "Weekly Substack #47"
- Open with a story or personal observation, then transition to the tactical stuff
- One core topic per issue. dont try to cover everything
- Match [[brand-voice]] at its most personal. see [[platform-tone]]
- End with ONE clear CTA. reply to the email, check out a resource, or try something specific
- Plain text or minimal design. fancy templates look like marketing spam. plain text looks like a real person

## Repurposing
- Deepest version of your weekly best topic
- Combine the [[x]] take + [[linkedin]] narrative + exclusive insights not shared on social
- This is where you go deep on the "how" behind your posts
- See [[repurpose]]

---

## Title + Subtitle Formulas

The title is the most important SEO and open-rate lever on Substack. It doubles as the OG title and email subject line. Get this right before writing anything else.

### Title Formulas That Work for TNB

**Confession + Flaw reveal** (highest open rate for postmortem track)
`"I [built/shipped/designed] [thing I was proud of]. [Outcome that challenges that pride]."`
- Example: "I Built a Content System I Was Proud Of. Then I Audited It."

**Universal flaw naming** (best for architecture deep-dive track)
`"Every [category of system] Has This [named flaw]. [Personal acknowledgement]."`
- Example: "Every 'Smart' AI System Has This Architectural Flaw. Mine Did Too."

**Direct diagnosis** (works when the flaw has a name worth front-loading)
`"The [named flaw]: Why [consequence that reader fears]"`
- Example: "The Write-Back Loop: Why Every AI Pipeline You've Built Is Getting Dumber"

**Audit frame** (strong for investigative pieces with data/projections)
`"I Audited [system]. Here's [the finding that changes how you build]."`
- Example: "I Audited My Own Content System. Here's the Architecture That Would've Killed It."

**Frozen system reveal** (for any piece about static vs. learning systems)
`"Your [AI system] Is Not [what you think it's doing]. It's [what it's actually doing]. Here's Why."`
- Example: "Your AI Pipeline Is Not Learning. It's Frozen. Here's Why."

### Subtitle Formulas

The subtitle delivers the specificity signal and the promise. It is read by the subscriber on the web version, in search results, and in the Substack app. Keep it under 160 characters.

**Architecture track:** `"[What the piece diagnoses] — [method of analysis] with [what the reader leaves with]"`
- Example: "How a missing feedback loop silently degrades every context-injection AI pipeline — full architecture audit with performance projections and fix estimates"

**Postmortem track:** `"[The system]. [What I did to it]. [What I found that you need to know.]"`
- Example: "A markdown-based AI content system. A full audit. The structural gap hiding inside every workflow that 'works.'"

**Research/framework track:** `"[The structural problem]. [Where it hides]. [The decision framework for fixing it.]"`

### Title + Subtitle Pairings — Recommended for "Content Skill Graph Audit" Issue

**Option A** — Recommended (Architecture Deep-Dive track, highest fit with TNB voice)
- Title: `Every "Smart" AI System Has This Architectural Flaw. Mine Did Too.`
- Subtitle: `How a missing write-back loop silently degrades every RAG-based pipeline — architecture audit, performance projections, and fix probability estimates.`

**Option B** — Stronger for cold discovery (sharper hook for non-subscribers)
- Title: `Your AI Pipeline Is Not Learning. It's Frozen.`
- Subtitle: `The write-back loop problem: why context-injection AI systems plateau at Month 3 and degrade by Month 6 — and the architecture that closes the loop.`

**Option C** — Postmortem register (best if this issue follows a previously shared build)
- Title: `I Audited My Own Content System. Here's What Would've Killed It by Month 6.`
- Subtitle: `A full architecture analysis of a markdown-based AI content engine — with failure mode breakdown and fix probability estimates for each structural gap.`

**Recommendation:** Option A for the primary issue. Option B if A/B testing open rates on a future repromote or republish.

---

## SEO Standards

Apply these to every Substack issue. The goal: discoverable via search, shareable via social, and optimised for Substack's native recommendation engine — in that priority order.

### Slug Rules
- Format: kebab-case, no stop words, no date stamp
- Length: under 60 characters
- Structure: `[primary-keyword-cluster]-[argument-signal]`
- The slug should read as a sentence fragment that communicates the post's argument, not just its topic
- Example pattern: `ai-content-system-write-back-loop-failure` (43 chars) — topic cluster first, argument last

### Meta Description Rules
- Length: 150–160 characters exactly. Count before publishing.
- Structure: `[primary keyword or flaw name as opener]. [method/scope signal]. [specificity marker that separates this from generic commentary].`
- Front-load the primary keyword or named flaw — this is what search surfaces
- End with a specificity signal: numbers, named methods, or scoped claims ("performance projections", "fix probability estimates", "3 failure modes") — these distinguish the piece from think-pieces
- Never: vague promises ("you'll learn", "discover how"), corporate language, or restatements of the title

### Primary Keyword Selection
- 2–4 words, informational intent (not commercial)
- Must match the search mode of the target reader: investigational ("why does my AI system degrade") not transactional ("buy AI content tool")
- Test: would a builder searching this phrase be the right reader for this piece? If yes, it's the right keyword.
- TNB primary keywords tend to follow the pattern: `[adjective] [AI system type]` or `[AI system type] [failure mode]`

### Secondary Keywords (5–8 per issue)
- Ordered by relevance to the specific argument, not by search volume
- Include at least 2 long-tail terms (5+ words) — these are low-competition and capture the highest-intent readers
- Flag niche/low-competition terms vs. broader category terms — both have a role but serve different discovery functions
- Niche terms anchor the piece's technical specificity; broad terms extend its discovery ceiling

### Open Graph Metadata
- OG Title: mirror the post title exactly
- OG Description: 1–2 sentences written for social sharing context, NOT for search
  - Use "I" voice (matches the newsletter's register)
  - Name the system, the finding, and the implication — in that order
  - End with "you" to create reader identification: "...and that's the flaw inside every pipeline you've built too"
  - OG description and meta description must be different texts. One is for search intent; one is for social curiosity.

### Substack Preview Text
- Substack auto-pulls the first 1–2 sentences as preview text in email and the app
- Rule: the first sentence must create a gap (story, confession, surprising fact) without giving away the flaw
- Rule: the second sentence must deliver enough context that the reader understands what the piece is about
- Avoid: opening with a question, a statistic without context, or a heading-style declaration — these flatten the personal register
- Test: read the first two sentences cold. Does the reader know who is speaking, what they built, and that something unexpected happened? If yes, the preview pulls correctly.

---

## Visual Content Standards

Every Substack issue should have a cover image and 2–4 section visuals where they earn their position. Visuals must do argumentative work — not decorate.

### Content Track → Palette Mapping

Identify the content track before specifying any visual. The palette follows the track.

| Track | Background | Accent | Text |
|-------|------------|--------|------|
| Research Breakdown | `#FFFBEE` | `#F5C518` | `#7A6010` |
| Production Post-Mortem | `#FFF3EE` | `#E8703A` | `#A03800` |
| Architecture Deep-Dive | `#EFF6FF` | `#2E72C4` | `#0D2A5A` |
| Enterprise AI Strategy | `#F3F0FF` | `#6B5DD3` | `#221A5A` |

Universal colours applied in every diagram regardless of track:
- Ink / border: `#1A1A18`
- Image background: `#F1F3F4`
- Neutral fill (inactive nodes): `#EDE7D9`
- Body text: `#4A4640`
- Muted captions: `#8A847C`

### Cover Image Standards
- Dimensions: 1200 × 628px (Substack / Open Graph standard)
- Concept: communicate the piece's central argument as a visual metaphor — not the topic, the *argument*
- Style: engineering whiteboard register. Flat nodes, clean lines, no gradients, no drop shadows. Generous whitespace.
- The cover serves three simultaneous placements: Substack post header, Open Graph card for all social shares, email thumbnail — design for all three at once
- Never use: shield iconography, padlock imagery, red/green binary matrices, stock photo people, circuit-board decorative elements. This audience has seen those thousands of times.
- Tools (ranked): Figma → Excalidraw → SVG direct

### Section Visual Rules
- A visual earns its position only if it does something the prose cannot: crystallises a relationship, makes an abstraction concrete, or provides a reference point the reader carries into subsequent sections
- Do not add visuals to: opening story sections (breaks narrative register), closing CTAs (breaks the reflective close), or sections where a table or code block already anchors the content
- Architecture and flow diagrams: build as reusable Figma components. The same node set should appear across 2–3 sections with progressive modification (standard → broken → fixed). This teaches the architecture visually as the argument unfolds.
- Production priority order: (1) cover image — highest reuse across placements; (2) the diagram at the argumentative core — where the central claim lands; (3) the corrected/fixed diagram — the reader's takeaway; (4) setup diagrams

### Platform Crop Notes
- LinkedIn square (1080 × 1080px): centre the core diagram element; move headline text to top third; ensure the key visual detail (gap, missing arrow, flaw marker) is not cropped
- Twitter/X card: Substack generates this automatically from the cover image via Open Graph tags. Confirm `twitter:card = summary_large_image` is set (default for Substack). No separate crop required if cover image is set.

---

## Hashtag Strategy (Substack Tags)

Substack tags feed the recommendation engine and topic browsing. Maximum 5 tags per issue.

### Rules
- Only use tags with sufficient critical mass on Substack to surface the piece in Browse
- Tags must match the piece's actual content — do not tag for reach if the reader who finds you via that tag will immediately unsubscribe
- Avoid over-specific tags with no browsing audience on Substack (e.g., "Write-Back Loop" has no Substack browsing mass even if it's the right keyword)

### TNB Tag Set — Architecture / AI Engineering Pieces
| Tag | Role |
|-----|------|
| AI | Highest-volume Substack topic. Base discoverability layer. Required for all TNB issues. |
| Technology | Second-tier broad reach. Captures non-specialist builders via Substack's cross-recommendation layer. |
| Software | Technical builder audience. Medium volume, high intent. Readers who finish 2,000-word architecture pieces. |
| Productivity | Automation / efficiency angle. Broadens reach without misrepresenting TNB content. |
| Startups | Indie hackers, solo operators, founders. High conversion to subscribers for TNB. |

Swap **Productivity** for **Marketing** when the piece has significant content strategy weight (audience will be larger and less technical but genuinely served by the content).
Swap **Software** for **Entrepreneurship** when the piece is Enterprise AI Strategy track (decision-maker audience, not developer audience).
