# JACK CLOSNER PORTFOLIO — Visual Style Guide

*Last updated: June 19, 2026 | Version 1.1*

---

## Emotional Thesis

The Jack Closner Portfolio is designed to deliver a rush of **outdoor adrenaline, varsity energy, and raw grit**. Before reading a single word, the visitor should feel the high-octane speed of a bike ride, the hands-on excitement of catching a creek snake, and the rugged warmth of a campfire. The visual register is active, bold, and adventurous—completely devoid of corporate stiffness or passive academic layouts.

---

## The World This Product Lives In

The visual environment draws from **Texas high school varsity sports, outdoor scouting, and active creek bed exploration**.

This world contains:
- **High-contrast orange** — evoking varsity jerseys, team sports, and safety gear.
- **Thick, blocky typography ('Bungee')** — evoking varsity letter jackets and athletic branding.
- **Deep gravel gray and jet black** — evoking night-time creek scouting, truck tires, and base camps.
- **Thick borders and sharp angles** — evoking physical signage, camp trails, and athletic boundary lines.
- **Candid adventure photography** — showcasing dirt, animals, and real-life action rather than polished studio poses.

The emotional register is **rugged and active**, not **delicate or minimal**. It is built to showcase movement and real-world accomplishments.

---

## Lighting

Lighting defines the atmosphere and is split between bright outdoor activity and warm campfire/night exploration.

- **Primary light:** High-contrast, bright Texas midday sun. It represents cycling, fishing, and catching reptiles in broad daylight. Colors are vivid, and shadows are sharp and short.
- **Secondary light:** The warm, flickering amber glow of a campfire, or the focused beam of a flashlight during a night-time creek crawl.
- **Avoid:** 
  - Soft, sterile corporate office lighting.
  - Moody, desaturated pastel filters.
  - Abstract neon cyberpunk gradients.

**In practice:**
- Light sections (Bio, Active) use pure white and high-contrast gray-50 to reflect the bright midday sun.
- Dark sections (Catches, Dream Car) use deep charcoal and black to establish the night-time/creekbed atmosphere.
- Warm orange highlights and yellow borders act as the crackling campfire or safety beacon against the dark background.

---

## Color Tone by Surface

| Surface | Dominant Colors | Emotional Role |
|---|---|---|
| Hero Header | `bg-orange-gradient` (`#f97316` to `#fb923c`), White | High-energy, warm, welcoming, and instantly action-oriented. |
| Bio / My Story | White (`bg-white`), Orange-600 text, Black photos | Academic pride, clean readability, and structured storytelling. |
| The Animal Catcher | Deep Gray (`bg-gray-900`), Dark Gray (`bg-gray-800`), Accent Borders | Rugged, dark, mysterious creekbed vibe; makes animal photos pop. |
| Fast & Active | White (`bg-white`), Orange-50 containers, Black | High-contrast readability, speed, and clean motion layouts. |
| Trail Life | Orange-600 background, White text, semi-transparent overlays | Scout troop unity, outdoor warmth, campfire team spirit. |
| Explorations / Travels | Gray-50 background, White cards, multi-color borders | Curious, exploratory, organized logbook of trips. |
| Dream Car / Footer | Pitch Black (`bg-black`), Orange-500 text, Gray accents | Heavy-duty, industrial, clean, and aspirational closure. |

---

## Photography Direction

### What to show
- **Real, hand-captured wildlife:** Snakes, softshell turtles, and armadillos held securely and photographed up close. All images are hosted in `assets/images/`.
- **Action & Endurance:** Bikes on trails, backpacking trips, and tending campfires.
- **Authentic Milestones:** Group photos at Texas A&M games, smiling with a gingerbread win, and student awards in school settings.
- **Natural Landscapes:** Sunsets at Port Aransas beach, desert canyons in Big Bend, and rock arches in Zion.

### What to avoid
- **Stock Photography:** Never use standard stock photos of animals, generic hikers, or generic bicycles.
- **Staged Studio Work:** Avoid overly polished, desaturated headshots or corporate-looking poses.
- **Low Contrast:** Avoid washed-out exposures. Photos must be vibrant, full of contrast, and sharp.

