# JACK CLOSNER PORTFOLIO — Design Guidelines

*Last updated: June 19, 2026 | Version 1.1*
*Companion document to: Jack Closner Portfolio Design System & Component Guidelines*

---

## Purpose of This Document

The Design System covers **what** to build—component specs, Tailwind custom properties, and utility classes.

This document covers **why**—the rationale behind layout decisions, the varsity/adventure tone of typography, color usage rules, hover states, and standard layout configurations for future updates.

---

## Typography System

The typography system is designed to evoke a varsity sports/high-adventure aesthetic combined with a highly readable modern layout.

### Font Roles

| Role | Font | Weights Used |
|---|---|---|
| Display / Hero | 'Bungee', cursive | Regular (900-equivalent style) |
| Section Headers | 'Bungee', cursive | Regular |
| Body / UI | 'Inter', sans-serif | 400 (Regular), 500 (Medium), 700 (Bold), 900 (Black) |
| Tags / Labels / Chips | 'Inter', sans-serif | 700 (Bold), 900 (Black) |
| Decorative Accent | 'Bungee', cursive | Regular (italicized/uppercase accents) |

### Type Scale

| Level | Font | Size | Weight | Line Height | Usage |
|---|---|---|---|---|---|
| Display | 'Bungee' | 48px–128px (text-5xl to text-9xl) | Regular | 1.0 | Hero heading, Dream Car footer |
| H1 | 'Bungee' | 48px–80px (text-5xl to text-8xl) | Regular | 1.1 | Hero main title |
| H2 | 'Bungee' | 48px (text-5xl) | Regular | 1.2 | Section titles ("MY STORY", "FAST & ACTIVE") |
| H3 | 'Bungee' | 24px (text-2xl) | Regular | 1.3 | Card titles (Catches, Swamp Tour) |
| H4 | 'Bungee' | 14px–20px (text-sm to text-xl) | Regular | 1.4 | Mini card titles (Gar, Mini Bikes) |
| Body Large | 'Inter' | 20px–24px (text-xl to text-2xl) | 500 / 700 | 1.5 | Hero subtitle, Bio introductory text |
| Body | 'Inter' | 16px–18px (text-base to text-lg) | 400 / 500 / 700 | 1.6 | General paragraphs and card details |
| Body Small | 'Inter' | 12px–14px (text-xs to text-sm) | 500 / 700 | 1.5 | Mini descriptions and warnings |
| Tag / Badge | 'Inter' | 10px (text-[10px]) | 900 | 1.0 | Travel category labels, watch clip badge |
| Fine Print | 'Inter' | 12px (text-xs) | 400 / 700 | 1.0 | Footer copyright and taglines |

**Sizing rules:**
- **'Bungee'**: Minimum size 12px (for badges/mini titles). Do not use for body text or long descriptions.
- **'Inter'**: Minimum size 10px (for compact tags). Ensure bold/black weights are used for high hierarchy elements.

### Loading Fonts

Fonts are loaded from Google Fonts in the HTML `<head>` using an `@import` statement inside `<style>` with normal fallback parameters:
```css
@import url('https://fonts.googleapis.com/css2?family=Bungee&family=Inter:wght@400;700;900&display=swap');
```

---

## Color System

The color system centers around a high-octane orange brand color contrasted against stark whites and deep, rugged grays/blacks.

### Color Tokens

The site relies on Tailwind CSS classes mapped to the following color palette:

| Token / Color Class | Hex / Value | Role |
|---|---|---|
| `bg-orange-gradient` | `linear-gradient(135deg, #f97316 0%, #fb923c 100%)` | Primary brand gradient (Hero background) |
| `text-orange-600` | `#ea580c` | Section titles, brand logo, inline links |
| `border-orange-500` | `#f97316` | Navigation border, Bio photo border, travel cards accent |
| `bg-gray-50` | `#f9fafb` | Primary light background (body, Explorations) |
| `bg-gray-900` | `#111827` | Primary dark background (The Animal Catcher section) |
| `bg-gray-800` | `#1f2937` | Card backgrounds on dark sections |
| `bg-black` | `#000000` | Dream Car footer background |
| `text-gray-900` | `#111827` | Primary text on light sections |
| `text-white` | `#ffffff` | Primary text on dark sections / text on gradient |
| `border-green-500` | `#22c55e` | Accent border for Snake card |
| `border-yellow-500` | `#eab308` | Accent border for Turtle card / Garner State Park highlight |
| `border-blue-500` | `#3b82f6` | Accent border for Alligator Gar |
| `border-red-500` | `#ef4444` | Accent border for Trailer Rescue / warnings |

### Color Decision Logic

