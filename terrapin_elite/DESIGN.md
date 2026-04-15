# Design System Document

## 1. Overview & Creative North Star: "The Collegiate Curator"
This design system moves away from the rigid, boxy layouts of traditional academic portals. Instead, it adopts the persona of **The Collegiate Curator**: a blend of high-end editorial prestige and modern community warmth. 

The system leverages **intentional asymmetry** and **tonal layering** to create a digital environment that feels curated rather than templated. We break the "academic grid" by overlapping typography onto image containers and utilizing wide, sweeping margins. The goal is to make the pre-business community feel like an exclusive but welcoming "clubhouse"—a space where professional ambition meets student-led energy.

---

## 2. Colors & Surface Philosophy
The palette is rooted in the heritage of Maroon and Gold but evolves through a sophisticated scale of neutrals to ensure the "BizDogs" identity feels modern and premium.

### Palette Strategy
- **Primary (`#7A0019`):** Used for "Brand Moments." Reserved for high-impact accents, primary CTAs, and active states.
- **Secondary (`#CC9900`):** Used as a "Highlight" color. Best applied to small UI elements like notification dots, active underlines, or specific call-outs within cards.
- **Tertiary (`#242525`):** Our "Professional Navy/Charcoal." Used to anchor the design in business-ready seriousness.

### The "No-Line" Rule
**Explicit Instruction:** Traditional 1px solid borders for sectioning are strictly prohibited. Boundaries must be defined solely through background color shifts or tonal transitions.
*   *Example:* A `surface-container-low` section sitting directly on a `surface` background creates a natural, soft edge.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers, similar to stacked sheets of fine vellum.
- **Surface (Base):** `#faf9f8`
- **Surface-Container-Low:** `#f4f3f2` (Used for background sections to sit "behind" content)
- **Surface-Container-Highest:** `#e3e2e1` (Used for "Hero" or "Focus" elements)

### The "Glass & Gradient" Rule
To add "soul" to the interface:
- **Glassmorphism:** For floating navigation bars or overlay modals, use semi-transparent `surface` colors with a `backdrop-filter: blur(20px)`.
- **Signature Gradients:** Use a subtle linear gradient transitioning from `primary` (#51000d) to `primary_container` (#7a0019) for main CTA buttons to provide a tactile, high-end finish.

---

## 3. Typography: The Editorial Mix
We utilize a high-contrast pairing to balance "Authority" with "Approachability."

### The Pairing
- **Display & Headlines (Public Sans):** A bold, authoritative sans-serif that speaks to professional ambition. Use large scales (`display-lg`) with tight letter-spacing (-2%) for an editorial, "magazine-style" look.
- **Body & Titles (Inter):** A clean, highly readable sans-serif for information density.

### Typographic Identity
*   **Hero Statements:** Use `display-lg` in `on_surface`. Don't be afraid to let text overlap onto an image container by 20-30px to create depth.
*   **Section Headers:** Use `headline-md` in `primary`. Pair with a `label-md` "subtitle" placed *above* the headline in all-caps with 10% letter spacing.

---

## 4. Elevation & Depth
In this design system, shadows are atmospheric, not structural.

### The Layering Principle
Depth is achieved by stacking containers. Place a `surface_container_lowest` (#ffffff) card on a `surface_container_low` (#f4f3f2) background to create a soft "lift" without a single line of code for shadows.

### Ambient Shadows
When a floating effect is mandatory (e.g., a dropdown or a "Featured" event card), use **Ambient Shadows**:
- **Blur:** 40px – 60px
- **Opacity:** 4% – 8%
- **Color:** A tinted version of `on_surface` (never pure black).

### The "Ghost Border" Fallback
If a border is required for accessibility, it must be a **Ghost Border**:
- Use `outline_variant` at **15% opacity**. It should be felt rather than seen.

---

## 5. Components

### Hero Sections
Avoid centered, symmetrical layouts. Use a 60/40 split. The 60% side contains high-impact `display-lg` typography; the 40% side features an image with a large `xl` (0.75rem) corner radius, slightly offset from the grid to create motion.

### Event Cards & Lists
- **Rule:** **No Divider Lines.** 
- Separate event items using vertical whitespace (32px or 48px) and subtle background shifts. 
- Use a `surface_container_low` background for the card, and a `surface_container_lowest` (pure white) for the internal "Join" button to make it pop.

### Call-to-Action (CTA) Buttons
- **Primary:** Gradient-filled (`primary` to `primary_container`), `xl` roundedness, with a `label-md` uppercase text style.
- **Secondary:** Transparent background with a "Ghost Border."
- **Tertiary:** Text-only with a 2px `secondary` (Gold) underline that expands on hover.

### Member Testimonials
Treat these as editorial pull-quotes. Use `title-lg` in *italic* (if available) or `primary` color. Place the student's headshot in a small `full` rounded (circular) container next to a `surface_variant` vertical bar (4px wide) to anchor the quote.

### Input Fields
- Background: `surface_container_high`.
- Border: None, until focus. On focus, use a 2px `primary` bottom-border only. This maintains the "academic ledger" feel while remaining modern.

---

## 6. Do’s and Don’ts

### Do:
- **Do** use generous whitespace. If you think there’s enough space, add 16px more.
- **Do** overlap elements. Let a badge or a tag sit halfway off the edge of an image.
- **Do** use `secondary_fixed` (Gold) for tiny, high-attention details like star ratings or "Live Now" indicators.

### Don't:
- **Don't** use 1px solid, high-contrast borders. It breaks the "premium paper" illusion.
- **Don't** use standard "Drop Shadows." They feel dated and "out-of-the-box."
- **Don't** clutter the screen with dividers. Let the content breathe and the background shifts do the work.
- **Don't** use pure black (#000000). Always use `tertiary` or `on_surface` for a softer, professional look.