### Technical specs
- **Aspect Ratios:** Standard vertical portrait crops (`aspect-[3/4]`, `h-80`, `h-96`) and horizontal grid blocks (`h-48`, `h-64`).
- **Fit:** Always use `object-cover` and `object-top` to ensure faces, heads of animals, and key action elements remain framed.
- **Borders:** All images should be nested inside cards with organic rounded corners (`rounded-3xl` or `rounded-[40px]`).

---

## Illustration & Iconography Direction

The site does not use digital illustrations, opting instead for **candid photography and clean vector iconography**.

**Style reference:** FontAwesome Solid & Brands vector icons.

**Characteristics:**
- **Icons:** Simple, thick silhouette vector glyphs (e.g. dog icon, warning triangle, truck pickup, play circle, play buttons).
- **Color:** Mapped directly to the section accent (e.g., orange-500, blue-400, red-400).
- **Placement:** Placed inside rounded circles or alongside headers to act as clean visual anchors.

**What to avoid:**
- Thin, delicate line-art icons.
- Colorful, generic flat-style tech illustrations (SaaS vector drawings).

---

## Typography in Context

### 'Bungee' (Cursive / Display) — Varsity & Athletic Branding

- **Feels like:** A varsity letter jacket, collegiate stadium signage, and sports apparel brands.
- **Used for:** Section headers ("MY STORY", "FAST & ACTIVE"), navigation brand logo ("JACK CLOSNER"), catch card titles, and the giant dream car text ("RAM 2500").
- **Rules:** 
  - Always uppercase.
  - Never used for paragraph text or captions.
  - Paired with text shadows (`text-shadow`) on gradient surfaces to enhance readability.

### 'Inter' (Sans-Serif) — Rugged Modern Readability

- **Feels like:** A clean, structured, high-grade technical logbook or map legend.
- **Used for:** Paragraph copy, descriptions, details of catches, and footer copyright text.
- **Rules:**
  - Standard weight (400) for general body text.
  - Bold (700) and Black (900) weights for tags, highlight callouts, and emphasis links.

---

## Motion Philosophy

Motion is used strictly to reinforce **speed, responsiveness, and tactile feedback** (matching the "Fast & Active" theme).

**Core principle:** Visual feedback should feel snappy and elastic, responding immediately to user interaction.

### When motion is appropriate
- **Card Hover:** Cards translate upwards by `-5px` with a smooth ease-out curve, simulating lifting a physical card off a table.
- **Button Hover:** Call-to-action buttons scale up by `1.05` to invite clicks.
- **Social Icon Hover:** Social media vectors scale up by `1.25` on hover.
- **Video Play Button:** Scales up by `1.1` on hover to emphasize playability.

### Timing reference

| Type | Duration | Easing |
|---|---|---|
| Card Hover / Translation | 300ms | ease-out |
| Scale Transformations | 200ms | ease-in-out |
| Video Play Scale | 150ms | ease-out |

---

## UI Surface Materials

- **Varsity Cards:** Substantial cardstock with extremely rounded corners (`rounded-[40px]`). Hover state increases shadow and lifts the card.
- **Tactile Borders:** Thick, solid colored border bands (`border-t-8`, `border-l-8`, `border-b-4`) that frame sections and anchor content modules.
- **Glassmorphic Shields:** `bg-white/10 backdrop-blur` containers used in the Trail Life section, suggesting outdoor weather protection and translucent gear.

---

## Voice in Visual Context

### Landing Hero
```
CHASING ADVENTURE & CATCHING ANIMALS
From 20-mile bike rides to catching snakes in the creek, I'm always on the move.
```
*Typography:* Heading in 'Bungee' (text-5xl/text-8xl, uppercase, text-shadow), Subtitle in 'Inter' (text-xl/text-3xl, medium, opacity-90).

### Card Captions
```
Tony the Turtle
He's a softshell slider I pulled from the water near home.
```
*Typography:* Title in 'Bungee' (text-2xl, text-yellow-400), Caption in 'Inter' (text-gray-400, regular).

---

## What This Product Is Not

- **Not a Tech Startup Resume:** Visually avoids thin san-serifs, pastel circles, flat digital drawings, and "clean minimalism."
- **Not a Corporate Portfolio:** Rejects neutral blues, sterile tables, passive layouts, and professional jargon.
- **Not a Dark Hacker Terminal:** Rejects green monospaced text, terminal boxes, and neon shadows in favor of bright, varsity colors.

---

*Jack Closner Portfolio | https://jackclosner.github.io | Personal Web Project*
