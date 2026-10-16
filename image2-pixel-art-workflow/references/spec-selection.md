# Choosing a pixel-art specification

Pixel dimensions are a design decision tied to intended display size, not a universal character standard. First determine how large the asset appears in the game/app, whether it is animated, the camera's scaling/filtering, and how much pose or material detail must remain readable.

## Ask or recommend

- If the user has an established approved asset, use it as the visual-density and balance reference. Measure its visible source pixels and in-context display; do not infer a target from a padded PNG canvas.
- If the user knows the desired grid, follow it and note any readability tradeoff.
- If they do not know, recommend one starting grid and explain the expected look: coarser grids give stronger clusters and simpler silhouettes; finer grids permit facial/material detail but can become noisy at small display sizes.
- When the choice materially affects the style, compare two or three versions of the same pose/object at the same displayed size. Show native-size, nearest-neighbor enlargement, and context composite. Keep subject, pose, palette intent, and display scale constant so the comparison isolates density.
- If the user says to decide, do so without blocking and document the choice. Do not turn every refinement into another approval question.

## Record the brief

Record only the values needed for the work: native canvas/visible dimensions, intended display size and scale, palette budget or palette source, alpha/outline conventions, animation frame list and timing source, and important anchors. For animation, keep the grid and apparent body scale coherent while allowing poses to change silhouette and occupied height naturally.

Do not force every asset to a character's pixel height, a single canvas size, or the same palette. Match pixel density to the asset's world/display size and role. Avoid non-integer enlargement in the final display when crisp pixel edges are required, or explain the limitations of the existing camera/engine if changing it is out of scope.
