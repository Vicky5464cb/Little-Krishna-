# Neon Sketch Reveal (HTML version)

A self-contained, single-file HTML/Canvas animation that reveals an image
as a glowing neon edge-sketch, then crossfades into the original picture.
No dependencies, no build step — the source image is embedded directly in
`neon_reveal.html` as base64, so the file works entirely on its own.

## Why it doesn't "work" when viewed directly on github.com

GitHub's normal file view (`github.com/<user>/<repo>/blob/main/neon_reveal.html`)
only ever shows the **source code** of an HTML file — it never runs the
JavaScript or renders the page. That's expected behavior, not a bug in the
file. To actually see it run, you need **GitHub Pages**, which serves the
repo's files as a real live website.

## How to view it live (GitHub Pages)

1. Push `neon_reveal.html` to a GitHub repository.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick the branch (usually `main`) and the folder (`/root`), then **Save**.
5. GitHub will give you a URL like:
   `https://<username>.github.io/<repo-name>/neon_reveal.html`
6. Open that URL — that's the live, running page. It can take a minute or two
   after saving for the first deploy to go live.

### Optional: make it the homepage of the repo

If you rename `neon_reveal.html` to `index.html` (or add a copy named that
at the repo root), it will load automatically at:
`https://<username>.github.io/<repo-name>/` — no filename needed in the URL.

## Controls

- Click anywhere, or press any key, to enter fullscreen (browsers require a
  user gesture before they'll allow fullscreen — it can't happen fully
  automatically on page load).
- **R** — restart the animation from the beginning.
- **Esc** / **Q** — pause.
- Once the reveal finishes, it freezes on the final image and does not loop.

## Notes

- Everything (image + code) lives in the one `.html` file, so it's safe to
  drag-and-drop it straight into a repo — no other assets required.
- If you swap in your own image, re-generate the file rather than editing
  the base64 by hand.
