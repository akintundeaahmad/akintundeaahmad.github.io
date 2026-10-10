# Portfolio Site Plan

## Site

Create a static, GitHub Pages user site for `akintundeaahmad.github.io`, published from the `main` branch and repository root. The site will use Jekyll, Markdown pages with YAML front matter, reusable Liquid layouts/includes, and plain responsive HTML/CSS.

## Pages and content

- **Home:** Introduce Akintunde Ahmad as an entrepreneur, marketer, and storyteller, with clear paths to selected work and contact.
- **About:** Present the supplied biography, capabilities, and education.
- **Work Experience:** Organize the supplied experience across ESO Ventures, Kinfolx, Ade Dehye, ServiceNow, and journalism/documentary work. Include individual media-project cards and an editable ServiceNow case-study placeholder.
- **Contact:** Provide editable LinkedIn, email, résumé, and project-link fields. Do not publish an email link or the uploaded résumé by default: the résumé contains a phone number and email address, and the user declined a public email link. Use clear placeholders for missing links and contact details.

Use the supplied portfolio text and résumé without inventing achievements or outcomes. Where the supplied material differs, prefer the portfolio text and retain specific résumé metrics only when they do not conflict. Leave image, synopsis, role, and viewing/listening-link fields editable for project cards.

## Presentation and accessibility

Use a light theme with crisp, technical typography. Take broad inspiration from the reference site's confident, image-led presentation, without copying its assets or layout. Keep the portfolio single-column, responsive at 375px and 1280px, keyboard-accessible, semantically structured, and high-contrast.

## Technical deliverables

Keep the complete site directly in the repository root: `_config.yml`, `index.md`, Markdown pages, `_layouts/`, `_includes/`, `assets/`, and the required GitHub Pages files. Configure `baseurl: ""` and use Jekyll URL filters. Include page-specific SEO metadata, a sitemap, favicon, and a README covering content edits, local preview, GitHub Pages publishing, and Lighthouse checks. Use no backend, database, CMS, contact form service, framework, or third-party trackers.

## Technical choices and assumptions

- Favor GitHub Pages' built-in Jekyll support so publishing from `main` and `/` needs no custom build workflow.
- Keep contact and project URLs in editable Markdown/front-matter content; use explicit placeholders until details or approved media are supplied.
- Avoid external fonts and scripts so the site remains lightweight and avoids unnecessary third-party requests.
- The current repository contains a Replit starter workspace and API/design artifacts rather than a Jekyll site. Implementing this plan means replacing that scaffold so the root contains only the static portfolio site and its source assets. Preserve the uploaded résumé as a source/reference, but do not publish it unless a version without private contact details is approved.

## Verification

Check that all navigation and URL-filtered links work, Jekyll builds for a GitHub Pages user site with an empty `baseurl`, and the rendered pages are usable at 375px and 1280px. Run Lighthouse and aim for at least 90 in Performance, Accessibility, Best Practices, and SEO; report any score limited by the local environment.
