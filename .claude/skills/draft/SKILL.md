---
name: draft
description: Expand the annotated outline into a full article written in the user's voice, learned from their example articles. This is the writing step.
---

# Draft

Write the full article. By now the thinking is done: research, structure, and product
spots are all decided. Your job is to render them in the user's voice.

## Input

- Annotated outline: `content/4-outlines-annotated/{slug}.md`
- The user's voice: `your-setup/brand-and-voice.md` AND, more importantly, the actual
  articles in `your-setup/voice-examples/`.

## How to write in their voice

Do not rely only on the rules. Read the voice examples and match their feel: how they open,
sentence length and rhythm, how they use evidence, their level of formality, their recurring
moves. The examples outrank the written rules when the two disagree.

## Writing approach

- Open with a hook that earns the read, then state the article's promise early.
- Each section leads with its point (inverted pyramid), then supports it.
- Always explain both **what** and **why**, not just instructions.
- Use the internal links from the reference notes.
- Act on the product signposts from the annotated outline, in context, never as a bolt-on.
- Lean on the **proprietary inputs** from the reference notes: original data, the user's POV,
  named examples. These are what make the piece worth reading over a generic AI answer.
- Keep claims concrete. Where you state a fact or number, mark it so `verify-claims` can
  source it. Do not invent statistics.

## Write so answer engines can cite you

- Make the opening sentence of each section a self-contained, quotable answer.
- Define terms plainly on first use, and answer the obvious question directly before adding
  nuance. Clean, extractable passages are what get pulled into ChatGPT, Perplexity, and AI
  Overviews.

## The "average of the internet" test

Before finishing, ask: could the reader get this same article by typing a one-line prompt
into ChatGPT or Google? If yes, it is not worth publishing. A draft that is just the
consensus, with no original data, POV, customer language, or specific example, has failed.
Push it back toward the proprietary inputs and the voice-of-customer material until it says
something only this user could say.

## Hard rules

- Never use em dashes. Use a comma, full stop, or colon.
- Apply every rule and avoided-word from `your-setup/brand-and-voice.md`.

## Output

Write the full draft to `content/5-drafts/{slug}.md`. Hand it to `verify-claims` next.
