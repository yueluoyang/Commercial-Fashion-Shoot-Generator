# Color Variant Workflow

Use this workflow only after the first four-image gallery has been generated and the user explicitly confirms it is fully correct. This rule still applies when the user uploaded color-variant references at the beginning of the workflow.

## Early Variant References

When the user provides base product references and additional colorway references in the same request:

- Identify which images define the first-batch/base color and which images are queued future color variants.
- If the base color is ambiguous, ask which color should be the first four-image sample before recommending sets or writing scripts.
- Use queued color references during indoor set planning only to choose a room palette, props, and small accent colors that can harmonize with all known colorways.
- Do not generate any variant image before the first-batch script is confirmed, the first four-image sample is generated, and the user confirms that sample is fully correct.
- Do not ask the user to re-upload queued color references after first-batch approval; summarize them and ask whether to proceed with those queued colors.
- Use queued color references only for garment color and color-dependent material behavior. Preserve garment construction from the approved first-batch product references unless the user explicitly identifies a queued image as a missing construction reference.

## Satisfaction Gate

After the first batch is delivered:

1. Ask whether the user is satisfied with all four images.
2. If the user wants corrections, ask for the exact image and issue when needed.
3. Correct only the specified issue. Keep the same model, same fixed body proportions, same base set, same garment construction, same approved script, same 3:4 ratio, and GPT Image 2.0/image_gen workflow.
4. Ask for satisfaction again after corrections.
5. Do not ask about color variants until the user says the first batch is fully correct.

## Color Variant Gate

After full confirmation, ask whether the user wants color variants.

If yes:

- Ask the user to upload product reference image(s) for each additional color only when no queued variant references exist or when a queued reference is unclear.
- If possible, request front and back references for each color. If only one color reference is available, use it only for color and material color behavior, while preserving garment construction from the approved original product references.
- Ask whether the user wants to keep the base indoor set exactly the same or allow small color-matched prop/decor adjustments.
- For each color, propose a concise color-variant plan before generation:
  - target color and undertone
  - any color-specific fabric behavior
  - unchanged garment construction
  - unchanged model/body lock
  - same four-shot script structure
  - optional small prop/decor adjustment, if allowed

## Variant Generation Rules

For every color variant:

- Generate exactly four 3:4 images: 正面图, 背面图, 细节特写图, 创意特性图.
- Use GPT Image 2.0 through the built-in image generation workflow.
- Preserve the same model identity and the fixed body proportions: 1.68m height, 7.5-head ratio, 0.64 leg-length ratio.
- Preserve the same base indoor set and approved four-shot script structure.
- Preserve the same styling-completion logic and footwear rule. Unless the user explicitly requested barefoot styling, the model must wear suitable shoes.
- Preserve the exact garment construction: silhouette, neckline, sleeve/strap design, length, hem, seams, ruffles, pleats, closures, fabric type, and decorative details.
- Change only the garment color and color-dependent fabric appearance based on the new color reference.
- Allow only small prop/decor changes when the user approves them. Examples: flower color, small vase color, fabric accent, small decorative object, or greenery tone. Do not change architecture, major furniture, camera angle logic, model styling, script purpose, or room identity.
- Continue to follow `shooting-script-guide.md`: the color variant must still serve the product's physical selling point and ecommerce logic.

## Output Pattern

For multiple colors, organize work by color:

```markdown
Color variant: <target color>
- Reference images used: <front/back/other>
- Set adjustment: <none or small prop/decor change>
- Four images generated:
  - 正面图: <path>
  - 背面图: <path>
  - 细节特写图: <path>
  - 创意特性图: <path>
```

After each color batch, ask whether the user wants corrections for that color before moving to the next color when practical.
