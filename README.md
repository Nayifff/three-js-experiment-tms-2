# TMS — Riyadh, after dark (riyadh-2: cinematic terminal)

A copy of `../riyadh` with the 3D environment redesigned for a photographic look: one wall of stacks on the right, a low off-axis 40mm camera, a single dominant floodlight with falloff and shafts, dense near-black fog, contact shadows and dented, scratched container paint. Copy, navigation and brand are unchanged. Serve on port 4176.

A minimalist landing page for an AI-powered transportation management system, built directly on the
Kage engine (see `../kage`): the same fixed WebGL canvas, scroll-driven camera, film composite,
word-by-word reveals, giant 3D wordmark, chapter rail and editorial layouts.

The temple world is gone. What is left is deliberately sparse: a wet apron at night, six shipping
containers standing still, the Riyadh skyline on the horizon, and the Kingdom Centre's outline with
its lit opening. Everything else is fog.

## Run locally

```bash
python3 -m http.server 4176 --bind 127.0.0.1
```

Then open http://127.0.0.1:4176/. There is no build step.

`?shot=2` jumps to a chapter for screenshots; add `&driver=timer` if the tab is in the background.

## Early access form

There is no backend. The form validates the input, stores the request in this browser's
`localStorage` under `tms-early-access`, and shows a confirmation. Replace the `localStorage` block in
`wireForm()` to send it somewhere real.

## Earlier versions

The daytime Riyadh version is kept in `../archive/riyadh-day`.

## Licence note

The engine code comes from Kage (github.com/MengTo/kage), which grants no licence for reuse or
redistribution. Fine for local experiments; get permission or rewrite the borrowed parts before
publishing. The vendored Three.js r149 is MIT-licensed.
