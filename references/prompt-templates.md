# Prompt Templates

Use these templates only after the user chooses the indoor set style and confirms the four-shot shooting script. The confirmed script must contain 正面图, 背面图, 细节特写图, and 创意特性图. Replace bracketed text. Keep all four prompts consistent.

## Shared Prompt Block

```text
Use case: identity-preserve commercial womenswear photography.
Asset type: online fashion product gallery, 3:4 vertical portrait.

Input images:
- Image 1: model identity reference. Preserve the same model identity, face, skin tone, hair, makeup mood, and premium catalog presence while standardizing the body to the fixed model proportion lock.
- Image 2: product front reference. Use for exact front garment construction.
- Image 3: product back/side reference. Use for exact back and side garment construction.

Fixed model proportion lock: the model is 1.68m tall, with a 7.5-head head-to-body ratio and a 0.64 leg-length ratio, where lower-body length from navel/pubic symphysis to floor divided by height equals 0.64. Keep these proportions consistent across all four images. Do not elongate legs, shrink the head, stretch the torso, use extreme low-angle distortion, or otherwise alter these proportions.

Scene/backdrop: [chosen indoor set style, same for all four images]. Keep the same room, props, light direction, seasonal mood, and color palette across the complete four-image gallery.

[Garment invariant block from garment-analysis.md]

Approved shooting script for this deliverable: [paste the confirmed row for this image: 主图序号; 构图、景别与机位角度; 空间场景与环境布光; 模特调度（肢体动作与细节展现）; 视觉呈现目的]. Follow this approved script exactly unless it conflicts with garment preservation or the fixed model proportion lock; if conflict exists, garment preservation and fixed model proportions win.

Lighting/mood: [specific light], photorealistic high-fidelity commercial fashion photography, realistic skin and fabric texture, crisp product detail.

Constraints: same model identity in all images; fixed 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio in all images; same indoor set in all images; exact product garment preservation; approved shooting script; 3:4 vertical; no logos, no text, no watermark, no face mask, no color blob, no reference artifacts, no extra garments, no distracting accessories. Do not alter garment design or model body proportions in any way.
```

## 1. Front Image

```text
[Shared Prompt Block]

Primary request: Create the 正面图 / front image from the approved script: a full-body or mid-long front-view product display photo of the same model wearing the exact product garment.

Composition/framing: straight-on camera at fashion catalog height, full body visible including shoes and hem, model centered, clean posture, key front construction fully visible, body proportions locked to 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio. Use minimal neutral shoes if appropriate. Hands may rest naturally but must not cover neckline, waist, ruffle, seams, closures, or hem.
```

## 2. Back Image

```text
[Shared Prompt Block]

Primary request: Create the 背面图 / back image from the approved script: a full-body or mid-long back-view product display photo of the same model wearing the exact product garment.

Composition/framing: straight camera at fashion catalog height, full back visible including shoulder/back construction, waist seam, back skirt, hem, and shoes, body proportions locked to 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio. The model may turn her head slightly over one shoulder for identity continuity, but the back construction must remain dominant and unobstructed.
```

## 3. Detail Close-Up

```text
[Shared Prompt Block]

Primary request: Create the 细节特写图 / product detail close-up from the approved script. The image must emphasize material texture, stitching, edge finish, drape, closure, neckline, cuff, pocket, ruffle, hem, or whichever construction detail the approved script identifies.

Composition/framing: 3:4 vertical close-up or macro-style crop defined by the approved script. Use material-appropriate lighting: angled side light for textured knit/linen/tweed/rib surfaces; broad diffused light for silk/satin/glossy smooth fabrics; soft backlight or side light for sheer/chiffon/lace. Hands may lightly indicate scale or touch fabric only if they do not hide the selling detail.
```

## 4. Creative Feature View

```text
[Shared Prompt Block]

Primary request: Create the 创意特性图 / creative feature image from the approved script. This is the core scene-mindset projection shot, designed to amplify the garment's strongest physical selling point through scene, camera, lighting, model posture, and controlled motion when appropriate.

Composition/action: follow the approved script's product-specific creative logic. For loungewear, use relaxed morning-home gestures; for slit or large-hem garments, use a breezy forward stride or controlled turn that reveals the moving hem/slit; for wide-leg/high-waist trousers, use a controlled 15-30 degree low angle only if it does not violate the fixed body proportion lock; for other products, stage the strongest physical creative point. Keep the garment readable, keep the same indoor set, avoid generic posing, avoid extreme motion blur, and avoid perspective distortion that changes the 1.68m / 7.5-head / 0.64 leg-ratio body.
```

## Iteration Prompts

If a generated image drifts, correct one issue at a time:

```text
Revise only [specific issue]. Keep the same model, fixed 1.68m height, 7.5-head ratio, 0.64 leg-length ratio, same indoor set, same lighting, same approved shooting script, same pose category, 3:4 ratio, and all garment invariants unchanged. The garment must match the product references exactly, especially [critical details].
```

## Color Variant Prompt Add-On

Use this add-on only after the first batch is fully confirmed by the user and the user provides additional color reference image(s).

```text
Color variant mode: create the [target color name] version of the approved four-image gallery.

Additional input image(s): use the color-variant product reference only to capture the new garment color, fabric color behavior, and any color-specific material appearance. Do not copy a different model, pose, background, face, body, or styling from the color reference.

Keep unchanged: same model identity as the approved first batch; fixed 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio; same base indoor set; same four-shot script structure; same garment silhouette, neckline, sleeves/straps, length, seams, ruffles, pleats, closures, hem, and construction details; same 3:4 vertical ratio; same commercial ecommerce polish.

Allowed optional scene adjustment: if the user approved color-matched set tweaks, adjust only small props or decorative accents such as flowers, vase color, textile accent, small object color, or greenery tone so the set harmonizes with the new garment color. Do not change the room architecture, main furniture, camera logic, lighting continuity, or shot purpose.

Color accuracy: match the target color reference faithfully while preserving realistic fabric texture and lighting. Avoid hue drift, invented patterns, extra trims, extra accessories, or changing the garment design.
```
