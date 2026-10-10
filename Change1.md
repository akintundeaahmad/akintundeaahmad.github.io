# Change 1: Add images to the portfolio

## Goal

Replace the portfolio's project image placeholders with the uploaded images in `assets/images`. Filenames match the corresponding project sections.

## Requirements

- Render image paths with Jekyll's `relative_url` filter.
- Give every image descriptive alt text.
- Keep images responsive on mobile.
- Preserve the existing minimal layout, pine-green/gold palette, and project copy.

## Image mapping

| Project | Image | Alt text |
| --- | --- | --- |
| Anthem | `/assets/images/anthem.jpeg` | Anthem documentary title over a dark audio mixing console. |
| Revolutionary Care: An Oakland Story | `/assets/images/revolutionary-care.jpeg` | Revolutionary Care: An Oakland Story artwork with colorful buildings, trees, and a steel bridge. |
| Viewers Like Us | `/assets/images/viewers-like-us.png` | Viewers Like Us artwork with a yellow eye, a red question mark, and orange-red title lettering. |
| A Right To Heal | `/assets/images/a-right-to-heal.jpeg` | A Right To Heal podcast artwork with white and yellow title lettering over a blue-green grid. |
| Hear Us Out | `/assets/images/hear-us-out.jpeg` | Hear Us Out Docfest artwork showing a group standing together on a stage at the Columbia Doc Program. |

## Implementation

- Populate image paths, alt text, and intrinsic image dimensions in the project front matter in `work.md`.
- Use the shared `_includes/project-card.html` template to render the images with `relative_url`, escaped alt text, and lazy loading.
- Display images in responsive 16:9 frames with `object-fit: contain`, preserving the complete artwork without cropping or stretching it.
- Update the project introduction so it no longer says images are missing. Unavailable media links and other missing details remain clearly marked.
- Keep this change document at the repository root, excluded from the public Jekyll output.

## Verification

- Strict Jekyll builds passed with both an empty base URL and `/portfolio-preview`.
- All five images are included in the output, have descriptive alt text and intrinsic dimensions, and return HTTP 200 in the preview.
- The alternate-base-URL build correctly prefixes every image path with `/portfolio-preview`.
- Browser checks at 375px and 1280px confirmed that all five images decode successfully, fit within the viewport without horizontal overflow, and use `object-fit: contain`. The project section was visually inspected at both widths.
- `Change1.md` remains at the repository root and is excluded from the public website output.