**Is this a primary brand container or the hero background?**
→ Use `bg-orange-gradient` or solid `bg-orange-600` for high impact.

**Is this a light section background?**
→ Use `bg-white` or `bg-gray-50`.

**Is this a dark section representing night-time, water, or industrial themes?**
→ Use `bg-gray-900` or `bg-black`.

**Is this a card element?**
→ Use `bg-white` (on light sections) or `bg-gray-800` (on dark sections).

**Is this card representing a specific animal or environmental category?**
→ Mapped borders:
- Reptiles / Snakes: `border-green-500`
- Relocations / General: `border-orange-500`
- Turtles / Softshells: `border-yellow-500`
- Fish / Water: `border-blue-500`
- Warnings / Emergencies: `border-red-500`

---

## Interaction Principles

### 1. Every action needs visible feedback within 100ms
Interactive grid cards respond to hover with a slight vertical translation and drop shadow increase.
- CSS class: `.card-hover`
- Behavior: `transform: translateY(-5px); transition: all 0.3s ease;`

### 2. Micro-Scaling for CTA Buttons
Primary buttons scale up slightly on hover to feel responsive and elastic.
- CSS classes: `hover:scale-105 transition-transform`

### 3. Social & Link Transitions
Footer social icons scale up and highlight when hovered.
- CSS classes: `hover:scale-125 transition-transform`

### 4. Interactive Video / News Play Overlay
The news clip card uses a dark overlay that lightens, and a play icon that scales up when hovered.
- Hover classes: `group-hover:opacity-40 transition-opacity` (thumbnail) and `group-hover:scale-110 transition-transform` (play icon).

---

## Developer Implementation Notes

### Custom Utility CSS
Define utility classes at the top of the stylesheet for consistency:
```css
.heading-font {
    font-family: 'Bungee', cursive;
}
.bg-orange-gradient {
    background: linear-gradient(135deg, #f97316 0%, #fb923c 100%);
}
.card-hover:hover {
    transform: translateY(-5px);
    transition: all 0.3s ease;
}
.text-shadow {
    text-shadow: 2px 2px 0px rgba(0,0,0,0.1);
}
```

### Layout Patterns & Sizing
- **Sections**: Use `py-24` (6rem top/bottom padding) to create breathing room between high-contrast blocks.
- **Card Corners**: Use rounded corners extensively (`rounded-[40px]` or `rounded-3xl`) to soften the high-contrast aesthetic and give a premium feel.
- **Borders**: Section separators and card highlights use a thick border style (`border-b-8`, `border-t-8`, or `border-l-8`) to maintain the athletic, bold brand presence.

### Image Assets Pathing
All image assets are served from `assets/images/` to maintain a clean codebase structure.
- **Example**: `<img src="assets/images/student_of_the_month.jpeg">`
- All activity images must use `object-cover` and a top alignment `object-top` where humans or animals are the focus, ensuring heads/details are not cut off.
- Hero images / Bio images: Use explicit grid spacing and `aspect-[3/4]` or `h-96`/`h-64`.

---

## Accessibility Checklist

- [x] **Heading Hierarchy**: One main H1 (`<h1>`) in the hero; H2s for all main sections; H3s/H4s for card titles.
- [x] **External Links**: All outbound links (BCHS, KBTX news, TPWD Garner) have `target="_blank"` for a seamless browsing flow.
- [x] **Image Alt Text**: Detailed descriptive alts:
  - BCHS Student of the Month: `alt="Student of the Month"`
  - Aggie Game: `alt="Aggie Game"`
  - Snake Capture: `alt="Caught a Snake"`
  - Bicycle: `alt="My Bicycle"`
  - Mini Bike: `alt="Mini Bike at the Farm"`
  - Backpacking: `alt="Backpacking"`
  - Campfire Mastery: `alt="Fire Mastery"`
  - Seashore Fishing: `alt="Beach Fishing"`
- [x] **Contrast**: Heavy contrast white text on dark gray/black backgrounds (`bg-gray-800`/`bg-gray-900`) and dark text on light gray/white backgrounds (`bg-gray-50`/`bg-white`).

---

## Design Review Checklist

- [x] **Typography Consistency**: Only 'Bungee' for headers/badges, and 'Inter' for UI descriptions.
- [x] **Responsive Grid**: Tailwind grids auto-adjust from `grid-cols-1` (mobile) to `md:grid-cols-2` or `lg:grid-cols-3/4` (desktop).
- [x] **Touch Targets**: Navigation links and social icons are large and spaced out (e.g. `space-x-12` and text size `text-4xl`).
- [x] **Aesthetic Flow**: Harmonious transitions between warm orange, neutral white, dark gravel, and clean gray surfaces.

---

*Jack Closner Portfolio | https://jackclosner.github.io*
