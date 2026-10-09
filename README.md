# Zaid — AI for Telecommunications

A complete static snapshot of the course website at https://zaid.hs-rp.com/, taught by الأستاذ المهندس زيد العنزي.

This repository preserves the deployed release `20260918T160127Z`, captured on 2026-10-09. All 40 hosted files are copied byte for byte, including the browser JavaScript and CSS, fonts, photos, video, captions, lecture presentations, notebooks, and example telecommunications dataset. The SHA-256 checksums are recorded in [docs/snapshot-manifest.json](docs/snapshot-manifest.json).

## Run locally

Python 3 is sufficient; there is no package installation or build step:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory public
```

Open http://127.0.0.1:8000/. Use a web server rather than opening `index.html` directly so that JavaScript modules and downloads work.

## Files

- `public/index.html`: Arabic right-to-left course page.
- `public/assets/`: compiled JavaScript, CSS, and fonts.
- `public/media/`: instructor photos, course video, captions, and social preview image.
- `public/resources/`: five lecture presentations, extracted lecture text, course notebooks, sample CSV data, and a ZIP of the presentations.

## Hosting

Serve `public/` as the document root of an ordinary static web server. Keep the directory structure intact. The existing canonical and social preview URLs point to https://zaid.hs-rp.com/; update them when moving to a different public URL. Embedded Python tutorial examples also use the original host’s CSV URL; update those examples if that address changes.

## Source availability

The original editable React/TypeScript project, package manifest, and build tooling were not found on the server. The JavaScript here is the compiled browser output; this snapshot preserves the running website and its teaching materials, but it cannot regenerate those bundles from original source. Add the original project if it becomes available before making substantial application changes.

## Verification

All 40 copied files matched the deployment SHA-256 checksums and were served successfully by a local HTTP server. The copied site also rendered 11 routes at mobile (360 px) and desktop (1440 px) sizes, with no JavaScript errors or failed local asset responses.

Repository preparation did not modify the hosted website; it continued returning HTTP 200.
