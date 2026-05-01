# Paper → Content Pipeline

Transforms an academic or technical research paper into platform-native content across the full repurpose chain. The [[substack]] article is the anchor output — every other platform version is derived from it, not from the raw paper.

Use this pipeline whenever the input is a paper link, arXiv ID, PDF, or paper title rather than a lived experience or opinion take.

---

## Step 0 — Ingest the Paper

**If a URL is provided:**
- Fetch the abstract page first (e.g. arxiv.org/abs/...).
- Then fetch the full-text HTML (e.g. arxiv.org/html/...) with a token limit of 10,000–15,000.
- If rate-limited, fall back to web search using the paper title + year. pull in GitHub repos, blog posts, review snippets.
- Always fetch the official GitHub repo if linked or discoverable — it often contains key implementation detail the abstract omits.

**If a PDF is attached:** read it directly. extract title, authors, abstract, method sections, results tables, and limitations.

**Minimum required before writing:**
- Title, authors, venue/year
- Abstract (complete)
- Core method description
- At least one set of quantitative results with benchmark names and metrics
- At least one stated or inferable limitation

Do not proceed to Step 1 until all five are confirmed.

---

## Step 1 — Internal Explanation Scaffold

Run this before writing any platform content. never skip.

### 1. High-level gist (2–4 sentences)
- What problem does the paper tackle?
- What is the core idea?
- Why does it matter right now?

### 2. Core contributions (3–6 bullets)
Pattern: "They do X so that Y becomes easier / possible / better."
Focus on: new formulations, algorithms, systems, key experiments — not vague claims.

### 3. Method in simple terms
- Problem setup: inputs, outputs, environment, what is optimised.
- Key idea(s): the one or two conceptual moves that make the paper distinctive.
- Step-by-step walkthrough for a typical example run.
- What is actually new vs. prior work and standard baselines.

### 4. Results and evidence
- Which tasks / datasets, which metrics.
- Rough improvement magnitude — no exaggeration.
- Evidence of robustness, transfer, or generality where present.

### 5. Strengths and limitations
- Strengths: formulation quality, system design, result credibility.
- Limitations: narrow evaluation, missing ablations, engineering overhead, partial open-sourcing, replication barriers, compute cost.
- Distinguish paper-stated facts from cautious inference.

### 6. Missing angles
- What was intentionally simplified (math, proofs, implementation depth).
- What a deeper understanding would require.
- Confirm the scaffold is sufficient for a first-pass conceptual read.

---

## Step 2 — Platform Adaptation

Map the scaffold onto the [[repurpose]] chain. the paper is the "idea" — every platform gets a different angle on it, not the same explanation reformatted.

### [[substack]] — anchor output (write first)

Apply the **Research Breakdown** track from [[brand-voice]].

**Length:** 1,200–2,000 words.

**Required sections (H2 headings):**
1. Opening hook — real pain point or observation that makes this paper timely right now.
2. The problem — what's broken or missing in current practice that this paper targets.
3. The core idea — name and explain every key mechanism from the scaffold.
4. How it works in practice — at least one concrete example walkthrough.
5. What the experiments show — tasks, metrics, main findings. cite actual numbers.
6. Who should pay attention — researchers / practitioners / architects / founders.
7. Strengths, limitations, and open questions — candid, non-negotiable. at least two real caveats.
8. Closing + paper link + question to drive comments.

**Voice:**
- First-person authoritative. write as a practitioner peer who read the paper so the reader doesn't have to.
- Concrete numbers over vague claims — every major finding gets a number.
- Anti-hype — never "revolutionary" or "game-changing" without hard evidence.
- Limitations section is non-negotiable. surface at least two meaningful caveats.
- Audience: AI/ML engineers, CTOs, architects, founders. no dumbing-down.
- Apply [[brand-voice]] vocabulary rules. see banned words list.

Use [[substack]] for title / subtitle formulas, SEO standards, visual content standards, and hashtag strategy.

### [[x]] — sharpest failure mode or claim from the paper

One concrete finding or flaw as a thread. hook = the number or claim that changes how you build. thread payoff = the architectural implication.

### [[linkedin]] — practitioner angle

What does this paper mean for someone building production systems today? open with "i read this paper so you don't have to." walk through the one finding that changes a decision they're about to make.

### [[instagram]] — carousel breakdown

Slide 1: bold claim from the paper. Slides 2–7: one finding, concept, or implication per slide. max 30 words per slide. Slide 8: CTA.

### [[youtube]] — full explainer

Cold open: "this paper changes how we should build X." flaw reveal at ~90 seconds. method walkthrough as main content. postmortem energy: what breaks if you implement this today?

### [[tiktok]] — one surprising result

45–60 second script. hook = the number that shocked you. show the table or figure if possible. close with the implication.

### [[threads]] — casual reaction post

Your honest take after reading. "just read [paper]. here's what actually matters." 1–3 short posts, under 500 chars each.

### [[facebook]] — community discussion

What does this mean for builders in this space? frame as an open question inviting debate. close with a specific question.

---

## Step 3 — Hallucination Red-Flag Check

Run internally before outputting any platform version. if any flag triggers, revise first.

**Flag if:**
- A claim, benefit, or conclusion not supported by the paper is included.
- Narrow / limited experimental results are presented as universal guarantees.
- Human-like understanding, agency, or intent is implied in models or systems.
- Future impact is predicted beyond cautious, evidence-based statements.
- No meaningful limitation or uncertainty is surfaced.

If a red flag cannot be avoided (e.g. the paper itself is speculative), name it explicitly in the rubric reasoning.

---

## Step 4 — Rubric Evaluation

Score every Substack output on these six dimensions (integers 1–5 each).

| Dimension | What it measures |
|---|---|
| Accuracy | Faithfulness to paper; no unsupported claims; correct emphasis |
| Readability | Clarity for the TNB audience (builders, engineers, founders) |
| Structure | Logical flow; good use of sections and transitions |
| Analogy | Effective use — or intentional non-use — of analogies and concrete examples |
| Limits & Uncertainty | How well limitations and caveats are surfaced |
| Educational Value | How much a motivated reader genuinely learns |

**Acceptable threshold:** total ≥ 26/30.

If total < 26 or red-flag check fails: revise, then re-output and recompute. only present output where total ≥ 26 AND red-flag status = Pass.

**Append this block at the end of every Substack output:**

```
---
## Rubric Report

- Accuracy: X/5
- Readability: X/5
- Structure: X/5
- Analogy: X/5
- Limits & Uncertainty: X/5
- Educational Value: X/5
- Total Score: X/30
- ACCEPTABLE SCORE: Yes/No
- HALLUCINATION RED-FLAG CHECK STATUS: Pass/Fail
- Rubric reasoning: <3–6 sentences>
```

---

## TNB Research Breakdown Voice

When writing from a paper, the [[brand-voice]] Research Breakdown track applies:

- **builder story** = your reason for reading the paper. what decision or system problem made you pick it up.
- **the pattern everyone is copying** = what the field currently assumes or uses that this paper challenges.
- **architecture flaw** = the gap between what the paper claims and what production would reveal. always answer: "what breaks if you implement this today?"
- **corrected architecture** = what the fix actually looks like. trade-offs documented, not glossed over.

The paper is the source material, not the story. *you* are still the narrator.

---

## Output Rules

- return only the platform-appropriate content + rubric report block (for substack).
- no meta-commentary about the pipeline itself.
- no preamble ("here is the article") — start directly with the content.
- paper link always included at the bottom of the substack article.
- apply [[humanizer]] before marking any output ready.
