# Design System Strategy: The Midnight Alchemist

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Midnight Alchemist."** 

This system rejects the sterile, functionalist "SaaS" aesthetic in favor of a high-end editorial experience that feels like a private, invitation-only lounge. We are moving away from the "app" look and toward a "digital artifact" look. The design breaks the traditional template through intentional asymmetry—placing oversized, dramatic serif typography behind or overlapping sharp, metallic product shots. We treat the screen not as a flat grid, but as a cinematic stage where depth is created through haze, smoke, and light rather than lines and boxes.

Everything is sharp. Everything is dark. Everything is intentional.

## 2. Colors
The palette is rooted in the depth of the night, using obsidian and matte black as a canvas for the "liquid light" of brushed gold and emerald.

*   **Primary (Brushed Gold):** `#f2ca50` is our light source. Use it for high-impact CTAs and moments of "alchemical" transformation.
*   **Tertiary (Emerald):** `#a8dac0` is the "low-light" accent. It represents the botanical soul of the brand. Use it for subtle status indicators or soft glows in the background haze.
*   **Surface Hierarchy (The Obsidian Stack):** 
    *   **Surface (Base):** `#131313` (Matte Black).
    *   **Surface-Container-Lowest:** `#0e0e0e` (True Obsidian). Use this to "recede" areas of the UI.
    *   **Surface-Container-Highest:** `#353534` (Polished Stone). Use this for elevated interactive elements.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. To separate the hero from a feature section, transition from `surface` to `surface_container_low`. If you feel a line is needed, you have failed to use the tonal scale correctly.

### The "Glass & Gradient" Rule
To achieve the "Cinematic Glow," use Glassmorphism for floating overlays. Apply `surface_container` colors at 60-80% opacity with a heavy `backdrop-filter: blur(20px)`. Main buttons should utilize a subtle linear gradient from `primary` (#f2ca50) to `primary_container` (#d4af37) at a 45-degree angle to mimic the sheen of brushed metal.

## 3. Typography
We use a high-contrast pairing to evoke a sense of heritage meeting modern precision.

*   **Display & Headlines (Newsreader):** This is our dramatic serif. It should be used at scale. Don't be afraid of `display-lg` (3.5rem) overlapping images. It conveys the "Editorial" authority of a luxury magazine.
*   **Body & Titles (Manrope):** This is our sharp, modern sans-serif. It provides the "technical luxury" feel. Use `body-md` for standard descriptions, ensuring generous letter-spacing (0.02em) to maintain an expensive, airy feel.
*   **Labels:** All labels (`label-md`) should be set in Uppercase with 0.1em tracking to mimic high-end fashion branding.

## 4. Elevation & Depth
In this system, depth is atmospheric, not structural.

*   **The Layering Principle:** Stacking is the new bordering. Place a `surface_container_highest` card on a `surface` background to create an immediate, sharp lift.
*   **Ambient Shadows:** If a floating element requires a shadow, it must be "The Golden Halo." Use a blur of 40px-60px with a 5% opacity of the `primary` (gold) color. This creates a glow rather than a shadow, making the element look like it is emitting light.
*   **The "Ghost Border" Fallback:** If accessibility requires a container boundary, use the `outline_variant` (#4d4635) at 15% opacity. This "Ghost Border" should be almost invisible, felt rather than seen.
*   **Sharpness:** The `Roundedness Scale` is strictly **0px**. Every corner in this system is a hard 90-degree angle. This evokes the precision of a high-end watch or a cut gemstone.

## 5. Components

### Buttons
*   **Primary:** Sharp 0px corners. Background is a gold metallic gradient. Text is `on_primary` (#3c2f00) in `label-md` (Uppercase).
*   **Secondary:** Ghost style. No background fill. `outline` (#99907c) at 20% opacity. On hover, the outline glows to 100% gold.
*   **Tertiary:** Text-only with a subtle emerald `tertiary` underline that expands from the center on hover.

### Input Fields
*   **Style:** No box. A simple 1px `outline_variant` line only at the bottom.
*   **State:** When active, the bottom line transitions to `primary` (gold) with a soft `primary_fixed_dim` outer glow.

### Cards & Lists
*   **Rule:** No dividers. Separate list items using `surface_container` shifts.
*   **Editorial Card:** Use an image-heavy layout where the text overlaps the image. Apply a `surface_container_lowest` gradient overlay at the bottom of images to ensure `on_surface` text remains readable.

### Signature Component: "The Haze Overlay"
Create a global background component that uses a radial gradient of `tertiary_container` (#8dbea5) at 10% opacity, moving slowly across the screen. This mimics shifting smoke and adds to the "Nightlife" mood without distracting from the UI.

## 6. Do's and Don'ts

### Do:
*   **Use Negative Space:** Luxury is the ability to waste space. Give your typography room to breathe.
*   **Asymmetry:** Place a small label in a corner balanced by a large heading in the opposite quadrant. 
*   **Cinematic Focus:** Use high-quality photography with deep blacks and high-contrast gold lighting.

### Don't:
*   **No Rounded Corners:** Ever. Not even for checkboxes.
*   **No Standard Grays:** If you need a gray, use a tinted obsidian from the `surface_container` scale. Pure gray is "cheap."
*   **No Generic Icons:** Icons should be ultra-thin (1pt stroke) and use the `primary` gold or `tertiary` emerald tokens.
*   **No Rapid Animations:** Transitions should be slow and "heavy," like smoke moving through a room (e.g., 500ms ease-in-out).