# Repository Guidelines

## Project Structure & Module Organization

This repository is a static website collection. The root `index.html` is the main Yoshihiko.inc landing page. Product-specific pages live in `Dreave/` and `eyerecovery/`, each with its own `style.css`, localized HTML pages, and assets. Legal pages live in `legal/` with language variants under `legal/en/` and `legal/ko/`.

Keep related files together:

- `Dreave/index.html`, `Dreave/en/index.html`, `Dreave/ko/index.html`: localized Dreave pages.
- `Dreave/assets/`: brand, screenshots, and App Store preview assets.
- `eyerecovery/images/` and `eyerecovery/assets/`: EyeRecovery media assets.
- Root `app-ads.txt` and verification HTML files must remain at the paths required by external services.

## Build, Test, and Development Commands

There is no package manager or build pipeline configured. Edit HTML and CSS directly.

- `python3 -m http.server 8000`: serve the repository locally at `http://localhost:8000`.
- `open http://localhost:8000/Dreave/`: preview the Dreave site.
- `rg "search text"`: search content across pages quickly.
- `git diff --check`: catch trailing whitespace and common patch issues before committing.

## Coding Style & Naming Conventions

Use semantic HTML and keep page structure consistent across Japanese, English, and Korean variants. Preserve existing file naming patterns such as `privacy.html`, `terms.html`, `contact.html`, and article-style names like `lucid-dream-guide.html`.

Prefer 2-space indentation in HTML/CSS when touching nearby code. Keep CSS selectors descriptive and scoped to the relevant site stylesheet rather than adding global rules in unrelated directories. Use relative links within each site section unless an external URL is required.

Do not end headings with punctuation. For Japanese headings, omit trailing `。` and `、`.

## Testing Guidelines

No automated test framework is present. Validate changes manually in a browser through the local static server. Check desktop and mobile widths, navigation links, localized alternates, image loading, and forms or mail links where present.

For SEO or metadata edits, verify canonical URLs, `hreflang`, titles, descriptions, and Open Graph tags across all affected language versions.

## Commit & Pull Request Guidelines

Recent commits use short, imperative English summaries, for example: `Fix layout collapse...`, `Add canonical and alternate hreflang tags...`, and `Optimize H1 text length...`. Follow that style and keep each commit focused on one concern.

Pull requests should include a brief change summary, affected paths, manual test notes, and screenshots for visible page changes. Mention any external service files touched, such as `app-ads.txt` or Google verification HTML.

## Agent-Specific Instructions

Do not overwrite localized pages independently when the same content or metadata should be updated in all languages. Avoid deleting verification files, ad configuration files, archived specs, or App Store assets unless explicitly requested.
