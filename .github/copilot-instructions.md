**Purpose**
- **Summary:** Concise instructions for AI coding agents to be immediately productive in this repository.

**Big Picture**
- **Project Type:** Single-file static site. Entry is `index.html` (root) that renders a small demo titled "Donut Shop".
- **Architecture:** No backend or build system; everything served as static HTML/CSS. There are no JS modules, package manifests, or tests discoverable.

**Key Files**
- **`index.html`:** Single-page entry and the main source of truth for layout and content. Look here for UI and styling patterns.
- **`README.md`:** Placeholder; contains no actionable build instructions.

**What to watch for (concrete examples)**
- **Broken/mistyped HTML:** `index.html` currently has `!doctype html` — replace with the canonical `<!DOCTYPE html>`.
- **External asset links:** The `img` in `index.html` points at a pngtree HTML page (`https://pngtree.com/...html`) rather than a direct image URL; prefer embedding a direct image or adding `assets/` and storing images locally.
- **Inline styling:** Styles are in a `<style>` block in `index.html`. Keep edits minimal and colocated unless you introduce an `assets/` or `css/` folder.

**Developer workflows**
- **Preview locally:** No build step — open `index.html` directly in a browser, or run a simple static server from the project root.

```powershell
# from project root (PowerShell)
python -m http.server 8000
# or (if Node available)
npx http-server . -p 8000
```

- **No tests or CI detected:** Do not attempt to run tests; none are present.

**Agent editing rules (practical constraints)**
- **Minimize scope:** This repo is a tiny static demo — prefer small, self-contained changes to `index.html` rather than adding heavy toolchains.
- **Preserve intent:** Keep title/content ("Donut Shop") unless user asks for feature changes.
- **Fix visible mistakes:** Correct typos in HTML (doctype), change invalid image `src` to a valid image URL or local asset, and ensure proper `<meta>` tags remain.
- **Assets:** If adding images, place them under `assets/` and update `index.html` to reference `assets/<file>`.

**Integration & external dependencies**
- **External content:** The site currently loads an external image reference; validate licensing before bundling that asset into the repository.

**PR guidance for humans**
- **Scope and rationale:** Each PR should be small; include a one-line rationale (e.g., "Fix doctype and correct image src to local asset").

**If unsure / need more context**
- Inspect `index.html` and ask the repo owner whether they want a static demo or an expanded project scaffold.

Please review — tell me which parts are unclear or if you want the agent to also scaffold `assets/` and replace the external image with a local one.
