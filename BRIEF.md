# NJP Sports Inc — Design Brief

> **Round 2 update:** First pass under-represented the catalog and incorrectly placed Edwards + Playmate in the "where the work lives" marquee. Capabilities expanded from 10 cards to a 17-line catalog organized in three groups; venue marquee now lists only real install locations; new dedicated **Distributors** band carries Edwards / Playmate / First Team. See bottom of file for the full Round 2 changelog.



## Brand Synopsis

NJP Sports Inc. is a Glendale, California-based windscreen and tennis-court-equipment specialist. **In business since 1971**. **On the web since 1996** (their domain has been online longer than most people have been on the internet). Family-run wholesale supplier, manufacturer, and licensed contractor (Lic. No. 284844 C-13) — they fabricate custom mesh and vinyl windscreen on a Glendale workshop floor, install across the greater Los Angeles area, and ship the rest worldwide.

Their work lives at venues that punch well above what the current website would suggest: **Indian Wells Tennis Garden** (BNP Paribas Open), **Pepperdine University** (1999 NCAA Tennis Finals court), **UCLA** (LA Open), **Studio City Golf & Tennis Club**, the **Hollywood Hills** for private hillside courts, and **University of Redlands**. They're the authorized Southern California sales and service center for **Playmate** ball machines, and the U.S. distributor for **Edwards of England** tennis nets and posts — a Wimbledon and ATP supplier that's been making nets since **1884**.

The current site is unchanged 1996-era HTML — table layout, dark-green sidebar, Times New Roman, Courier accents. Authentic, but a brand mismatch with the calibre of work they actually deliver. The redesign honors the heritage and the fabrication craft while making sure a first-time visitor gets that this is the shop major venues call.

## Design Decisions

### Mood
"Industrial heritage workwear meets editorial sports photography." Restrained, authoritative, tactile. SoCal sports legacy. Built for a long workday, not a launch party.

### Style (PRO-MAX MODE)
Hybrid pulled from the `ui-ux-pro-max` skill's deep-dive: **Editorial Grid / Magazine** + **Swiss Modernism 2.0** + a touch of **Anti-Polish / Raw Aesthetic** for the paper grain. The skill's auto-recommended "Vibrant & Block-based" sport-orange direction was rejected — it was keying off the word "sports" and ignoring the heritage brief.

