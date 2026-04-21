# Project Summary

## 2026-04-21
* Fixed deployment error by adding a `build` script to `package.json` that generates production Tailwind CSS assets.
* Adjusted build script to create an `out` directory and populate it with static assets, resolving the Cloudflare Pages deployment error.
* Replaced a 31MB hero video with a 12MB version and removed unused 30MB+ assets to stay under Cloudflare's 25MB file size limit.

## 2026-04-20
* Removed the yellow falling wisp animation and related Javascript from `index.html`.
* Removed the glow and highlighted floating elements around the "Magic" text in the hero section to simplify the visual design.
