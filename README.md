# Downloads

A simple download page: https://x-alted1.github.io/downloads/

Anything in the `files` folder shows up on the page with a Download button. Links in `links.json` show up as link cards.

## Add a file

1. Open this repo on github.com.
2. Go into the `files` folder.
3. Click **Add file** → **Upload files**.
4. Drag your files in and click **Commit changes**.

The page updates about a minute later.

**Size limits:** the browser uploader accepts files up to 25 MB, and GitHub rejects any file over 100 MB. For bigger files, use **GitHub Releases** (Releases → Draft a new release → attach files → Publish). The page also lists the files attached to the latest release.

## Add a link

Edit `links.json` (click the file, then the pencil icon) and add an entry:

```json
[
  { "title": "My link", "url": "https://example.com", "description": "Optional short note" }
]
```

Separate entries with commas, then commit.

## How it's published

GitHub Pages serves the `gh-pages` branch. A small workflow (`.github/workflows/sync-pages.yml`) copies `main` to `gh-pages` on every commit, so you only ever edit `main`.