### Fonts
- **Display: [Bebas Neue](https://fonts.google.com/specimen/Bebas+Neue)** — condensed, anchored, stadium-signage energy. Heritage SoCal sports.
- **Editorial body: [Newsreader](https://fonts.google.com/specimen/Newsreader)** — variable serif with optical sizing. Used for pullquotes, captions, body copy in editorial blocks.
- **UI body: [Inter](https://fonts.google.com/specimen/Inter)** — clean grotesque for utility text, lists, labels.
- **Mono: [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono)** — eyebrows, technical specs, the email card. Direct callback to the original site's Courier accents.

### Colors
| Role | Hex | Use |
|---|---|---|
| Court Ink | `#0E1410` | Primary text, dark sections, nav wire |
| Windscreen Bone | `#F4F1EA` | Page canvas — warm off-white, the cream of vinyl screen |
| Paper | `#EDE7DA` | Card surfaces, secondary canvas |
| Stadium Green | `#1F3D2A` | Primary brand accent, signature mesh card, large display |
| Stadium Dark | `#152C1E` | Image bezels |
| Net Tape Red | `#C2422A` | Accent — eyebrows, dot markers, the "samples." word in the contact headline |
| Asphalt | `#5C5950` | Body-tier muted text |
| Dust | `#9A958A` | Tertiary muted text |

The stadium green is a deliberate echo of the original site's `#006400` sidebar — pulled down a few stops for sophistication. The net-tape red is the Edwards center-strap red.

### Layout
**12-column editorial grid**, asymmetric, mobile-first, long-scroll. Sections: top wire → floating sticky nav → hero → heritage marquee → capabilities bento → spec/regulation band → installations editorial gallery → Edwards heritage pullquote → process steps → contact → masthead footer with oversized wordmark.

### Signature move
**Chain-link fence pattern as a recurring CSS texture.** Pure-CSS diagonal mesh (two crossed `linear-gradient`s at ±45°) renders the diamond pattern without any image overhead. It appears as: decorative corner blocks framing the hero image, the full background of the Mesh Screen capability card, the inner texture of the Playmate card, and an overlay on the dark Edwards heritage section. It ties the whole site to what they actually do — windscreen on chain-link.

A second running motif: technical specs treated as design. The regulation tennis net dimensions (42′ × 3′6″ × 3′ + 43′ sleeve span + 30″ depth + 2′² footing) become a typographic spec system across the band between Capabilities and Installs.

### What's killed
- The 1996 sidebar nav, table layouts, `<font>` tags, and Times New Roman.
- Any "energetic startup sports" tropes — orange-to-purple gradients, "Get started for free," shouty CTA shapes.
- Generic stock tennis photography. We use NJP's own installation photos under a unified archival treatment.

### Logos used (Logo Search)
None pulled this build — venue references in the marquee and gallery are typeset in Bebas Neue rather than logos to avoid implying brand permissions we don't have. The vintage tennis-player line drawing in the favicon and brand mark is **lifted from NJP's own existing logo banner** (`Logoweb.jpg`), center-cropped — pure 1971 brand authenticity, not a search result.

### 21st.dev Component Provenance

| Mockup section | 21st.dev component | Search query | Source file | What we borrowed |
|---|---|---|---|---|
| Hero | `Hero with group of images, text and two buttons` | hero editorial heritage industrial | `21st-sources/inspiration-notes.md` | Two-column rhythm with eyebrow + tracking-tight oversized headline + outline + filled CTA pair |
| Capabilities grid | `Bento Product Features` | capabilities grid bento services | `21st-sources/inspiration-notes.md` | 3×3 grid with one tall feature card spanning two rows + supporting smaller cards |
| Heritage marquee | `Logo Cloud 4` / `Marquee Logo Scroller` | marquee logo strip clients | `21st-sources/inspiration-notes.md` | Mask-edge gradient on the marquee container + slow 60s loop + duplicated content set for seamless wrap |
| Sticky floating nav | `Floating Header` | nav sticky transparent monospace | `21st-sources/inspiration-notes.md` | `top-5` floating offset, rounded border + backdrop-blur, monospace wordmark, right-aligned single CTA |
| Footer | Default Footer (Hexagon + brand + links + legal) | footer oversized typographic editorial | `21st-sources/inspiration-notes.md` | Masthead-style top row (logo + brand on left, content on right), horizontal rule, multi-column meta block |
| Gallery | `Portfolio Gallery` | photo gallery portfolio editorial captions | `21st-sources/inspiration-notes.md` | Staggered hover-lift behavior + editorial caption rhythm under each photo |

Full notes including rationale and translation tactics live in `21st-sources/inspiration-notes.md`.

## Content Inventory

### Images pulled (from `http://www.njpsports.com/`)
- `Indian_Wells_Stadium.jpg` — 960×720, hero + featured install + OG source
- `University_of_Redlands_Field.jpg` — 960×720, featured install (wide bottom)
- `Logoweb.jpg` — 270×72, source for favicon (center-crop of vintage tennis player figure)
- `PEPPERDINE3.jpg`, `BWEdwardsP.jpg`, `9jetb.jpg`, `30ls.jpg`, `40ls.jpg`, `VINYLHILLSIDE2.jpg`, `studiocitya4.jpg` — capability cards + featured installs (288–576px tall)
- `Champ.jpg`, `comboposts.jpg`, `enviroinstall.jpg`, `greenstadium4.jpg`, `CENTERSTRAP.jpg` — held in `images/` for future use, not in current mockup

All photos are treated with a unified `archival` (or `archival-strong` for the hero) CSS filter that combines grayscale + contrast + sepia. This hides 90s JPEG artifacts and reads as a single editorial portfolio.

### Key copy used
- "Specialists in custom-fabricated windscreen for tennis courts, baseball fields, yard fences, privacy fences, wrought iron, front gates, and overhead." (verbatim from homepage)
- "In business since 1971." / "On the web since 1996." (verbatim)
- "Edwards… have manufactured tennis equipment since 1884… used at Wimbledon, the Olympics, and on the professional tour." (paraphrased from `nets.html`)
- All regulation specs (42′ × 3′6″ × 3′, 43′ sleeve span, 3″ post diameter, 30″ sleeve depth, 2′² footing) — verbatim from `nets.html` and `tennispost.html`.
- All contact details (phone, fax, email, address, license, mailing) — verbatim from homepage footer block.

### Links preserved
- Phone (toll-free + local)
- Fax (display only)
- Email (mailto)
- Playmate's product site (`playmatetennis.com/products/`) — same outbound link as the source `ballmachines.html`
- USAPA (`usapa.org`) — same outbound link as the source `paddletennis.html`

## Share Preview

- **OG image source:** Indian Wells Stadium photo (sourced from `http://www.njpsports.com/Indian Wells Stadium.jpg`), scaled by `sips` to 630 height then cropped to 1200×630 from center. JPEG q85.
- **OG image path:** `images/og.jpg` (1200×630, ~228 KB)
- **OG title:** `NJP Sports Inc — Windscreen & Tennis Specialists · Since 1971`
- **OG description:** `Custom-fabricated windscreen and tennis court equipment in Glendale, California. Family-run since 1971. Edwards nets, Playmate ball machines, installs from Indian Wells to Pepperdine.`
- **Twitter card:** `summary_large_image` with same image + title + description
- **Favicon source:** Center 72×72 crop of `Logoweb.jpg` (the green-panel vintage tennis-player line drawing), upscaled to 192×192 (`favicon.png`) and 512×512 (`favicon-512.png`) via PIL bicubic
- **Theme color:** `#0E1410` (Court Ink)
- **Sub-pages with their own OG:** None — single-page mockup

## Image Generation Prompts

Auto-generation skipped this build (Grok / Gemini API keys not set in this session). Three Grok-ready upgrade prompts for atmospheric assets are documented in `IMAGE_LOG.md` under "Grok Imagine prompts" — all non-text, non-business-specific atmospheric per the project's image accuracy rules. Drop into Grok Imagine, save into `images/`, then push.

## Suggested Next Mockups

- **Capabilities detail page** — long-scroll spec sheet for mesh and vinyl, with material chips, hem styles, grommet spacing diagrams, and a downloadable spec PDF.
- **Installations index** — filter by venue type (stadium / NCAA / club / private / parks-and-rec) with proper case-study writeups.
- **Quote-builder form** — mobile-first form where a customer enters fence run length, height, and screen choice and gets an estimate range plus a "we'll mail samples" confirmation. Replaces the current "call or email" model with something a contractor could send to a homeowner from their phone.
- **Pickleball conversion guide** — given how often clubs and parks now ask about it, a visual layout showing four pickleball courts inside one tennis court, post heights, net lengths.
- **Edwards / Playmate brand pages** — proper distributor pages for each, with the heritage story upfront and product specs below.

## Build Timing

| Phase | Duration |
|---|---|
| Step 1: READ (homepage + 19 sub-pages + 15 images + Yelp attempt) | ~1m 30s |
| Step 2: DIRECTION (Pro-Max skill + 6 21st.dev searches) | ~25s |
| Step 3: BUILD (HTML + favicon + OG image) | ~3m 00s |
| Step 4: VERIFY (preview, snapshots, mobile reflow, email-card fix) | ~1m 15s |
| Step 5: BRIEF + ACCURACY + IMAGE_LOG | ~45s |
| **Total before publish** | **~6m 45s** |

PUBLISH and DELIVER timings appended to delivery message.

## Round 2 Changelog

After Daddy flagged that the first pass under-represented the actual catalog and that "the work doesn't live at Playmate Tennis":

### Capabilities expanded — 10 cards → 17 lines, three groups

**Group A · Custom Fabrication** (cut, hem, grommet, label, on the Glendale floor)
- A.01 Custom Mesh Screen (flagship — open & closed knit polyethylene, custom heights to 15′)
- A.02 Custom Vinyl Screen
- A.03 **NEW: Printed & Designed Screens** (custom logos / graphics on mesh or vinyl — was missing)
- A.04 **NEW: Temporary Screen / Construction Screen** (premade panels + 150′ rolls — was missing)
- A.05 Padding & Polycap (4″ fence guard, 250′ rolls, baseball bunting — was thin)
- A.06 Baseball · Golf · **Custom Netting** (#42 HDPE, batting cages, ball containment, plant structures — custom-netting use case was missing)

**Group B · Tennis Court Equipment** (Edwards · England · since 1884)
- B.01 Tennis Nets (Edwards 30 LS / 40 LS, 47′ cable)
- B.02 Tennis Posts (Edwards Classic round 3″ steel)
- B.03 **NEW: Post & Net Installation as a service** ($525–$650, LA / Orange / Ventura — was missing the flat pricing and tri-county scope)
- B.04 Court Cleaning (9-jet waterbroom, special non-scuff ¾″ hose in 75/100/150′ lengths, foam court rollers)
- B.05 **NEW: Court Valets, Trash & Scorekeepers** (Court Valet $70, Courtserve trashcan/ball collector $225 — was missing)
- B.06 Umpire Chairs & Benches (2532 aluminum chair 6′ tall, 2502/3 5′ polyurethane benches)

**Group C · Authorized Distribution + Other Sports**
- C.01 **Playmate Ball Machines** (authorized SoCal sales & service)
- C.02 **NEW: Playmate Ball Mowers** (also authorized — was conflated with ball machines)
- C.03 **NEW: First Team Basketball Backboards** (authorized distributor — was generic "basketball backboards")
- C.04 Volleyball / Paddle / Pickleball (combo posts, sleeves, USAPA-compliant pickleball conversion)
- C.05 **NEW: How to Measure & Install Windscreen** (free in-house resource — was missing)

### Distributors band added
A new dedicated section after Capabilities — heading: **"THE BRANDS WE CARRY, NOT WHERE THE WORK LIVES."** — three cards for Edwards (England, since 1884), Playmate (authorized SoCal), and First Team (authorized distributor). This separates the "what we stock and service" from the "where we installed" question, which the first pass conflated.

### Venue marquee corrected
Removed Edwards + Playmate (they're not places NJP installed — they're brands NJP carries). Added Harvard-Westlake (custom batting cage), Sunset Hills T.C. (mesh logo print), Malibu (closed-mesh awning), and the LA / Orange / Ventura tri-county service tag.

### Installs gallery expanded
Added four text-only callouts beneath the photo gallery for Harvard-Westlake (school batting cage), Sunset Hills T.C. (logo print), Malibu (residence), and Baseball Field (printed blue vinyl). Re-captioned the U. of Redlands photo to call out that the image actually shows a printed-vinyl Farquhar Field outfield wall — a real printed-screens receipt.

### Process section expanded
Added a **"How to Measure & Install Windscreen"** free-resource callout (the actual notes NJP hands to its crews — tension-bar to tension-bar, no panel longer than 50–60′, plan seams to land on a fence post, standard heights 3′ / 6′ / 8′ / 10′ / 12′ measured from valley to valley of the chainlink diamonds), plus a service-area block clarifying the difference between **screen install (Greater LA)** vs **net & post install (LA / OC / Ventura)** vs **shipping (worldwide)** vs **samples (by mail)**.

### Nav update
Added a **BRANDS** link to the desktop nav for the new Distributors section anchor (`#brands`).

### Accuracy callout removed
The Round 1 mesh wind-block ratios ("~70% open / ~95% closed") were industry typicals, not NJP-quoted figures. Replaced with descriptive copy that matches what the source site actually says about visibility behind open vs. closed mesh.

## Production Notes

To build this into a real site, use Claude Code (Opus, high effort) in **HANDOFF MODE**. The vanilla HTML mockup translates cleanly to **Next.js + Tailwind** if NJP wants a CMS-driven site (case studies, capabilities, contact form), or to **Astro** if they want a fast static site with the same long-scroll structure. Either way, lift the chain-link CSS pattern verbatim, extract the editorial grid utilities, port the `archival` photo filter, and switch the brand image set to professionally re-shot installation photography (the existing 960×720 Indian Wells image is the highest-res asset they have on the public web and is not retina-grade for a real production site).
