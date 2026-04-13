```markdown
# Design System Strategy: The Alpine Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Refined Alchemist."** It is a visual language that balances the raw, rugged textures of nature with the precision of high-end editorial print. We are moving away from the "template" look of standard wellness sites to create an experience that feels like a curated journey through a luxury spa hidden within a primeval forest.

This system breaks the rigid digital grid through **Intentional Asymmetry**. We utilize generous white space (negative space as a luxury) and overlapping elements where typography breaks across image boundaries. The goal is to make the user feel they are turning the pages of a high-end physical monograph, not scrolling through a generic database.

---

## 2. Colors & Tonal Depth
The palette is rooted in deep forest greens (`primary: #062a05`), rich earth tones (`secondary: #934b19`), and a sophisticated off-white base (`background: #fafaf5`).

*   **The "No-Line" Rule:** We do not use 1px solid borders to define sections. Structural boundaries are achieved exclusively through shifts in background color. For example, a `surface-container-low` section should sit directly against a `surface` background to denote a change in content without the "boxiness" of lines.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers of fine paper. Use `surface-container-lowest` for cards that need to "pop" off a `surface-container-low` section. This creates a natural, soft depth that feels premium and tactile.
*   **The "Glass & Gradient" Rule:** For floating navigation or modal overlays, use **Glassmorphism**. Apply `surface` at 70% opacity with a `24px` backdrop-blur. 
*   **Signature Textures:** Main CTAs and Hero sections should avoid flat fills. Instead, use a subtle linear gradient (135°) transitioning from `primary (#062a05)` to `primary-container (#1d4118)`. This adds a "soul" to the color, mimicking the way light hits moss or deep water.

---

## 3. Typography
Our typography is a dialogue between the authoritative weight of **Noto Serif** and the modern, breathable clarity of **Work Sans**.

*   **Display & Headlines (Noto Serif):** Used for storytelling. `display-lg (3.5rem)` should be used with tight letter-spacing (-0.02em) to create an editorial, high-fashion impact.
*   **Body & Labels (Work Sans):** Used for utility. These are set with generous leading (1.6x) to ensure the heavy weight of the serif headlines is balanced by "breathing room" in the copy.
*   **Identity through Scale:** We use a high-contrast scale. A very large `headline-lg` paired with a significantly smaller, all-caps `label-md` creates an intentional hierarchy that signals premium curation.

---

## 4. Elevation & Depth
In this design system, shadows are a last resort. We prioritize **Tonal Layering**.

*   **The Layering Principle:** Depth is "stacked."
    *   *Base:* `surface` (#fafaf5)
    *   *Section:* `surface-container-low` (#f4f4ef)
    *   *Card:* `surface-container-lowest` (#ffffff)
*   **Ambient Shadows:** If an element must float (e.g., a primary action button), use a shadow with a `20px` blur, `0%` spread, and `6%` opacity. The shadow color must be a tinted `primary-fixed-dim` rather than pure black to keep the light feeling "organic."
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline-variant` at **15% opacity**. This creates a suggestion of a container rather than a hard cage.
*   **Glassmorphism:** Use semi-transparent `surface-variant` layers for utility elements like search bars or filters to allow the lush background photography to bleed through, softening the interface.

---

## 5. Components

### Buttons
*   **Primary:** Gradient fill (`primary` to `primary-container`), `roundness-md`, `label-md` text in all-caps with `0.1rem` letter spacing. No border.
*   **Secondary:** Ghost style. Use the "Ghost Border" (15% opacity `outline-variant`) with `on-surface` text.
*   **Tertiary:** Text only, with a 2px underline in `secondary` color that expands on hover.

### Cards & Lists
*   **The Rule of Zero Dividers:** Forbid the use of horizontal rules. Separate list items using the spacing scale (`spacing-4` or `spacing-6`).
*   **Editorial Cards:** Images should have a slight `roundness-sm`. Text should overlap the image slightly using a negative margin to break the "contained" look.

### Input Fields
*   **Refined Inputs:** No background fill. Only a bottom border using `outline-variant` (20% opacity). On focus, the border transitions to `primary` and thickens to 2px.

### Additional Components: The "Aperture" Image
*   A custom component for this system: An image masked in an asymmetrical organic shape (using `roundness-xl` on three corners and `none` on one) to mimic a window view into the spa/nature.

---

## 6. Do's and Don'ts

### Do:
*   **Use Intentional Asymmetry:** Offset text blocks from the center of images to create a "crafted" feel.
*   **Embrace the White Space:** Use `spacing-20` and `spacing-24` between major sections to let the design breathe.
*   **Tone-on-Tone:** Use `on-surface-variant` for secondary text to keep the visual noise low.

### Don't:
*   **No Hard Shadows:** Never use high-opacity or dark grey shadows; they look "cheap" and digital.
*   **No Standard Grids:** Avoid the "3-column card row" whenever possible. Try a 2/3 and 1/3 split to maintain the editorial edge.
*   **No High-Contrast Borders:** Never use `outline` at 100% opacity for boxes. It kills the "The Refined Alchemist" aesthetic.
*   **No System Fonts:** Always ensure **Noto Serif** and **Work Sans** are loaded; fallback sans-serifs will break the premium tone.```