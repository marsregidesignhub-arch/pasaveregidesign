# Design System Strategy: The Architectural Authority

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Architectural Authority."** 

To move beyond the generic "business template," we treat digital space like a high-end physical office—composed of heavy, premium materials, intentional light play, and expansive breathing room. We reject the "flat" web. Instead, we embrace **Intentional Asymmetry** and **Tonal Depth**. By shifting elements off the rigid center-axis and using overlapping layers, we create a sense of movement and bespoke craftsmanship that signals a "Regidesign" (Registry + Design) level of precision.

## 2. Colors: Tonal Depth & The No-Line Rule
Our palette is rooted in the depth of `primary` (#00352c) and the clarity of `surface` (#f8fafb). 

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections. Layout boundaries must be achieved through background shifts.
*   **Example:** A hero section in `surface` transitions into a feature section using `surface-container-low` (#f2f4f5). The change in tone is the "line."

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked sheets of fine stationery.
*   **Base:** `surface` (#f8fafb)
*   **Secondary Content:** `surface-container-low` (#f2f4f5)
*   **Interactive Containers:** `surface-container-lowest` (#ffffff) sitting atop a lower tier to create a natural, "lifted" look without traditional shadows.

### Signature Textures
To inject "soul" into the business environment, use **The Deep Gradient**. For primary CTAs or Hero Backgrounds, transition from `primary` (#00352c) to `primary_container` (#024e41) at a 135-degree angle. This prevents the teal from feeling "muddy" and adds a subtle, silk-like sheen.

## 3. Typography: Editorial Authority
We utilize a dual-font system to balance corporate reliability with high-end editorial flair.

*   **Display & Headlines (Manrope):** Chosen for its geometric precision. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero statements to command authority.
*   **Body & Labels (Inter):** The workhorse. Inter provides maximum readability in complex business data. 
*   **The Hierarchy Shift:** Maintain a high contrast between `headline-lg` and `body-md`. This "Large-Small" pairing mimics premium print magazines, making the content feel curated rather than just "displayed."

## 4. Elevation & Depth: Atmospheric Perspective
We eschew the standard "drop shadow" in favor of **Tonal Layering** and **Ambient Light**.

### The Layering Principle
Depth is achieved by stacking. A card using `surface-container-lowest` (#ffffff) placed on a background of `surface-container` (#eceeef) creates a perceived 2dp elevation purely through color contrast.

### Ambient Shadows
When a floating effect is required (e.g., a hovered card), use an "Atmospheric Shadow":
*   **Blur:** 40px to 60px.
*   **Opacity:** 4% - 6%.
*   **Color:** Use a tinted version of `on-surface` (#191c1d) rather than pure black to simulate natural light refraction.

### Glassmorphism & Ghost Borders
For the sticky header, use a backdrop-blur (12px) with a 70% opacity `surface` fill. 
*   **Ghost Border:** If a separator is required for accessibility, use the `outline-variant` (#bfc8c8) at 15% opacity. It should be felt, not seen.

## 5. Components

### Modern Cards
*   **Base:** `surface-container-lowest` (#ffffff).
*   **Corner Radius:** `xl` (0.75rem) for a modern, approachable feel.
*   **Interaction:** On hover, the card should translate -4px Y-axis and transition its background to a subtle gradient of `surface-container-lowest` to `surface-container-low`. 
*   **Content:** No dividers. Use `Spacing 6` (1.5rem) to separate header text from body text.

### Sleek Buttons
*   **Primary:** Background `primary` (#00352c), Text `on-primary` (#ffffff). Use `Roundedness: full` for a "pill" shape that contrasts against the architectural grid.
*   **Secondary:** Background `secondary_container` (#a3ecf0), Text `on-secondary-container` (#1b6d71). 
*   **Hover State:** A subtle scale-up (1.02x) and a shift to a slightly brighter `surface_tint`.

### The Sticky Header
*   **Height:** `Spacing 20` (5rem).
*   **Style:** Glassmorphic fill (70% `surface`). 
*   **Layout:** Use asymmetrical spacing. Logo on the far left, navigation clustered toward the right, with the primary CTA isolated by a `Spacing 10` margin to ensure it draws the eye immediately.

### Input Fields
*   **State:** Default state uses `surface-container-high` (#e6e8e9) with no border.
*   **Focus:** Transitions to `surface-container-lowest` with a `Ghost Border` using `primary`. This "glow-in" effect feels more premium than a simple color change.

## 6. Do’s and Don’ts

### Do:
*   **Use Overlays:** Allow images to slightly overlap container edges to break the "boxed-in" feel.
*   **Embrace White Space:** Use `Spacing 24` (6rem) between major sections to signal luxury and breathing room.
*   **Tint Your Greys:** Always use the `surface` tokens which are slightly tinted teal/blue, ensuring the design never feels "cold" or "dead."

### Don’t:
*   **Don’t use 100% Black:** Never use #000000. Use `on-surface` (#191c1d) for all text to maintain a high-end, ink-on-paper look.
*   **Don’t use Dividers:** Avoid horizontal rules (`<hr>`). Use a `Spacing 8` gap or a subtle tone shift instead.
*   **Don’t Crowd the Edge:** Ensure a minimum of `Spacing 6` (1.5rem) internal padding for all cards and containers.