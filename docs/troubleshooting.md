# Troubleshooting

Common snags and how to fix them. If you are stuck, you can also just ask Claude Code in
plain English: "this is not working, here is what happened."

## "It told me to run /setup and will not write anything"

That is the setup gate doing its job. The engine will not write content until you have
replaced the placeholders with your own brand and voice. Run `/setup` and answer the
questions. Once every file in `your-setup/` is filled in, the engine unlocks.

## "claude: command not found"

Claude Code did not install, or your Terminal has not picked it up yet. Close the Terminal
panel and open a new one, then try again. If it still fails, re-run the install step in your
START-HERE guide.

## "code: command not found" (the `code .` step)

VS Code's command-line shortcut is not installed. Open VS Code, press the shortcut to open
the command palette (Cmd+Shift+P on Mac, Ctrl+Shift+P on Windows), type
"Shell Command: Install 'code' command in PATH", and run it. Then try `code .` again.

## "git clone" did not work

Check you pasted the full link your host gave you, with no spaces broken across lines. Make
sure you have an internet connection. If it says git is not found, install Git from your
START-HERE guide.

## The article does not sound like me

You need better voice examples. Add 5 to 10 of your strongest articles to
`your-setup/voice-examples/` and run `/setup` again. See
[customise-your-voice.md](customise-your-voice.md). Rules alone will not do it; the examples
are what teach your voice.

## A research step gave thin or generic results

By default the engine uses built-in web search. For sharper keyword and SERP data, connect
a data tool and turn it on in `your-setup/data-sources.md` (see below).

## Connecting a data tool (Ahrefs, Search Console, GA4)

These connect as MCP servers in Claude Code. Each provider has its own setup. In short: you
add the server to your Claude Code settings, authenticate, then change that tool from `off`
to `on` in `your-setup/data-sources.md`. Ask Claude Code "help me connect the Ahrefs MCP"
and it will walk you through your specific case.

## Connecting a CMS (WordPress, Webflow, others)

Same idea: connect the CMS as an MCP server or via its API, then update
`your-setup/cms-connection.md` to `status: connected`. Ask Claude Code "help me connect my
WordPress site" and follow along. Until then, the engine gives you a clean document to copy
and paste, which works everywhere.

## I want to change a step

Every step is a small file in `.claude/skills/`. Open the one you want to change (for
example `.claude/skills/draft/SKILL.md`) and edit it, or ask Claude Code to change it for
you: "make the draft step write shorter intros." It is meant to be changed.
