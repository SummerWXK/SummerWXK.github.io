# Repository Guidelines

## Project Structure & Module Organization

This repository is a static GitHub Pages personal website. The main page lives in `index.html`, with global styles in `main.css` and `stylesheet.css`. Additional CSS and legacy Bootstrap files are under `css/` and `format/`. Blog pages live in `blogs/`, with article-specific images in `blogs/lingbot_video_assets/`. Site images, logos, and certificates are in `images/`; publication PDFs and citation text files are in `work/`. Search and crawler files such as `robots.txt`, `sitemap.xml`, and verification HTML/XML files stay at the repository root.

## Build, Test, and Development Commands

There is no package manager or build step. Edit the static files directly.

- `python3 -m http.server 8000`: serve the site locally from the repository root.
- `open http://localhost:8000`: preview the rendered site in a browser.
- `git status --short`: check pending changes before committing.

When changing links, assets, or metadata, verify the affected pages in the browser rather than relying only on source inspection.

## Coding Style & Naming Conventions

Use 2-space indentation for standalone HTML pages that already follow that style, and preserve existing indentation in older files. Prefer lowercase, descriptive file names for new HTML/CSS assets; keep existing publication and certificate names unchanged if they are externally referenced. Keep CSS selectors semantic and scoped to the page or module being changed. Avoid adding generated files such as `.DS_Store`.

## Testing Guidelines

No automated test framework is configured. Manual testing is expected for visual and navigation changes. For each update, run a local server and check the modified page at desktop and mobile widths. Confirm images and PDFs load from relative paths, external CDN links still resolve, and `sitemap.xml` remains accurate when adding or removing public pages.

## Commit & Pull Request Guidelines

Recent history uses short, direct commits such as `fix: news`, `update: sitemap.xml`, and `update: iclr 2026`. Keep commits focused and use a concise imperative or `type: summary` format. Pull requests should describe the visible change, list files or pages touched, mention any updated search metadata, and include screenshots for layout or image changes. Link related issues when available.

## Security & Configuration Tips

Do not commit private analytics tokens, unpublished documents, or personal data beyond content intended for the public site. Keep large media intentional; `.gitattributes` currently routes only `*.pptx` and `*.mp4` through Git LFS.
