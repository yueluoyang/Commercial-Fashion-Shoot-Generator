# Shooting Script Guide

Use this guide after the user chooses the indoor set style and before any image generation. It is distilled from the user's womenswear AI shooting-script DOCX guide and adapted to this skill's fixed deliverables: front, back, dynamic candid/action, and detail close-up.

## Core Principle

Treat the four images as a conversion-oriented ecommerce sequence, not four isolated photos. Each shot must translate garment physics into visual selling value:

- Front product view: first-look trust, true color, full silhouette, exact front construction.
- Back product view: remove uncertainty about back cut, waist shaping, closures, seams, and hem.
- Dynamic candid/action view: the creative feature shot; amplify the strongest physical selling point through motion, pose, camera angle, or set interaction.
- Detail close-up: reduce the "cannot touch fabric online" problem through texture, stitching, drape, edge, and construction fidelity.

## RACE Planning Frame

Use this internal frame when writing the script:

- Role: act as a senior womenswear ecommerce visual director and fashion photographer.
- Action: convert the garment analysis into a four-shot commercial shooting plan.
- Context: honor the selected indoor set, online sales purpose, product invariants, and same-model/same-location constraints.
- Example logic: map fabric, cut, silhouette, and key details to camera, lighting, pose, and commercial purpose.

## Script Inputs

Before writing the script, carry forward:

- Garment category, silhouette, length, color, fabric, and construction invariants.
- Core product highlight or "physical selling point": ruffle, slit, drape, waist shaping, texture, sleeve volume, back detail, wide leg, etc.
- Selected indoor set style and its props/light.
- Drift risks that must be blocked during image generation.

## Four-Shot Logic

### 1. Front Product View

- Use eye-level, catalog-height framing.
- Prefer full-body or mid-long shot so neckline, waist, hem, and whole silhouette are readable.
- Keep the model's posture clean and centered.
- Use soft, low-contrast commercial light to preserve true color and fabric.
- Avoid hands, props, hair, or furniture covering key front details.

### 2. Back Product View

- Keep background and lighting visually continuous with the front view.
- Use back or slight side-back angle; optional gentle over-shoulder head turn only when it does not hide the back design.
- Show shoulder/strap/sleeve construction, back waist, darts or seams, closure area, skirt/pants back, and hem.
- Avoid inventing back bows, cutouts, exposed zippers, or extra closures.

### 3. Dynamic Candid/Creative Feature View

- Treat this as the shot that projects the wearing scenario and amplifies the garment's strongest selling point.
- Choose the action based on garment physics:
  - Slit or flowing hem: mid-step walk, gentle turn, skirt edge moving naturally.
  - Ruffle, drape, or flounce: soft hand movement or body turn that reveals layered edge and flow.
  - Wide-leg pants or long vertical lines: slightly lower camera angle and asymmetrical stride to enhance leg length and drape.
  - Knit, soft loungewear, or pajamas: relaxed indoor pose, stretch, seated/leaning gesture, morning light.
  - Structured tailoring: confident stance, architectural set interaction, clean lines.
- Keep the garment readable; avoid extreme motion blur or poses that distort construction.

### 4. Detail Close-Up

- Use close-up or macro-style framing with shallow depth of field.
- Choose the detail based on product value: neckline, ruffle edge, button, zipper, waist seam, sleeve cuff, pocket, stitching, fabric texture, hem, drape, or back closure.
- Use lighting based on material:
  - Knit, linen, cotton texture, tweed, rib, rough or raised surfaces: angled side light to reveal micro-shadows.
  - Silk, satin, glossy synthetic, smooth crepe: broad diffused light to avoid blown highlights while preserving sheen.
  - Sheer/chiffon/lace: backlight or soft side light to show translucency and edge detail.
- Hands may indicate scale or touch fabric lightly, but must not cover the detail being sold.

## Required Script Output

After set selection, output a concise script in this structure and ask for confirmation:

```markdown
### Garment Recap
<category, silhouette, color, fabric, core construction, core selling point>

### Generation Risk Notes
<details most likely to drift and must be locked>

### Four-Shot Shooting Script
| Deliverable | Composition / Camera | Scene & Lighting | Model Direction | Garment Detail Emphasis | Commercial Purpose |
|---|---|---|---|---|---|
| Front product view | ... | ... | ... | ... | ... |
| Back product view | ... | ... | ... | ... | ... |
| Dynamic candid/action view | ... | ... | ... | ... | ... |
| Detail close-up | ... | ... | ... | ... | ... |

Please confirm this shooting script, or tell me which shot to revise. I will generate images only after confirmation.
```

## Script Quality Rules

- Be specific enough that each row can become an image prompt without reinterpretation.
- Tie every pose, camera angle, and light choice to a garment property or sales purpose.
- Keep the selected indoor set consistent across all rows.
- Do not introduce props or actions that hide the product.
- Keep the user's original four deliverables and constraints unchanged.
