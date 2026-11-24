# Redline Rush

An endless night-highway racer by **Obi Promise** (CSC 131).

**Play:** https://obipromise.github.io/redline-rush/ (best on a phone held sideways)

Weave through traffic on a neon city highway as the speed climbs from 90 to 300 km/h. Skim past cars for near-miss combos, fill the nitro bar, and see how far you get.

## Controls

| | Phone | Keyboard |
|---|---|---|
| Steer | Tilt the phone like a steering wheel, or hold the left/right side of the screen | ← → or A / D |
| Nitro | Hold NITRO | Space or ↑ |
| Pause | Pause button (also re-centres tilt) | Esc or P |

## Scoring
- Distance earns points, scaled by speed
- A **near miss** (passing a car within 90 cm) gives 150 × combo points, doubled under 40 cm, and refills nitro
- Combos go up to ×5 if you chain near misses within 3.5 seconds

## Tech
One HTML file using JavaScript and Three.js.
- The player stays at z = 0 and the world scrolls past, so the road never ends and number precision never drifts.
- Cars are curved extruded side profiles at real size (4.5 m sedans, 12.6 m trucks).
- Street lamps and buildings are instanced meshes recycled on a 560 m loop.
- Every light glow on screen is one additive point cloud, drawn in a single call.
- Rendering is capped at 60 fps. There are no shadow maps, and the pixel ratio is capped for battery life.
