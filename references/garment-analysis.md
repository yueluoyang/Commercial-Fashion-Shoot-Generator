# Garment Analysis

Use this only as a supporting checklist inside the fused multimodal product analysis in `shooting-script-guide.md`. Do not run it as a separate workflow stage before the guide-based product analysis. The goal is to create a tight invariant list that can be repeated in every image prompt.

## Analysis Checklist

- Category: dress, blouse, skirt, pants, suit, outerwear, knitwear, set, etc.
- Color: exact color family and undertone; mention if lighting may shift it.
- Fabric and surface: matte, satin, chiffon, crepe, knit, ribbed, denim, lace, sheer, structured, fluid, stretch, heavy, lightweight.
- Silhouette: fitted, A-line, column, mermaid, wrap, oversized, cropped, high-waist, low-waist, straight, flared.
- Length: mini, knee, midi, ankle, floor, crop, longline.
- Neckline/collar: crew, V, square, asymmetric, halter, one-shoulder, shirt collar, stand collar, lapel.
- Sleeves/straps/armholes: sleeveless, cap, short, long, puff, slit, spaghetti straps, wide straps, dropped shoulder.
- Front construction: seams, waistline, darts, panels, ruffles, pleats, drape, gathers, pockets, buttons, zipper, belt, tie.
- Back construction: back neckline, straps, closures, seams, darts, slit, plain/ornate areas.
- Hem and side details: slit, scallop, raw edge, ruffle continuation, side seam, asymmetric hem.
- Styling boundaries: shoes and jewelry that are acceptable, and items that would distract or conceal the product.

## Garment Invariant Format

Use a compact invariant block in every final prompt:

```text
Garment invariants, must be exact: <color>; <fabric>; <silhouette>; <length>; <neckline>; <sleeves/straps>; <front construction>; <back construction when relevant>; <hem>; no <forbidden drift items>. Preserve the product construction exactly from the product references.
```

## Drift Risks

Call out details that image models often change:

- Asymmetric neckline becoming symmetric.
- Ruffle/flounce changing side, size, or starting point.
- Dress length shifting shorter or longer.
- Sleeveless garments gaining straps or sleeves.
- Plain backs gaining bows, cutouts, or zippers.
- Product color becoming white, beige, gray, or over-saturated.
- Extra belts, buttons, jewelry, bags, or jackets appearing.

Include these risks in the prompt as negative constraints when relevant.
