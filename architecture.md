# JACK CLOSNER PORTFOLIO — Site Architecture, Pages & Navigation

*Last updated: June 19, 2026 | Version 1.1 | PLATFORM: Single-Page Marketing & Personal Portfolio Site*

---

## Directory Structure

To maintain a clean, modern workspace, all media assets are consolidated into a dedicated directory rather than cluttering the root folder. The site uses the following clean architecture:

```
├── assets/
│   └── images/                     # Consolidates all portfolio JPEG and PNG images
├── index.html                      # The single-page website entrance
├── CNAME                           # Domain mapping for hosting
├── README.md                       # Repository overview
├── architecture.md                 # This document
└── design.md                       # Design and typography system guidelines
```

---

## Visitor Roles

### Primary Visitor: Friends, Peers, and Family Members
This visitor is looking for updates on Jack's life, viewing photos of recent outdoor excursions, looking at caught animals, and sharing in travel experiences.

**Core characteristics:**
- Navigates quickly, focusing heavily on visual elements and images.
- Prefers direct, casual storytelling.
- Likely browsing on mobile devices.
- Interested in social links (Instagram, Snapchat) to connect.

**What this means for site structure:**
Every section must lead with a compelling, high-contrast image located under `assets/images/` and an immediate, clear heading so the user understands the context within 2 seconds.

---

### Secondary Visitors

| Visitor Type | Goal | Priority Pages / Sections |
|---|---|---|
| Academic Recruiter / School Admin | Verify Jack's senior status, leadership skills, and achievements. | Hero tagline, `#about` (Student of the Month, BCHS link), and Trail Life news segment. |
| Scout Coordinators / Outdoor Peers | Review outdoor skills, safety consciousness, and group experiences. | Trail Life section (backpacking, fire mastery, coastal fishing) and `#animals` relocation details. |

---

## Navigation Structure

### Header Navigation

| Nav Item | Links To | Dropdown? | Notes |
|---|---|---|---|
| **JACK CLOSNER** | `/` (Top of page) | No | Brand logo, italicized, bold, and uppercase. |
| **Bio** | `#about` | No | Links directly to "My Story". |
| **Catches** | `#animals` | No | Links to "The Animal Catcher" gallery. |
| **Active** | `#active` | No | Links to "Fast & Active" bikes section. |
| **Travels** | `#travel` | No | Links to "Explorations" travel gallery. |

*Note: There are no primary CTA buttons in the header; navigation remains minimal to focus on the main scroll.*

### Footer Navigation

| Column Label | Links / Elements |
|---|---|
| **Social Connections** | Instagram link, Snapchat link, Email envelope link |
| **Branding & Copyright** | © 2026 Jack Closner |
| **Tagline** | Fast • Active • Energetic |

### Mobile Navigation
On mobile devices (below `md` breakpoint), the navigation links are hidden (`hidden md:block`), leaving only the primary brand logo **JACK CLOSNER** centered or left-aligned. This ensures a clean, distraction-free view on smaller screens, relying on scroll-based navigation.

---

## Page Section Purposes

| Section | Anchor / ID | Single-sentence purpose |
|---|---|---|
| Hero Header | (Top of page) | Captures immediate attention, defines senior status, and provides immediate links to core content. |
| My Story | `#about` | Establishes academic credentials at BCHS and mentions personal interests like sports. |
| The Animal Catcher | `#animals` | Showcases hand-capture capabilities, creek relocations, and trailer rescues. |
| Fast & Active | `#active` | Documents physical endurance (20-mile cycling) and farm riding hobbies. |
| Trail Life | (Flows after `#active`) | Showcases group leadership, campsite mastery, coastal fishing, and a KBTX news segment feature. |
| Explorations | `#travel` | Chronicles trips to national parks, deep caves, and highlights favorite Texas spots (Garner State Park). |
| Dream Car | (Flows after `#travel`) | Concludes the scroll with a massive, bold statement of personal drive and aspirations. |
| Contact Footer | `#contact` | Offers direct social media connection endpoints. |

---

## Primary Visitor Journeys

### Journey 1 — Browsing Catches & Adventures (Friends/Peers)
A friend wants to see the latest animals Jack caught.

```
Landing on index.html
→ Clicks "The Catch List" CTA in Hero
→ Smooth scrolls to "#animals"
→ Views snake, armadillo, and turtle cards
→ Views images served from assets/images/
→ Scrolls down to see the Bass Pro alligator gar and mouse rescue details
→ Connects via Instagram in the footer
```

**Success state:** The visitor sees all catches and successfully clicks through to social media.

---

### Journey 2 — Verifying Academic & Leadership Credentials (Recruiter/Scout Leader)
An administrator wants to check Jack's community involvement and academic standing.

```
Landing on index.html
→ Reads Bryan Collegiate tagline
→ Clicks "Bio" in Header Nav
→ Reads "My Story" (noticing Student of the Month status)
→ Scrolls to Trail Life section
→ Clicks on KBTX News segment link to watch the television clip
```

**Success state:** The visitor confirms Jack's BCHS attendance, student achievement, and news-featured scout leadership.

---

## Page Section Patterns

### Hero Section
- **Pattern:** High-impact text layout overlaid on a subtle SVG circle-pattern background.
- **Details:** Centered white headings in 'Bungee' typography with shadow, preceded by a rounded white badge indicating school status, followed by dual black-and-white CTA buttons.

### Social Proof & Media Trust
- **Pattern:** Trusted link cards and badges.
- **Details:** Incorporates a video-play card linking to an external KBTX news story, complete with a thumbnail (`assets/images/news_trail_life.png`) and play overlay, as well as an official link to Texas Parks & Wildlife Department (TPWD) for Garner State Park.

### Card Grids
- **Pattern:** Multi-column grids (1 column on mobile, 2–3 columns on desktop) with a clean border, rounded corners (`rounded-[40px]`), and a `.card-hover` lift translation.

---

## Technical Architecture

### Framework & Hosting
- **Framework:** Vanilla HTML5 & CSS3.
- **CSS Engine:** Tailwind CSS CDN (`https://cdn.tailwindcss.com`) for responsive utility-first layout.
- **Icons:** FontAwesome CDN (`all.min.css`) for social icons, dog icons, warning symbols, and truck pickups.
- **Hosting:** GitHub Pages (configured via CNAME to point to the repository domain).
- **CMS:** None (hardcoded static files for speed, offline portability, and zero server maintenance).

### Performance Targets
- **Largest Contentful Paint:** < 1.0s (minimized script load, optimized JPEG assets).
- **Cumulative Layout Shift:** 0.0 (static layout, fixed aspect ratios for key image sections).

---

*Jack Closner Portfolio | https://jackclosner.github.io | Personal Web Project*
