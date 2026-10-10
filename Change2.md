# Change 2: Replace placeholder project links

## Goal

Replace the portfolio's placeholder project links with the supplied real hyperlinks. Match destinations by project title; the Vimeo URL belongs to the Hear Us Out documentary.

## Requirements

- External links open in a new tab with `target="_blank"` and `rel="noopener noreferrer"`.
- Links within the portfolio use Jekyll's `relative_url` filter.
- Use descriptive link text rather than “click here.”
- Preserve the existing pine-green and gold link styling.

## Link mapping

| Project | Destination | Link text |
| --- | --- | --- |
| Ade Dehye | https://adedehye.com/ | Visit Ade Dehye |
| Kinfolx | https://kinfolxoakland.com/ | Visit Kinfolx |
| Viewers Like Us | https://viewerslikeus.com/ | Explore Viewers Like Us |
| Hear Us Out | https://vimeo.com/378389873/f68ff036ba?fl=pl&fe=vl | Watch Hear Us Out on Vimeo |
| Anthem | https://www.hulu.com/movie/anthem-6b25fac9-da2b-45a3-8e09-e4156b0471cc | Watch Anthem on Hulu |
| Revolutionary Care: An Oakland Story | https://give.ucsfbenioffchildrens.org/stories/revolutionary-care-oakland-story-podcast | Listen to Revolutionary Care |
| A Right To Heal | https://podcasts.apple.com/us/podcast/a-right-to-heal/id1707626036 | Listen to A Right To Heal |

## Implementation

- Populate the five film/audio destinations and descriptive labels in `work.md`.
- Populate the Kinfolx and Ade Dehye website destinations in `contact.md`.
- Use a shared `_includes/site-link.html` template for project links and the optional résumé link. External URLs are escaped and retain their original destination, including Vimeo's query parameters. Internal paths pass through `relative_url`.
- Keep the existing `text-link` and `field-value` classes, theme colors, hover styles, and keyboard focus styles.
- Update outdated text that says media links are unavailable. Other missing details remain placeholders.
- Keep `Change2.md` at the repository root, excluded from public Jekyll output.

## Verification

- Strict Jekyll builds passed with both an empty base URL and `/portfolio-preview`.
- Rendered HTML checks passed for all seven project-to-URL mappings, descriptive labels, `target="_blank"`, and `rel="noopener noreferrer"`.
- External destinations remained unchanged in both builds, including the complete Vimeo URL. Internal navigation correctly gained the alternate base-URL prefix.
- All seven project link placeholders were replaced. The separate, unconfigured résumé link remains a placeholder.
- `Change2.md` was confirmed absent from public output.
- The running Contact page returned HTTP 200 and was visually checked to confirm the Kinfolx and Ade Dehye links retain the existing theme styling.
