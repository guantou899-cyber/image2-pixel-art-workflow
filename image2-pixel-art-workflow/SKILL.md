---
name: image2-pixel-art-workflow
description: Turn a visual reference into polished pixel art through deliberate redraw, rasterization to a chosen native grid, and pixel-cluster cleanup. Use for sprite, prop, effect, or animation creation; not for changing gameplay rules unless separately requested.
metadata:
  short-description: Redraw, rasterize, and refine pixel art
---

# Image-to-pixel-art workflow

Create pixel art that reads as intentionally designed at native resolution, not a high-resolution image with a pixel filter. Preserve the user's subject and visual goals while choosing a grid that fits its intended on-screen size.

## Workflow

1. Inspect the reference, target use, display size, camera scale, animation needs, and any existing art standard. Ask what native pixel size or density the user wants. If they are unsure, recommend a concrete starting specification based on the target display and reference art; briefly explain the tradeoff. Offer a small same-subject density comparison only when the choice is genuinely uncertain. If the user delegates the choice, decide and proceed.
2. Establish a compact art brief: visible dimensions at the native grid, palette range, outline treatment, contrast/material clusters, transparency, and (for animation) frame count, timing source, anchors, and loop requirements. Do not impose one character height or palette on unrelated art.
3. Use Image2 or another available image-generation/editing tool to redraw the reference toward the chosen pixel-art design. Treat the result as a redraw/concept stage, not automatically as final pixel art. Keep the source reference, prompt, generated redraw, and provenance together when practical.
4. Rasterize deliberately to the selected native grid. Use a repeatable local tool or script when useful, but avoid a blind resize-and-quantize pass as the finish. Inspect and manually refine contours, silhouette, pixel clusters, value grouping, palette, stray pixels, and edge transparency at native resolution. Keep small clusters purposeful; details must survive at intended display size.
5. For animation, keep a consistent grid, palette logic, scale, and anchor conventions. Review every frame and the loop at native size and integer nearest-neighbor enlargement. Prevent neighboring-frame contamination and record the source frame/timing relationship. Never infer or alter gameplay timing from the artwork.
6. Review the final asset in context: native-size preview, nearest-neighbor enlargement, and actual target-engine/app composite when available. Check both light and dark backgrounds where relevant. Report what was actually tested and what remains unverified.
7. Deliver the editable source where available, final assets, brief/specification, provenance, and concise QA notes. Do not replace production assets or publish externally unless the user explicitly authorized that scope.

## Research and tools

Online research and other available Skills may be used when they materially improve the result. Prefer primary documentation and inspect a third-party Skill/tool's source, license, dependencies, network behavior, write scope, and commands before installing or executing it. Do not install globally or run untrusted scripts just because a repository recommends them. Aseprite/LibreSprite or a local raster script are optional adapters, not prerequisites. State clearly when a tool was unavailable or not actually tested.

Image generation may redraw forms to improve pixel-art readability; do not promise that a prompt alone produces a compliant native pixel grid. Do not present an automatically reduced or filtered image as finished pixel art. Keep the high-resolution redraw and final rasterized/refined result distinguishable.

## Boundaries

Follow the user's current project instructions and permissions. Art authorization does not imply permission to change gameplay, collision, input, animation timing, levels, or production assets. For an existing game, preserve those unless the user explicitly allows a specific change. Do not copy another game's sprites or distinctive artwork; references may guide general craft such as silhouette clarity, cluster organization, contrast, and animation readability.

Read [references/spec-selection.md](references/spec-selection.md) when choosing a grid or palette, and [references/pixel-qa.md](references/pixel-qa.md) for animation/export review. Read [references/attribution-and-provenance.md](references/attribution-and-provenance.md) when sourcing third-party material or preparing a shareable package.
