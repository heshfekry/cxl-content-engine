# Read me first

This folder is the part you make your own. Everything else in the engine reads from here.

## What is a placeholder?

The other files in this folder are filled with **placeholder** text. Anywhere you see:

```
{{REPLACE_ME}}
```

that is a blank waiting for your real information. And any file with this line near the top:

```
<!-- SETUP_INCOMPLETE -->
```

has not been filled in yet.

While those markers are still here, the engine will refuse to write content. That is
deliberate. It stops you accidentally publishing in a generic or borrowed voice.

## You do not edit these by hand

You could, but you do not have to. Instead, start Claude Code and run:

```
/setup
```

It interviews you, fills in every file below, and removes the markers as it goes. When
all the markers are gone, the engine unlocks.

## What lives in this folder

| File | What it holds | Filled by |
|---|---|---|
| `brand-and-voice.md` | How you sound: tone, rules, words you avoid | `/setup` |
| `your-offer.md` | What you sell, so it gets mentioned naturally | `/setup` |
| `data-sources.md` | Which data tools you have turned on | `/setup` |
| `cms-connection.md` | Whether you publish straight to a CMS | `/setup` |
| `voice-examples/` | 5 to 10 of your best articles | you drop files in, `/setup` reads them |
| `source-docs/` | Existing brand, voice, audience, or product docs you already have | you drop files in, `/setup` reads them |

## The most important part: voice examples

The engine learns your voice from real examples, not from rules you write. Drop your best
articles into `voice-examples/` (as `.md`, `.txt`, or by pasting links during `/setup`).
Claude reads them, works out what makes them good, and writes content that matches. You
review and correct what it inferred. See [customise-your-voice.md](../docs/customise-your-voice.md).

You can re-run `/setup` any time to update any of this.
