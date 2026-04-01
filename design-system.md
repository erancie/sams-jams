```markdown
# Design System Strategy: The Sonic Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Neon Pulse"**
This design system moves away from the static, boxy constraints of traditional web interfaces and instead embraces the fluidity of sound. We are not building a database; we are building a stage. The goal is "Sonic Editorial"—a high-end digital experience that feels like a premium music magazine brought to life through kinetic energy and light.

To achieve this, we break the "template" look through **Intentional Asymmetry**. Hero sections should utilize overlapping elements where typography breaks the bounds of image containers. We treat the screen as a canvas of light, using high-contrast scales and deep tonal depth to guide the user’s eye through the "rhythm" of the content.

---

## 2. Colors & Light Theory
Our palette is a high-octane mix of deep midnight foundations and electrified accents.

*   **Foundation:** The `surface` (`#0e0e13`) acts as our "silence." It is deep and absolute, allowing the `primary` (Electric Purple) and `secondary` (Neon Cyan) to vibrate against it.
*   **The "No-Line" Rule:** Direct sectioning with 1px solid borders is strictly prohibited. We define space through "Tonal Carving." A section is distinguished by shifting from `surface` to `surface-container-low` or `surface-bright`.
*   **Surface Hierarchy & Nesting:** Treat the UI as layers of glass.
    *   **Level 0 (Background):** `surface-dim`
    *   **Level 1 (Sections):** `surface-container`
    *   **Level 2 (Cards/Interaction):** `surface-container-high`
*   **The "Glass & Gradient" Rule:** Use `primary` to `primary-container` gradients for interactive states. For floating elements, use a `surface-variant` with a 60% opacity and a 20px backdrop-blur to create a "frosted" look that lets the "neon pulse" of background glows bleed through.
*   **Signature Textures:** Apply a subtle grain overlay on `surface-container-lowest` to mimic the tactile feel of vinyl or high-end print.

---

## 3. Typography: The Visual Voice
We use typography as a rhythmic instrument.

*   **Display & Headlines (Epilogue):** This is our "Lead Vocal." Used for discovery titles and artist names. It is bold, expressive, and unapologetic. Use `display-lg` for hero moments, allowing letters to track tightly for a "poster" aesthetic.
*   **Body (Manrope):** This is our "Rhythm Section." It provides the steady beat. It is highly legible and clean, ensuring that even in a vibrant environment, the content remains the priority.
*   **Labels (Space Grotesk):** Our "Percussion." Used for data points, rankings, and metadata. The monospaced-leaning vibe of Space Grotesk adds a technical, "studio equipment" feel to the discovery process.

---

## 4. Elevation & Depth
In this design system, elevation is conveyed through **Tonal Layering**, not structural shadows.

*   **The Layering Principle:** To lift a video card, do not add a black shadow. Instead, place the `surface-container-high` card on a `surface-container-low` background. The delta in luminance creates the lift.
*   **Ambient Shadows:** For floating navigation or modals, use an "Atmospheric Glow." Instead of `#000000`, use the `primary_dim` color at 8% opacity with a `48px` blur. This simulates light reflecting off a neon surface.
*   **The "Ghost Border" Fallback:** If a boundary is required for accessibility, use the `outline-variant` token at **15% opacity**. It should feel like a suggestion of an edge, not a cage.

---

## 5. Components

### Video Player Cards
*   **Structure:** No borders. Use `surface-container-highest` for the base.
*   **Interaction:** On hover, the container should scale slightly (1.02x) and the `primary_dim` ambient shadow should intensify.
*   **Overlay:** Use a `surface-container-lowest` gradient at the bottom (0% to 60% alpha) to house the play duration and title in `label-md`.

### Ranking List Items
*   **Rule:** No dividers. Separate items using `3.5rem` (`spacing-10`) of vertical white space or a subtle shift to `surface-container-low` for every even-numbered item.
*   **Rank Numbers:** Use `display-sm` in `tertiary` (Neon Pink) to create a bold vertical rhythm down the page.

### Dynamic Navigation
*   **Style:** A "Glassmorphism" dock. Use a semi-transparent `surface-bright` with a heavy backdrop blur.
*   **Active State:** Instead of an underline, use a small `2.5rem` (`spacing-2.5`) pill of `secondary` behind the icon/text with a 20% opacity.

### Buttons
*   **Primary:** Gradient from `primary` to `primary_dim`. `radius-full`. No shadow.
*   **Secondary:** `outline-variant` (at 20% opacity) with text in `on-surface`.
*   **Tertiary:** Text-only using `tertiary` color, all caps, using `label-md` for a "utility" feel.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical margins. If the left margin is `spacing-8`, try a right margin of `spacing-12` for editorial layouts.
*   **Do** lean into high-contrast type. Pair a `display-lg` headline with a `body-sm` description.
*   **Do** use the `tertiary` (Neon Pink) sparingly for "Pops" of energy—like a notification dot or a "New" badge.

### Don’t
*   **Don’t** use 100% opaque white for body text. Use `on-surface-variant` (`#acaab1`) to reduce eye strain against the dark background.
*   **Don’t** use standard "Drop Shadows." They muddy the vibrant palette. Use "Atmospheric Glows" (tinted shadows).
*   **Don’t** use grid lines. If you feel the need to draw a line, try adding a `spacing-16` gap instead. Let the alignment create the structure.

---

## 7. Spacing Rhythm
Spacing is the "Tempo" of the site.
*   **Macro-Spacing:** Use `spacing-20` and `spacing-24` to separate major content blocks. Give the music room to breathe.
*   **Micro-Spacing:** Use `spacing-1.5` and `spacing-3` for tight groupings (e.g., Artist Name + Genre tag).```