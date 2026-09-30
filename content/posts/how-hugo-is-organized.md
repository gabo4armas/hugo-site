---
title: "How a Hugo project is organized"
date: 2026-09-29
---

After a bit of experimenting, this is the mental model I ended up with:

- `hugo.toml`: site-wide settings (title, menu, parameters).
- `content/`: pages and posts written in Markdown with front matter.
- `layouts/`: HTML templates. `baseof.html` is the skeleton, and `single.html`
  and `list.html` render individual pages and section listings.
- `static/`: files copied as-is, such as CSS.

Once I understood that folder structure, the rest was just filling it in.
