# The Content Engine

This is a content writing system you run on your own computer. You give it a topic
or keyword, and it works through the same steps a senior content team would: research,
outline, draft in your voice, fact-check, and hand you a finished article ready to review.

It runs inside a free tool called Claude Code. You do not need to know how to code.
You type plain English.

## What you can do with it

- Take a keyword and get a publish-ready first draft in about ten minutes.
- Refresh and update articles you have already published.
- Make every article sound like **you**, by teaching it from your own best writing.
- See every step of the work, so you can fix the one part that went wrong instead of starting over.

## The one rule: set it up first

This engine ships with **placeholder** brand, voice, and product information. It will
not write good content until you replace those placeholders with your own.

You do not edit files by hand. You run one guided command and answer some questions:

```
/setup
```

If you try to run the engine before setup is done, it will stop and remind you. That is
on purpose.

## How to install it

Pick your computer and follow the steps. They assume you have never used GitHub,
VS Code, or Claude Code before, and explain every click.

- **Mac:** open [START-HERE-MAC.md](START-HERE-MAC.md)
- **Windows:** open [START-HERE-WINDOWS.md](START-HERE-WINDOWS.md)

## After setup, your first article

In Claude Code, type:

```
/blog-pipeline "your keyword here"
```

That runs the whole pipeline. Want to update an existing article instead?

```
/update-pipeline "https://your-site.com/the-article-to-refresh"
```

## Learn how it works

- [docs/how-it-works.md](docs/how-it-works.md) explains the thinking behind the system.
- [docs/customise-your-voice.md](docs/customise-your-voice.md) shows how to make it sound like you.
- [docs/troubleshooting.md](docs/troubleshooting.md) covers common snags.

## How this engine was built

This engine began as a fork of an idea from **Ryan Law**, Director of Content Marketing at
**Ahrefs**. He documented his Claude Code content pipeline in his post
[How I Do Content Engineering with Claude Code](https://ahrefs.com/blog/how-i-do-content-engineering-with-claude-code/)
and demoed it on the [Ahrefs Podcast](https://www.youtube.com/watch?v=iVZrVeESnFQ) with Tim
Soulo. The core structure here is his: small skills chained into a pipeline, every step
saving its output so you can debug it, a master command that runs them in order, and a
fork-and-personalise philosophy. Full credit and thanks to Ryan and Ahrefs.

We then made three sets of changes:

**1. A friendlier setup and onboarding flow.** Ryan's repo assumes you already know your
brand, voice, and process. Ours is built for people setting this up for the first time:
- **Plain-English install guides** for Mac and Windows that assume no prior GitHub, VS Code,
  or Claude Code experience.
- **Placeholder context files** in `your-setup/` (brand, voice, offer, data sources) with a
  setup gate that stops the engine running until you have made it yours.
- A guided **`/setup` command** that fills those files in for you. It asks for documents you
  already have first (brand guide, ICP, product one-pager) and only asks questions for the
  gaps, so you are not retyping things you already wrote down.

**2. Upgraded with tactics from four CXL courses.** We pulled the strongest ideas from CXL's
content and search courses and baked them into the skills:
- Start **bottom-of-funnel** and prioritise commercial intent over raw search volume.
- Mine **voice of customer** (sales calls, interviews, tickets, reviews) for high-intent
  topics and real buyer language that keyword tools miss.
- Write for **answer engines** (ChatGPT, Perplexity, AI Overviews), not just rankings, so
  your content gets cited, and keep your brand represented accurately in them.
- Pass the **"average of the internet" test**: if a reader could get the same article from a
  one-line prompt, it is not worth publishing. Lead with proprietary data and point of view.

**3. Focused on B2B marketing.** Every skill is biased toward B2B: buyer-journey stages,
decision factors (integrations, pricing, compliance, support), comparison content, and
sourcing every competitor claim.

For the full list of what changed, see [docs/how-this-was-made.md](docs/how-this-was-made.md).

## Credits

- **Ryan Law** and **Ahrefs**, for the original content-engineering approach this is built on.
  Read his post: <https://ahrefs.com/blog/how-i-do-content-engineering-with-claude-code/>
- The **CXL courses** these tactics come from:
  - [Build optimized B2B content funnels with AI](https://cxl.com/institute/online-courses/b2b-lead-generation-with-ai/), Andy Crestodina
  - [Bottom-of-funnel SEO strategies in tough niches](https://cxl.com/institute/online-course/bottom-of-funnel-seo-strategies-in-tough-niches/), Gaetano DiNardi
  - [Increase visibility and revenue from AI discovery engines](https://cxl.com/institute/live-course/increase-visibility-and-revenue-with-ai-discovery-engines/), Alex Birkett
  - [Optimize pages for AI search with GEO](https://cxl.com/institute/online-courses/optimize-pages-for-ai-search-with-aeo-cohort/), Steve Toth

## Make it yours

This is a starting point, not a finished product. You are meant to fork it, rename
skills, add steps, and remove the parts you do not use. The more you shape it to how
you actually work, the better it gets.
