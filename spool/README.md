# The spool paradox

Interactive Three.js teaching experiment: pull a string horizontally from the
top or bottom of a spool's inner axle. Both arrangements roll toward the pull
when there is enough static friction for rolling without slipping.

Pupil page after GitHub Pages publishes this folder:

https://enigmaldc.github.io/YoYoSim/spool/

## Suggested classroom sequence

1. Start with **String on top** and ask pupils to predict the direction.
2. Choose **Pull for 2 seconds**, or hold **Hold to pull**.
3. Switch to **String underneath**, predict again, and repeat.
4. Choose **Compare both** for equal forces, settings, time and camera scale.
5. Reveal **Show why it happens** to see the contact-point explanation.
6. Explore slow motion, force arrows, lever arms, inner radius, mass and inertia.

The default two-second trial gives 1.40 m for the top string and 0.60 m for
the lower string. The top case has lever arm R+r about the ground contact;
the lower case has R-r. Both distances are positive.

## Model and controls

- Fixed-radius, rigid spool; massless string; horizontal pull; no slipping.
- Exact constant-force integration, with translation and rotation coupled by
  theta = -x/R. The string-end movement is consistent with winding/unwinding.
- Releasing the pull removes the force; the ideal spool coasts.
- A two-second trial freezes for inspection. Finite string or track limits can
  end a trial early at extreme settings.
- Forces, mass, radii and inertia can be changed. Parameter changes reset trials.
- Space: hold to pull; P: pause/resume; R: reset; N: small pull.
- Drag the view to orbit, scroll to zoom, or choose Side view.
- Angled pulling, slipping, lift-off, stretch and string-layer growth are excluded.

## Hosting and local use

All application code is in `index.html`. No build step, database, API key or
OpenAI hosting is required. Three.js and OrbitControls both use version
0.180.0 from jsDelivr. Viewers need internet and a browser with WebGL 2.

This folder is served by the existing GitHub Pages configuration on `main`.
For another static host, upload `index.html` as the entry file.

For optional Windows local preview, run `py -m http.server 8000 --bind 127.0.0.1`
in this folder and open http://localhost:8000/.

## Physics reference

UMass Amherst, Walking the Spool:
https://people.umass.edu/plecprep/mech/1k1030.html
