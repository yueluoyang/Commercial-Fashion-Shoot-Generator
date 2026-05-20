# Prompt Templates

Use these templates only after the user chooses the indoor set style and confirms the four-shot shooting script. Replace bracketed text. Keep all four prompts consistent.

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

Approved shooting script for this deliverable: [paste the confirmed row for this image: composition/camera, scene and lighting, model direction, garment detail emphasis, commercial purpose, and model proportion control]. Follow this approved script exactly unless it conflicts with garment preservation or the fixed model proportion lock; if conflict exists, garment preservation and fixed model proportions win.

Lighting/mood: [specific light], photorealistic high-fidelity commercial fashion photography, realistic skin and fabric texture, crisp product detail.

Constraints: same model identity in all images; fixed 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio in all images; same indoor set in all images; exact product garment preservation; approved shooting script; 3:4 vertical; no logos, no text, no watermark, no face mask, no color blob, no reference artifacts, no extra garments, no distracting accessories. Do not alter garment design or model body proportions in any way.
```

## 1. Front Product View

```text
[Shared Prompt Block]

Primary request: Create a full-body FRONT VIEW product display photo of the same model wearing the exact product garment.

Composition/framing: straight-on camera at fashion catalog height, full body visible including shoes and hem, model centered, clean posture, key front construction fully visible, body proportions locked to 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio. Use minimal neutral shoes if appropriate. Hands may rest naturally but must not cover neckline, waist, ruffle, seams, closures, or hem.
```

## 2. Back Product View

```text
[Shared Prompt Block]

Primary request: Create a full-body BACK VIEW product display photo of the same model wearing the exact product garment.

Composition/framing: straight camera at fashion catalog height, full back visible including shoulder/back construction, waist seam, back skirt, hem, and shoes, body proportions locked to 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio. The model may turn her head slightly over one shoulder for identity continuity, but the back construction must remain dominant and unobstructed.
```

## 3. Dynamic Candid View

```text
[Shared Prompt Block]

Primary request: Create a dynamic full-body commercial fashion photo of the same model wearing the exact product garment, interacting naturally with the chosen indoor set. Treat this as the approved creative feature shot: it must project the product's strongest wearing scenario or physical selling point.

Composition/action: three-quarter front or side-front view, full body visible, body proportions locked to 1.68m height, 7.5-head ratio, and 0.64 leg-length ratio. The model may walk, turn softly, touch a curtain, sit lightly on a stool edge, or interact with a flower/vase/furniture piece only if the garment construction remains readable. Add subtle movement in hair, fabric, or curtain; avoid extreme motion blur and avoid perspective distortion that lengthens legs or changes body ratio.
```

## 4. Detail Close-Up

```text
[Shared Prompt Block]

Primary request: Create a close-up product detail image of the same model wearing the exact product garment, emphasizing the garment's most important construction details: [neckline/seams/waist/ruffle/fabric/closure/texture].

Composition/framing: 3:4 vertical crop from [appropriate upper crop] to [appropriate lower crop]. Hands may lightly indicate scale or touch a seam/ruffle edge without hiding construction. Background remains the same chosen indoor set, softly blurred. Keep fabric, stitching, drape, and edge details sharp.
```

## Iteration Prompts

If a generated image drifts, correct one issue at a time:

```text
Revise only [specific issue]. Keep the same model, fixed 1.68m height, 7.5-head ratio, 0.64 leg-length ratio, same indoor set, same lighting, same approved shooting script, same pose category, 3:4 ratio, and all garment invariants unchanged. The garment must match the product references exactly, especially [critical details].
```
