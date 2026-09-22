# Rendering contract

## Canvas

- 1080×1440, 30fps, white background
- Captions stay in the upper safe area
- Illustrations use `object-fit: contain`; never crop with `cover`

## Motion

- Direct-cut mode: `text → bw_full → color`
- Every layer reveals from left to right
- Page-flip mode: untouched static full master, followed by a bottom-right page curl; no extra caption or BW stages
- No camera shake, bounce, narration, or text-synchronized music

## Assets

- Generated and uploaded masters share `scripts/page-assets.mjs`; uploaded masters are copied into a content-addressed generated directory
- Text defaults to image-tool generated handwriting; inspect exact glyphs before import
- Direct cuts contain/pad caption and illustration plates; page flips preserve whole masters
- Private reference profiles/images live in ignored `.story-video/`, never in the built-in catalog
- Caption, black-and-white, and color plates share aligned canvases
- Generated assets and rendered videos are disposable runtime outputs

## Visual style

The following lock applies to the default diary style only. Other catalog styles and analyzed reference profiles have independent recipes. The catalog holds 297 styles + 30 palettes, with 30 curated default menu entries.

- Flat white paper
- Uneven felt-tip outlines and sparse wax-crayon color
- Generous negative space
- No realistic shading, glossy gradients, watermark, or paper texture
