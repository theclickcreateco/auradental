# Design System Specification: Cosmetic Dental Studio

## 1. Overview & Creative North Star
**Creative North Star: "The Ethereal Clinic"**

This design system moves away from the sterile, rigid grids of traditional medicine and toward a "High-End Editorial" experience. The goal is to balance clinical precision with the warmth of a luxury spa. We achieve this through **Soft Minimalism**—a style defined by breathing room, fluid layering, and intentional asymmetry. 

Rather than boxing content into a grid, we treat the screen as a canvas of light. We break the "template" look by using exaggerated typography scales and overlapping high-quality dental photography with soft, semi-transparent UI elements. The result is a digital environment that feels breathable, trustworthy, and premium.

---

## 2. Colors & Surface Philosophy
The palette is rooted in `surface` (soft whites) and `seafoam blue` (#E0F2F1), but it is executed through tonal depth rather than flat blocks.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning content. Boundaries must be defined solely through background color shifts or tonal transitions. To separate a "Before & After" gallery from a testimonial section, transition from `surface` to `surface-container-low`.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine, translucent paper. 
- **Base Layer:** `surface` (#f4fafa) for the primary page background.
- **Content Blocks:** `surface-container-low` (#eff5f5) for large structural areas.
- **Interactive Cards:** `surface-container-lowest` (#ffffff) to provide a "pop" of clean white against the seafoam-tinted background.

### The "Glass & Gradient" Rule
To add "soul" to the clinical aesthetic:
- **Glassmorphism:** Use `surface-container-lowest` at 70% opacity with a `20px backdrop-blur` for floating navigation bars or treatment pricing modals.
- **Signature Gradients:** For primary CTAs and Hero sections, use a subtle linear gradient from `primary` (#006a63) to `primary-container` (#a2fff4) at a 135-degree angle. This mimics the way light hits polished enamel.

---

## 3. Typography
We use a dual-sans-serif approach to balance authority with modern approachable luxury.

- **Display & Headlines (Manrope):** Chosen for its geometric precision and wide apertures. Use `display-lg` (3.5rem) for high-impact dental transformations. The tight tracking and large scale convey "High-End Editorial."
- **Body & Labels (Inter):** The workhorse for trust. Inter provides exceptional legibility for clinical details and procedure descriptions.
- **The Editorial Shift:** Invert expectations by using `display-sm` for pull-quotes or testimonials, set in `primary` color to break the monotony of black text.

---

## 4. Elevation & Depth
In this design system, depth is a feeling, not a shadow.

- **Tonal Layering:** Avoid shadows for standard cards. Achieve lift by placing a `surface-container-lowest` (#ffffff) element on top of a `surface-container` (#e9efef) background.
- **Ambient Shadows:** When an element must float (e.g., a "Book Appointment" FAB), use a highly diffused shadow: `0px 20px 40px rgba(22, 29, 29, 0.06)`. The tint is derived from the `on-surface` token, ensuring it looks like natural light, not digital ink.
- **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline-variant` (#c2c8c7) at **15% opacity**. It should be felt, not seen.
- **The Glass Depth:** Use a 1px "inner highlight" on glass components using `surface-container-lowest` at 40% opacity to simulate a beveled edge on a glass tray.

---

## 5. Components

### Buttons
- **Primary:** High-gloss. Background: `primary` gradient. Shape: `xl` (1.5rem / 24px). Text: `on-primary` (White).
- **Secondary:** The "Treatment" button. Background: `surface-container-highest`. Text: `on-surface`. Soft `lg` (1rem) corners.
- **Tertiary:** Text-only with a subtle `primary` underline that expands on hover.

### Cards & Lists
- **The "No-Divider" Rule:** Forbid horizontal lines between list items. Use 24px-32px of vertical white space (Spacing Scale) to define list items.
- **Procedure Cards:** Use `xl` (24px) corner radius. Imagery should bleed to the edges or overlap the card boundary slightly to create an asymmetrical, custom feel.

### Input Fields
- **Style:** Background-filled using `surface-container-high`. No bottom border.
- **State:** When focused, the background shifts to `surface-container-lowest` with a subtle `primary` glow (not a harsh outline).

### Specialized Dental Components
- **Before/After Slider:** A minimalist toggle using `primary_fixed` to slide between transformation photos.
- **Trust Badges:** Micro-chips using `tertiary_container` with `on-tertiary-container` text to denote certifications or "Pain-Free" guarantees.

---

## 6. Do's and Don'ts

### Do
- **DO** use generous whitespace (64px, 80px, 128px) between sections to reduce "medical anxiety."
- **DO** use imagery of sunlight, water, and soft dental environments.
- **DO** use `xl` (1.5rem) roundedness for large containers to echo the organic curves of a smile.

### Don't
- **DON'T** use 100% black (#000000) for text. Always use `on-surface` (#161d1d) for a softer, more premium contrast.
- **DON'T** use sharp 90-degree corners; they feel aggressive and non-clinical in a cosmetic context.
- **DON'T** clutter the UI with "Call Now" buttons. One clear, high-contrast CTA per scroll-depth is sufficient for a high-end experience.
- **DON'T** use generic medical icons. Use custom, thin-stroke (1.5px) iconography that matches the weight of the Inter typeface.