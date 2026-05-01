---
name: humanizer
version: 2.5.1
description: |
  Remove signs of AI-generated writing from content output. Apply after any
  platform post or newsletter draft is written. Detects and fixes patterns
  including: inflated significance, promotional language, superficial -ing
  phrases, vague attributions, em dash overuse, rule of three, AI vocabulary
  words, passive voice, negative parallelisms, and filler phrases.
source: uploaded SKILL.md (humanizer v2.5.1)
applies-to: all platform outputs, all newsletter drafts
---

# Humanizer: Remove AI Writing Patterns

This skill strips AI writing patterns from any content produced by the engine.
Apply it as a final pass after [[repurpose]] produces platform drafts.

It is based on Wikipedia's "Signs of AI writing" guide maintained by WikiProject AI Cleanup.

---

## When to use

Apply this skill:
- After any platform post is drafted (LinkedIn, Substack, X, Instagram captions, etc.)
- Before any content is marked "ready to publish"
- When reviewing older content that sounds flat or assembled

---

## The process

1. Read the draft carefully
2. Identify all AI pattern instances (see categories below)
3. Rewrite each problematic section
4. Check that revised text:
   - Sounds natural read aloud
   - Varies sentence length naturally (short and punchy mixed with longer)
   - Uses specific details over vague claims
   - Matches the [[brand-voice]] register for the platform
5. Run the audit loop:
   - Ask: "What makes this obviously AI generated?" — list the remaining tells
   - Rewrite to eliminate those tells
6. Present: draft → audit bullets → final version

---

## Core patterns to catch

### Content patterns

**Significance inflation** — words like "pivotal", "landmark", "testament", "underscores", "reflects broader", "enduring". Cut or replace with a specific fact.

**Promotional language** — "groundbreaking", "nestled", "vibrant", "breathtaking", "showcasing", "boasts". Replace with direct description.

**Superficial -ing phrases** — "highlighting...", "symbolizing...", "contributing to...", "fostering..." tacked onto sentences to fake depth. Remove them. The sentence ends where the thought ends.

**Vague attributions** — "experts argue", "industry observers", "some critics". Name the source or cut the claim.

**Formulaic challenges sections** — "Despite X challenges... continues to thrive." Cut the whole section or replace with one specific fact.

---

### Language patterns

**AI vocabulary** — additionally, align with, crucial, delve, emphasizing, enduring, enhance, fostering, garner, highlight (verb), intricate, key (adjective), landscape (abstract), pivotal, showcase, tapestry (abstract), testament, underscore, valuable, vibrant. Replace with plain words.

**Copula avoidance** — "serves as", "stands as", "marks a", "boasts". Replace with "is" or "are".

**Negative parallelisms** — "It's not just X; it's Y." Cut or flatten.

**Rule of three overuse** — forced triads everywhere. Break one. Let the list be two things or four.

**Synonym cycling** — protagonist → main character → central figure → hero. Pick one word and use it.

---

### Style patterns

**Em dash overuse** — replace most with commas, periods, or parentheses.

**Bold mid-text** — remove bold emphasis from body text unless it's a platform convention (it usually isn't).

**Inline-header lists** — "- **Speed:** Code is faster..." → convert to prose or a plain list without bold headers.

**Title Case headings** — use sentence case. "The architecture flaw" not "The Architecture Flaw".

**Emojis on headings/bullets** — remove unless the platform explicitly uses them (only Instagram).

---

### Communication patterns

**Chatbot artifacts** — "Great question!", "I hope this helps!", "Let me know if you'd like me to expand" → cut entirely.

**Sycophantic tone** — "You're absolutely right", "That's an excellent point" → cut.

**Knowledge-cutoff disclaimers** — "As of my last training update..." → cut.

---

### Filler and hedging

**Filler phrases** → replace:
- "In order to achieve this" → "To achieve this"
- "Due to the fact that" → "Because"
- "At this point in time" → "Now"
- "It is important to note that" → delete the phrase, keep the fact
- "The system has the ability to" → "The system can"

**Excessive hedging** — "could potentially possibly be argued that... might" → "may"

**Generic positive conclusions** — "The future looks bright. Exciting times lie ahead." → replace with one specific, concrete next step or just end the piece.

**Signposting** — "Let's dive in", "Let's explore", "Here's what you need to know" → delete. Start with the actual content.

---

## TNB-specific additions

Beyond the Wikipedia patterns, apply these TNB voice checks:

- Does the piece have a real opinion or just neutral reporting? Add one.
- Does the closer feel assembled or human? If it's a kicker-aphorism, loosen it.
- Are the section headers sentence-case and lowercase where appropriate?
- Is there at least one moment of genuine uncertainty or complexity acknowledged?
- Does the first line work as a standalone hook, or does it need the second line to make sense?

---

## Output format

1. Draft (the AI-generated content)
2. "What makes this obviously AI generated?" — brief bullets, 3-6 tells
3. Final version (rewritten after the audit)
4. Optional: brief summary of changes (useful for teaching the system what patterns keep appearing)

---

## Reference

Based on [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), WikiProject AI Cleanup.

Key principle: "LLMs use statistical algorithms to guess what should come next. The result tends toward the most statistically likely result that applies to the widest variety of cases."

That's the problem. A skill graph narrows the statistical field. The humanizer catches what still slips through.
