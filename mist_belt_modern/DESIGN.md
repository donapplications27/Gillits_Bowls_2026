# Design System Specification: The Mist-Belt Collective

## 1. Overview & Creative North Star: "Atmospheric Precision"
This design system moves away from the dusty, traditional aesthetic of lawn bowls and pivots toward a high-energy, premium sporting lifestyle. Our Creative North Star is **"Atmospheric Precision."** 

We draw inspiration from the Winston Park mist-belt—where the sharp, technical lines of a world-class bowling green meet the soft, ethereal diffusion of KwaZulu-Natal mist. To achieve this, the design system rejects the "boxed-in" layout of standard web templates. Instead, we embrace an editorial approach: intentional asymmetry, oversized typography, and a layering system that feels like physical sheets of glass and light. We are not just building a club website; we are designing a digital clubhouse for the future of B20 Cricket Bowls.

---

## 2. Colors: Tonal Immersion
The palette is a sophisticated range of "Mist-Belt Greens." We avoid flat, lifeless colors by utilizing the Material 3 tonal range to create a sense of depth and environment.

*   **Primary (`#176a21`) & Secondary (`#246830`):** These are our "Green-on-Green" signatures. Use the Primary for high-action touchpoints and the Secondary for prestige elements.
*   **The "No-Line" Rule:** Sectioning must never be achieved with 1px solid borders. To separate content, use a background shift from `surface` to `surface-container-low`. The transition is the boundary.
*   **Surface Hierarchy & Nesting:** Treat the UI as a series of nested layers. 
    *   *Example:* A `surface-container-lowest` card (pure white/off-white) should sit atop a `surface-container` section to create a natural, organic lift.
*   **The Glass & Gradient Rule:** For hero sections and primary CTAs, use a linear gradient transitioning from `primary` to `primary-container`. For floating navigation or modal overlays, apply a **Glassmorphic effect**: use `surface` at 70% opacity with a `20px` backdrop-blur. This mimics the Winston Park mist, allowing underlying content to bleed through softly.

---

## 3. Typography: The Energetic Editorial
We utilize **Lexend** for its pioneering, rhythmic geometry and **Plus Jakarta Sans** for its high-end, clean readability.

*   **Display (Lexend, 3.5rem - 2.25rem):** These are our "shout" moments. Use `display-lg` for impactful headlines about B20 Cricket Bowls. Character spacing should be slightly tight (-2%) to feel modern and aggressive.
*   **Headline & Title (Lexend, 2rem - 1rem):** Used for section headers. Always pair a `headline-lg` with a `body-md` in a wide, asymmetrical layout to create "breathing room."
*   **Body (Plus Jakarta Sans, 1rem - 0.75rem):** Our workhorse. It provides a technical, premium feel that balances the energetic Lexend headlines.
*   **Label (Lexend, 0.75rem):** Use for technical stats (e.g., bowl speed, scoreboards). All labels should be uppercase with +5% letter spacing for a "pro-sport" aesthetic.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are too heavy for this "misty" aesthetic. We define depth through light and tint.

*   **The Layering Principle:** Depth is achieved by stacking. A `surface-container-highest` element (the "closest" to the user) should only be used for the most critical interactive components.
*   **Ambient Shadows:** If a shadow is required for a floating action button, use the `on-surface` color at 6% opacity with a 32px blur and a 16px Y-offset. It should feel like a soft glow, not a dark edge.
*   **The "Ghost Border" Fallback:** In rare cases where a border is needed for accessibility (e.g., input fields), use `outline-variant` at 15% opacity. Never use 100% opaque outlines.
*   **Glassmorphism:** Use `surface-variant` with 60% opacity and a heavy backdrop-blur for headers that stick to the top of the page as the user scrolls, creating a "frosted glass" transit through the mist.

---

## 5. Components: The Social Primitives

### Buttons
*   **Primary:** High-energy. `primary` background with `on-primary` text. Use `xl` (1.5rem) roundedness to lean into the "pioneering" personality.
*   **Secondary:** The "Mist" variant. `secondary-container` background with `on-secondary-container` text.
*   **Interaction:** On hover, buttons should scale 2% and transition to a subtle gradient fill.

### Cards & Lists
*   **The "No-Divider" Rule:** Forbid the use of horizontal lines between list items. Instead, use a `16px` vertical gap and a subtle background change (`surface-container-low`) on hover to indicate interactivity.
*   **The "B20 Card":** A `surface-container-lowest` card with `lg` (1rem) corner radius. Use an asymmetrical layout: Image on the left, oversized `title-lg` on the right, bleeding slightly off the grid.

### Chips (Game Modes & Status)
*   Use `tertiary-container` for B20-specific tags to distinguish them from standard club news. They should feel like "badges of honor."

### Input Fields
*   **State:** Unfocused inputs use `surface-container-high` as a solid fill with no border. On focus, the background shifts to `surface` and a `2px` `primary` "glow" (not a border) appears at the bottom edge only.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use extreme white space. The "mist-belt" vibe requires air.
*   **Do** overlap elements. Have a headline partially cover a high-quality photograph of the greens to create depth.
*   **Do** use "Mist-Belt" imagery—dew on grass, soft morning light, and vibrant green textures.

### Don't:
*   **Don't** use black (`#000000`). Use `on-surface` (`#2a3127`) for all "dark" text to maintain the organic green undertone.
*   **Don't** use sharp 90-degree corners. Everything must feel approachable and inclusive; use the `DEFAULT` (0.5rem) or `lg` (1rem) roundedness scale.
*   **Don't** use standard grid layouts for galleries. Use a masonry or staggered approach to reflect the "social and dynamic" nature of the club.