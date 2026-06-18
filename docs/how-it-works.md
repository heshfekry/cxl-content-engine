# How it works

This engine copies how a good content team actually works, and hands each part to a small,
focused skill. Understanding the ideas behind it will help you get more out of it and shape
it to how you work.

> The structure here is based on Ryan Law's content-engineering system at Ahrefs, then
> upgraded for new users and B2B marketing. For the full story see
> [how-this-was-made.md](how-this-was-made.md).

## The seven ideas it is built on

**1. Chain small skills, do not use one big prompt.**
Each step (research, outline, draft, and so on) is its own skill with one job. Chained
together by `/blog-pipeline`, they take a keyword to a finished draft. You can also run any
one on its own.

**2. Save the output of every step.**
If the final article is off, you do not start over. You open the saved file from each step,
find where it went wrong, fix that step, and continue from there. Every step writes to the
`content/` folder for exactly this reason.

**3. Keep skills lean, and test them.**
Modern models are good. Sometimes a long, detailed skill produces worse results than a short
one. When a step underperforms, try simplifying its `SKILL.md`. Shorter is often better.

**4. Give it good data from good sources.**
The engine works on built-in web search, and gets sharper if you connect tools like Ahrefs
or Search Console. Either way, it is told never to invent numbers. Real data in, real
content out.

**5. Front-load your direction.**
A few sentences of steering at the start shape the whole article. That beats heavy editing
at the end. See [../inputs/context-example.md](../inputs/context-example.md).

**6. Review in a readable preview.**
Reading raw markdown hides problems. The `preview` step renders the article as a styled web
page so you read it the way a reader will.

**7. Fork and personalise.**
There is no single right way to make content. This is a starting point. Rename skills, add
steps, remove ones you do not use, change the data sources. The more it reflects how you
work, the better it gets.

## The pipelines and commands

- **Creation:** `/blog-pipeline "keyword"` runs (optional) voice-of-customer-mining,
  research, answer-engine-audit, your-reference, outline, product-mentions, draft,
  verify-claims, (optional visuals), and preview.
- **Update:** `/update-pipeline "url"` runs extract, guidance, answer-engine-audit, the three
  audits (claims, product mentions, topic gaps), update-draft, and a side-by-side diff preview.
- **Brand page:** `/llms-brand-page` builds an LLM-readable brand page so answer engines
  describe you accurately. Run it once, then refresh when your offer changes.

## What it is good for, and what it is not

It shines on straightforward, well-trodden topics where the value is doing the legwork well:
researching, structuring, drafting, and keeping a library current. It is not built to
replace genuinely original thinking, strong opinions, or first-hand experience. Use it to
clear the drudgery so you can spend your effort on the work that needs you.
