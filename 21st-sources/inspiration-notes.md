# 21st.dev Inspiration Pass — NJP Sports Inc

Searches run for the Pro-Max DIRECTION step. We borrow patterns, never copy. Vanilla HTML + Tailwind CDN, so React scaffolding gets stripped.

## Hero — "Hero with group of images, text and two buttons"
**Query:** `hero editorial heritage industrial`  
**Component:** Hero with group of images, text and two buttons  
**Borrowed:** the asymmetric two-column rhythm with a small badge eyebrow, a tracking-tight oversized headline, a muted-foreground supporting paragraph, and a paired image grid on the opposite column. We replace the right-side three-tile grid with a single full-bleed Indian Wells photo, but keep the proportions and the "outline + filled" CTA pattern.

## Capabilities — "Bento Grid"
**Query:** `capabilities grid bento services`  
**Component:** Bento Product Features  
**Borrowed:** the 3-column / 3-row grid where one tall card spans the full height (our "Custom Windscreen" feature) and several shorter cards fill the remainder. Translated to vanilla `grid-template` and Tailwind utility classes.

## Heritage marquee — "Logo Cloud 4" / "Marquee Logo Scroller"
**Query:** `marquee logo strip clients`  
**Component:** Logo Cloud 4 / Marquee Logo Scroller  
**Borrowed:** the masked-edge infinite-marquee pattern (linear-gradient mask on the container), uppercase wordmarks rather than logos, and the slow 40s loop speed. We render venue names typographically (Indian Wells, Pepperdine, UCLA, etc.) instead of logos because we don't want to imply endorsement we don't have rights to.

## Nav — "Floating Header"
**Query:** `nav sticky transparent monospace`  
**Component:** Floating Header  
**Borrowed:** the `top-5` floating offset, rounded border + backdrop-blur, monospace wordmark on the left, and the right-aligned single CTA. We anchor the eyebrow with `EST. 1971` in JetBrains Mono.

## Footer — "Footer (Default)"
**Query:** `footer oversized typographic editorial`  
**Component:** Footer (with logo + brand name + social + main links + legal)  
**Borrowed:** the masthead-style top row (logo + brand name on the left, social icon row on the right), then a horizontal rule, then a multi-column meta block. We swap the link columns for full address blocks, contractor license, hours.

## Gallery — "Portfolio Gallery"
**Query:** `photo gallery portfolio editorial captions`  
**Component:** Portfolio Gallery  
**Borrowed:** the staggered hover-lift behavior and the editorial caption rhythm under each photo. Translated to vanilla CSS `transform` + `transition` because we don't ship Framer Motion.
