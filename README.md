# Physics Playground — source of truth

**Project:** KazTech Physics Playground  
**URL:** https://kaztech99.com/playground.html  
**Repository:** `kasowitz/kaztech99.github.io`  
**Last updated:** October 25, 2026  
**Version:** 0.1 — initial prototype (hands-on browser testing pending)

## Project goal
Build an enjoyable, realistic-looking and increasingly physically accurate **2D** browser physics sandbox. Smooth interaction is a priority. Begin with rigid objects; expand later to sand, water, and experimental mechanisms.

## Scope and site safety
- This project owns only `playground.html` and this root `README.md`.
- **Do not change any pre-existing website files** (including `index.html`, assets, other pages, CNAME, sitemap) unless explicitly requested and authorized.
- The new page is a standalone direct URL. Do not add navigation links to the existing site without permission.
- Prefer a single self-contained page until growing complexity warrants additional new files.
- GitHub Pages deployment is triggered by commits to the site's repository even when only new files are added.

## Implemented in source (v0.1)
- Standalone HTML/CSS/JavaScript page (no build step).
- **Rapier 2D 0.21.0 compatibility build** for rigid-body physics, imported from a pinned CDN URL.
- **PixiJS 8.22.0** for hardware-accelerated 2D rendering, imported from a pinned CDN URL.
- Gravity, collisions, angular motion, restitution and friction.
- Dynamic balls and boxes; fixed angled ramps; floor, wall and ceiling colliders.
- Click to spawn, pointer dragging/throwing, grab-only, erase, spawn multiple balls.
- Gravity, bounciness and friction sliders; pause/resume, reset and clear controls.
- Responsive layout, object counter, approximate FPS counter, error state when CDNs fail.
- Fixed 60 Hz physics steps with catch-up cap; limit 200 user-created objects.
- Initial scene spawns two balls, one box and one ramp.

**Verification distinction:** The above is what code attempts to implement; it has **not yet been fully tested in a real browser**, so do not claim every control works until actual tests pass. Record any confirmed issues below.

## Known constraints
- CDN imports require an internet connection and third-party availability.
- First-load cost includes Rapier's WASM initialization.
- Sand/water and liquid/particle-solid interactions are **not implemented**.
- The FPS display reports rendering cadence; physics runs at fixed 60 Hz if compute budget permits.
- 60 FPS is a performance goal, not a guarantee on every device.
- The toy has no persistent saving or user accounts.

## Roadmap (planned, NOT implemented)
1. Test the public URL, library initialization and pointer interaction on desktop and mobile; resolve any bugs.
2. Add material/object configuration, rotate/rescale, more ramps and obstacles; save/load scenarios.
3. Pendulums, hinges, joints, chains, springs, dominoes and motors.
4. Granular particle solver for sand.
5. Fluid solver for water and interaction with rigid bodies.
6. Performance profiling and optional worker/GPU acceleration as needed.

## Mandatory upkeep — README is the truth
- **Read this README before every substantive change.**
- **Keep this README updated alongside every implemented change.**
- Separate verified functionality, code implemented but not tested, limitations and future ideas.
- Update controls, library versions, architecture decisions, dependencies, known defects and test status accurately.
- Never claim features are finished when they are only planned.
- Never touch existing site files without explicit permission.
- A successful GitHub commit confirms repository changes, but does not by itself verify GitHub Pages is serving the updated page.

## Testing log
- **2026-10-25:** Initial prototype created. Public deployment and real-browser functionality remain to be checked.
