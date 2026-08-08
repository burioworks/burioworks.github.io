# burioworks Brand Kit v1 — Approved Master

This kit uses the green `B` from the approved Concept C board as the **authoritative master**.

## Critical rule

The shape, proportions, polygon boundaries, and color placement of the approved master are not
redesigned in this kit.

The `SVG` files in this package intentionally embed the approved raster master rather than
re-tracing it. This preserves the approved appearance exactly. They are not true vector redraws.

## Approved brand rules

- Brand name: `burioworks` — always lowercase.
- Symbol: uppercase polygonal `B`.
- Primary direction: green / teal.
- Polygon treatment: simple and relatively flat.
- Do not stretch, rotate, skew, redraw, or add additional facets.
- Do not add 3D depth, bevel, glow, or shadow to the mark.
- Product brands may have their own colors; the studio identity remains neutral + teal.

## Authoritative files

- `reference/approved-green-B-master.png`
- `logo/mark/burioworks-mark-approved-master.png`
- `reference/approved-concept-board.png`

If another export differs visually from the authoritative master, the master above wins.

## Folder contents

- `reference/` — approved source board and exact source crops.
- `logo/mark/` — approved mark and size exports.
- `logo/lockup/` — approved horizontal lockup extracted from the source board.
- `icons/` — approved icon tile and social icon sizes.
- `web/` — favicon/PWA assets and brand color tokens.
- `docs/` — quick guide and contents list.

## Note on vectorization

A true path-based SVG is intentionally excluded from v1. Producing one requires a separate
trace-and-overlay validation pass so that the approved geometry is not altered.

## True vector masters

Path-based production SVGs are now included:

- `logo/mark/burioworks-mark-vector.svg`
- `logo/mark/burioworks-mark-vector-monochrome-dark.svg`
- `logo/mark/burioworks-mark-vector-monochrome-light.svg`
- `logo/lockup/burioworks-horizontal-lockup-vector.svg`
- `logo/lockup/burioworks-horizontal-lockup-vector-dark-background.svg`
- `logo/lockup/burioworks-horizontal-lockup-vector-monochrome.svg`

These files are true vector SVGs built from paths.
The approved green Concept C mark remains the visual source of truth.
