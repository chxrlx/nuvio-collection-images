# nuvio-collection-images

Artwork for my Nuvio collections (static + animated hover images).

## Layout

```
<collection-slug>/
  static.png   — static backdrop image (16:9)
  hover.webp   — animated hover version (slow zoom loop, 4 s)
```

Raw URLs once pushed to GitHub (public repo `nuvio-collection-images`):

```
https://raw.githubusercontent.com/chxrlx/nuvio-collection-images/refs/heads/main/<slug>/static.png
https://raw.githubusercontent.com/chxrlx/nuvio-collection-images/refs/heads/main/<slug>/hover.webp
```

## Status (2026-11-12)

- ✅ **k-drama** — static.png (2048×1152) + hover.webp (960×540, 48 frames, 4 s loop, 1.9 MB) — both verified.
- ✅ **marvel, dc, universal, mgm, a24, warner-bros, disney, pixar, sony** — all staged locally 2026-11-12: static.png (2048×1152, plain serif title overlay via ffmpeg drawtext, no logos) + hover.webp (960×540, slow-zoom loop, 4 s, all < 3 MB). Base art generated from brand-free evocative prompts (no trademarked names in prompts). All files verified with PIL; 3 statics visually inspected (title legible).
- ⏳ Upload pending: the GitHub repo `nuvio-collection-images` does not exist yet.

## Notes

- The GitHub repo `nuvio-collection-images` does not exist yet and could not be created via the GitHub connector (the GitHub App token returns 403 for repo creation in a personal account). Create it as a **public** repo first, then push this directory.
- Animated WebP note: this ffmpeg build's ffprobe cannot parse animated WebP ("image data not found") — the files were verified with Python/PIL instead (valid WebP, correct frame count, zoom confirmed visually).
