# Akintunde Ahmad — Personal Portfolio

A static Jekyll site for the GitHub Pages user-site URL `https://akintundeaahmad.github.io/`. The repository root is the site source; no application framework, backend, database, or separate build service is needed on GitHub Pages.

## Publish with GitHub Pages

1. Push this repository to a repository named **`akintundeaahmad.github.io`** under the GitHub account `akintundeaahmad`.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select `main` and `/ (root)`, then save.
5. Allow GitHub Pages to finish the first build and open `https://akintundeaahmad.github.io/`.

This is a user site, so `_config.yml` intentionally sets `baseurl: ""`. Site links use Jekyll’s `relative_url` filter.

## Edit the site

- `index.md`, `about.md`, `work.md`, and `contact.md` contain the page copy and YAML front matter.
- `_layouts/default.html` provides the shared page shell. The other layouts arrange page content; `_includes/` holds shared navigation, footer, page headings, and project cards.
- `_data/navigation.yml` controls the main navigation.
- `assets/css/site.css` contains the responsive design and accessible focus styles.
- `assets/favicon.svg` is the site icon.
- The visual direction is inspired by the Oakland A’s colors: deep pine green, subdued gold, and a minimal single-column layout. No team logo or borrowed artwork is used.
- In `contact.md`, update the `contact` fields to add approved résumé or project links. Keep `show_email: false` unless you explicitly decide to publish an email link. To enable a public email, fill in `email` and set `show_email: true`. A `mailto` link makes the address public and requires visitors to have an email app. Update the Contact page’s Markdown copy at the same time.
- Any résumé file placed in `assets/` is public. The uploaded résumé is not published because it includes private contact details. A future public version can be placed in `assets/files/` and linked through `resume_url`.
- `work.md` has a `projects` list in YAML front matter. Edit each project’s `synopsis`, `role`, `image`, `image_alt`, `url`, and `link_label`. Put approved images under `assets/images/` and use paths such as `/assets/images/anthem.jpg`. Missing values appear as clearly marked placeholders. Do not use `attached_assets/` directly because those source files are excluded from the published site.
- `PLAN.md` records the approved build plan and is excluded from the public site.

## Preview locally

Install Ruby, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000/`. Jekyll rebuilds the site when source files change.

Replit’s **Jekyll Preview** workflow serves this same Jekyll site; it is not a separate preview application. `_site/` is generated output, is ignored by Git, and is not the GitHub Pages publishing source.

## Check with Lighthouse

After previewing locally or publishing, open Chrome DevTools → **Lighthouse**, select **Mobile** and the Performance, Accessibility, Best Practices, and SEO categories, then run an audit. The design targets scores of 90 or higher; final values can vary by browser, machine, and network.

Check the layout at both **375px** and **1280px** widths. The site is single-column, uses system fonts, contains no client-side scripts or trackers, and has visible keyboard focus and a skip-to-content link.

### Verified results

Local Chromium mobile Lighthouse audits returned the following scores:

| Page | Performance | Accessibility | Best Practices | SEO |
| --- | ---: | ---: | ---: | ---: |
| Home | 100 | 100 | 100 | 100 |
| About | 100 | 100 | 100 | 100 |
| Work Experience | 100 | 100 | 100 | 100 |
| Contact | 100 | 100 | 100 | 100 |

All four pages were checked at 375px and 1280px with no horizontal overflow. Local navigation, assets, and anchor links passed; the GitHub Pages-compatible Jekyll build passed with strict front-matter validation. The published output excludes uploaded source documents and contains no public email link. Re-run Lighthouse after changing content or publishing to measure the live hosting environment.

## Important choices and assumptions

- Jekyll and the `github-pages` gem match GitHub Pages’ supported build environment; `jekyll-sitemap` generates the sitemap.
- The GitHub username is exactly `akintundeaahmad`, as supplied.
- Where the résumé and portfolio text differ, the portfolio text takes priority—particularly Ade Dehye’s February 2021 founding date.
- No headshot, project image, approved ServiceNow case-study detail, public résumé, or project website URL was supplied. These remain explicit placeholders rather than fabricated content.

