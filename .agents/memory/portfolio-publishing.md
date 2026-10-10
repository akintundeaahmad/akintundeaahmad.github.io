---
name: Portfolio publishing rules
description: User-directed scope and privacy constraints for the portfolio.
---

The user explicitly chose a root-level static Jekyll site for GitHub Pages over the initially selected React/Vite artifact. Do not introduce a separate framework app, backend, database, or preview application.

**Why:** The user requires direct GitHub Pages publishing from `main` and `/ (root)` with Markdown content, reusable HTML/Liquid templates, CSS, and minimal JavaScript.

**How to apply:** Keep the publishing source at the repository root. A local Jekyll preview serves that same source; it must not become a second application.

The user declined a public email link. Do not publish their uploaded résumé by default, because it contains contact details.

**Why:** The user does not want contact information exposed through the public site or its downloadable files.

**How to apply:** Obtain approval or an explicitly shareable résumé before linking a public copy. Source uploads must remain excluded from Jekyll output.

The user requested deleting placeholder content rather than displaying unfinished areas. Show only supplied content and omit empty fields; retain real project information and links.

**Why:** The user finds visible placeholders tacky and prefers a finished, minimal portfolio.

**How to apply:** Do not add dummy content, incomplete-field messages, or coming-soon notices. Keep optional content out of public output until it is supplied.
