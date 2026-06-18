# Drop your voice-of-customer material here

This is the single best source of B2B content ideas: the language your customers use when
they describe their problems. The engine mines it for high-intent topics, real buyer
phrasing, pain points, and objections that keyword tools never surface.

## What to add

Any material where customers or prospects speak in their own words:

- Sales calls and discovery call transcripts
- Customer interviews and win/loss calls
- Support tickets and chat logs
- Survey open-ended responses
- Review-site comments (yours or competitors')

Transcript exports from Gong, Fireflies, Otter, Zoom, or plain `.txt` and `.md` files all
work. Drop the files straight in this folder.

## How it's used

- `/blog-pipeline` runs `voice-of-customer-mining` first when this folder has files, and
  feeds the findings into research.
- You can also run the `voice-of-customer-mining` skill on its own to build a topic backlog.

If the folder is empty, the engine carries on and reminds you to add material next time.

> Note: files here stay on your computer. They are ignored by git so private call and
> customer data never gets pushed when you share the repo.
