---
name: update-preview
description: Build a side-by-side HTML view of the original article next to the refreshed version, so the user can see exactly what changed and approve or reject it.
---

# Update preview

Show the user precisely what the refresh changed. Trust comes from seeing the diff, not
from being told "it is updated."

## Input

- Original: `content/updates/1-extracted/{slug}.md`
- Updated: `content/updates/7-updated-draft/{slug}.md`

## Steps

1. Build a single self-contained HTML file showing the two versions side by side (or
   stacked on narrow screens).
2. Highlight what changed: additions, removed text, and swapped facts or stats marked
   clearly. Make it easy to scan for what is new.
3. For each changed stat, show the source next to it so the user can sanity-check.
4. Keep all CSS inline so the file opens with no internet and no other files.
5. Apply the user's brand colours lightly if defined, but keep readability first.

## Output

Write to `content/updates/5-update-preview/{slug}.html` and give the user the path to open
it. Remind them: nothing is published until they say so. Once they approve, they can run
`format-for-publish` to produce the final version or push a draft to their CMS.
