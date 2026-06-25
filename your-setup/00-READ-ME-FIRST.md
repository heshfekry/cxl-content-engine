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

## Updating your setup later

Your setup is not locked in. Change it whenever your brand, voice, offer, or audience moves
on. There are two ways:

1. **Re-run `/setup`.** It sees what is already filled in, shows it back, and lets you change
   only what you want. This is the easy path.
2. **Edit the files by hand.** Open any file in this `your-setup/` folder (`brand-and-voice.md`,
   `your-offer.md`, `data-sources.md`, `cms-connection.md`) and edit the text directly. Add or
   swap articles in `voice-examples/` and docs in `source-docs/` any time. Save, and the engine
   uses the new version on the next run. No special steps needed.

> Note on the first-run gate: the `{{REPLACE_ME}}` and `<!-- SETUP_INCOMPLETE -->` markers,
> and the setup-gate check in the commands, are a one-time safeguard for your very first run.
> Once setup is complete the engine retires that check so it does not waste tokens. That does
> not lock anything: you can still re-run `/setup` or edit these files by hand at any time, as
> above. The gate simply does not need to run again.
