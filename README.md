# Quiet Summit

A free, open-source mountaintop meditation for Meta Quest (2, 3, 3S, Pro) and any modern browser.

**Use it:** open <https://doktorigi.github.io/quiet-summit/> in the Quest browser and pick a length. No install, no account, no tracking.

You sit on a summit at sunrise above a valley of lakes and meadows, ringed by snowy ranges. The sun's glow and the wind swell and fade at a slow breathing pace (4s in, 2s hold, 6s out). A bell marks the start and the end.

Sister app: [Quiet Orb](https://github.com/doktorigi/quiet-orb).

## Develop

It is one file, `index.html`, with no build step. three.js loads from a CDN and all sound is synthesised. The landscape is generated in code at load: heights, normals and cast shadows are computed once, then shaded per pixel (ground cover, lakes, haze and sky share one sky model). Only the summit rocks use real lights and a shadow map.

    python -m http.server 8766

Open <http://localhost:8766/>. Add `#test` to the URL to run the self-check (the tab title becomes "tests ok").

WebXR needs HTTPS, so to try changes in a headset, push to GitHub Pages.

## License

MIT
