# Repository Guidelines

## Project Structure & Module Organization
- `content/`: Markdown pages and posts (e.g., `content/posts/meu-primeiro-post.md`).
- `archetypes/`: Blueprints for `hugo new` front matter.
- `themes/`: Hugo themes; active theme is `PaperMod` (git submodule). `ananke/` is included for reference.
- `config.toml`: Site configuration (pt-br locale, menus, PaperMod profile mode).
- `static/` (optional): Public assets like images (`static/images/...`) served at `/images/...`.

## Build, Test, and Development Commands
- `hugo server -D`: Run locally with drafts, live reload at http://localhost:1313.
- `hugo`: Build production site into `public/`.
- `git submodule update --init --recursive`: Ensure `themes/PaperMod` is present.
- `hugo version`: Verify Hugo Extended (PaperMod requires >= v0.146.0).

## Coding Style & Naming Conventions
- **Markdown:** Use `#` headings, wrap lines reasonably, prefer Portuguese content (site `languageCode` is `pt-br`).
- **Filenames:** Kebab-case and lowercase for content (e.g., `minha-pagina.md`).
- **Front matter:** Prefer TOML for consistency with `config.toml`. Include `title`, `date`, `draft`.
- **Assets:** Place images under `static/images/` and reference as `/images/<name>.jpg`.
- **Overrides:** Do not edit theme files; customize via `layouts/` or `assets/` in repo root.

## Testing Guidelines
- No formal test suite. Validate locally with:
  - `hugo --gc --minify` to catch build issues and produce optimized output.
  - Review console for warnings (i18n, unused templates) and fix before PR.
- Include screenshots for visual changes and check mobile/desktop in `hugo server`.

## Commit & Pull Request Guidelines
- **Commits:** Use Conventional Commits where possible (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`). Imperative, concise subject.
- **PRs:** Provide description, linked issues, setup/verification steps, screenshots or preview URL (e.g., Vercel) for UI changes. Keep PRs focused and small.

## Security & Configuration Tips
- Keep secrets out of the repo; use deployment env vars.
- Update theme via submodule, not by copying. If upgrading PaperMod, note any breaking changes.
