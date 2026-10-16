# Pixel-art and animation QA

Use machine checks for objective constraints and human visual review for design quality. A passing color count or pixel grid does not prove an asset looks good.

## Objective checks

- Confirm native dimensions, visible bounds, transparency type, palette size/membership, and source/output correspondence.
- Inspect edge pixels for unintended antialiasing, semi-transparent halos, gradients, or resampling artifacts. Preserve intentional soft effects when the art brief calls for them; do not force all effects into binary alpha.
- Ensure the enlargement preview uses nearest-neighbor sampling and an integer scale. Never use that preview as the source asset.
- For spritesheets, validate frame count/order and each cell's independent bounds. Prefer independently exported frames when unsafe gutters, overlaps, or ambiguous body-part ownership could cause neighboring-frame leaks.
- Preserve anchor conversions when padding or canvas bounds change. Track foot/contact, head, hand/grip, or effect-origin anchors as appropriate.
- For animation, compare adjacent frames and the loop for scale pops, palette drift, detached limbs/props, silhouette flicker, and accidental frame contamination. Airborne frames may naturally move the feet; do not force a constant baseline.

## Human review

At 1x, check subject recognition, silhouette, pose readability, and whether important details survive intended display. At enlarged native pixels, inspect cluster shape, outline consistency, stray pixels, corner rhythm, and value/material grouping. In-engine, check compositing against actual backgrounds, movement/camera sampling, and animation playback.

Keep reports separate: record automatic findings, visual findings, engine/context findings, and untested assumptions. Do not claim an animation or engine integration passed based only on a static sheet.
