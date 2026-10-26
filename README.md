# YoYoSim

Interactive 3D yo-yo simulation for teaching gravity, rotation, inertia, and energy.

## Enable GitHub Pages

The site files are ready on `main`. To publish them:

1. Open https://github.com/enigmaldc/YoYoSim/settings/pages
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose **main** and **/(root)**, then click **Save**.
4. Wait for GitHub to finish the Pages deployment. Use **Visit site** on the Pages settings screen to confirm publication.

Expected address after successful publication:

https://enigmaldc.github.io/YoYoSim/

Share the `github.io` address with pupils. They do not need GitHub accounts, Python, or installations. They need internet access and a current browser with WebGL 2.

## Controls

- Drop, pause/resume, reset, or advance one simulation step.
- Adjust gravity, string length, mass, body radius, axle radius, inertia, and energy loss.
- Drag to rotate the view, scroll to zoom, and right-drag to pan.
- Keyboard: Space = play/pause, R = reset, N = step, C = reset view.

## Technical details

All application code is in `index.html`; no build step is needed. `.nojekyll` tells GitHub Pages to serve the files directly. Three.js and OrbitControls both load from jsDelivr, pinned to version 0.180.0. The physics runs in the visitor's browser. There are no paid AI calls, API keys, databases, or OpenAI hosting dependencies.

The simulation uses an ideal fixed-axle, vertical Maxwell-wheel model. It does not model swinging or free-spinning bearing tricks. The in-page notes describe the assumptions.

## Updates

Update `index.html` on `main` and commit the change. Once Pages is enabled, GitHub republishes from that branch. Editing the separate OneDrive copy does not automatically update GitHub.

The previous ChatGPT-hosted copy is independent of this repository.

## Optional local preview on Windows

```powershell
py -m http.server 8000 --bind 127.0.0.1
```

Open http://localhost:8000/.

[Official GitHub Pages publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
