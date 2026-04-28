# Image Log — NJP Sports Inc

No API image generation in this build. The brand's own site has 50+ years of real installation photos hosted on its own domain — those are the right asset, even though they're 90s-CDN-small. They're treated with a unified archival CSS filter (`grayscale 0.85 + contrast 1.08 + sepia 0.18`) which:

1. hides JPEG compression artifacts
2. unifies the 12 source images into one editorial language
3. reads as archival / heritage — which lines up with the 1971 brand story

## Images downloaded from source

All sourced from `http://www.njpsports.com/` — same domain as the live brand site, so they're authoritative, not stock.

| File | Source path | Size | Used for |
|---|---|---|---|
| `Indian_Wells_Stadium.jpg` | `/Indian%20Wells%20Stadium.jpg` | 960×720 | Hero image (right column) + Featured Install 01 + OG share preview |
| `University_of_Redlands_Field.jpg` | `/University%20of%20Redlands%20Field.jpg` | 960×720 | Featured Install 06 (wide bottom of gallery) |
| `Logoweb.jpg` | `/Logoweb.jpg` | 270×72 | Source for the favicon — center 72×72 crop is the vintage tennis-player line drawing on dark green; that becomes the brand mark |
| `PEPPERDINE3.jpg` | `/4" TALL WEBPHOTOS/PEPPERDINE3.jpg` | 384×288 | Featured Install 02 |
| `Champ.jpg` | `/4" TALL WEBPHOTOS/Champ.jpg` | 432×496 | Reserved (not currently in mockup, keeping in folder for future) |
| `BWEdwardsP.jpg` | `/4" TALL WEBPHOTOS/BWEdwardsP.jpg` | 409×360 | Capability 04 — Tennis Posts |
| `9jetb.jpg` | `/4" TALL WEBPHOTOS/9jetb.jpg` | 576×412 | Capability 05 — Court Cleaning |
| `30ls.jpg` | `/4" TALL WEBPHOTOS/30ls.jpg` | 397×288 | Featured Install 03 — UCLA |
| `40ls.jpg` | `/4" TALL WEBPHOTOS/40ls.jpg` | 418×288 | Capability 03 — Tennis Nets |
| `comboposts.jpg` | `/4" TALL WEBPHOTOS/comboposts.jpg` | 102×432 | Reserved |
| `enviroinstall.jpg` | `/4" TALL WEBPHOTOS/enviroinstall.jpg` | 360×288 | Reserved |
| `VINYLHILLSIDE2.jpg` | `/4" TALL WEBPHOTOS/VINYLHILLSIDE2.jpg` | 432×288 | Capability 02 — Vinyl Screen + Featured Install 05 — Hollywood Hills |
| `greenstadium4.jpg` | `/4" TALL WEBPHOTOS/greenstadium4".jpg` | 400×288 | Reserved |
| `studiocitya4.jpg` | `/4" TALL WEBPHOTOS/studiocitya4".jpg` | 384×288 | Featured Install 04 — Studio City G&T |
| `CENTERSTRAP.jpg` | `/4" TALL WEBPHOTOS/CENTERSTRAP.jpg` | 132×288 | Reserved |

## Derived images (built locally, no API)

| File | Built from | Dims | Used for |
|---|---|---|---|
| `og.jpg` | `Indian_Wells_Stadium.jpg` cropped to 1200×630 with `sips`, JPEG q85 | 1200×630 | Open Graph + Twitter card share preview |
| `favicon.png` | Center crop of `Logoweb.jpg` (the green vintage tennis-player figure) | 192×192 | Browser tab favicon |
| `favicon-512.png` | Same center crop, scaled to 512 | 512×512 | Apple touch icon |

## Auto-generation attempted

Attempted Grok Imagine for one atmospheric "windscreen detail" hero asset before falling back to source photos.

```
2026-04-27 21:14 — Tier 1 Grok Standard 2K, 16:9, 1 image
Result: 401 Bad credentials — XAI_API_KEY is not set in this shell
Action: skipped per CLAUDE.md "never block the build waiting for images" 
        and proceeded with brand-served photos. Prompt preserved 
        below for Daddy to run in Grok Imagine when convenient.
```

`GEMINI_API_KEY` was likewise not set this session.

**Total auto-generation cost: $0.00** (no successful API calls).

## Grok Imagine prompts — for Daddy to run if/when desired

Each prompt follows `GROK_IMAGE_PROMPTS.md`: 50–100 words, prose, lead with subject, includes lighting + camera. All non-text, non-business-specific atmospheric — safe per `feedback_image_accuracy.md`.

### Upgrade Prompt 1 — Hero atmospheric / share preview alt

- **Slot:** Hero right column (replaces Indian Wells if a cleaner hero is desired) and/or alternate `og.jpg`
- **Aspect ratio:** 16:9
- **Prompt:**
> Tight close-up photograph of weathered green vinyl tennis-court windscreen attached to a chain-link fence in Glendale, California, at golden hour. The vinyl shows fine canvas weave texture, brass grommets at the top edge holding the screen with white nylon ties, and faint diagonal shadows from the chain-link diamonds visible behind it. Late-afternoon raking sidelight pulls warm amber tones across the surface and casts long shadows from the fence wires. Documentary craftsman photography, shallow depth of field, 50mm lens, fine grain, subtly desaturated palette of dusty green, warm cream, asphalt black. No people, no logos, no readable text.
- **Why:** Closer, more tactile alternative to the brand's existing 960×720 stadium photo. Reads as craft + material rather than venue.

### Upgrade Prompt 2 — Workshop atmospheric (between sections)

- **Slot:** Optional break section between Capabilities and Installations
- **Aspect ratio:** 21:9
- **Prompt:**
> Wide-angle photograph of a sun-lit fabrication workshop floor in Glendale, California. Long rolls of green vinyl windscreen and black mesh fabric stacked on industrial steel shelving, brass grommet press in the foreground, a sewing machine on a wood-top bench, fluorescent shop lights overhead with warm late-afternoon sun coming through high frosted windows. No people. The mood is quiet, ordered, working. Documentary photography, 28mm lens, deep depth of field, slightly desaturated industrial palette of olive green, raw steel, warm cream, ochre wood. No logos, no readable text.
- **Why:** Adds a "how it's made" beat between specs and installs without trying to depict the actual NJP workshop (we don't have reference). Generic enough to be honest.

### Upgrade Prompt 3 — Edwards-detail still-life (heritage band)

- **Slot:** Optional, behind the "Edwards · Est. 1884" pull-quote section
- **Aspect ratio:** 3:2
- **Prompt:**
> Close-up still life photograph of a single black tennis post head with a polished brass winder mechanism and a removable steel handle, placed on weathered concrete with a coil of white nylon cable beside it. Late-afternoon side-light from the right rakes across the brass, picking up faint patina, and casts a long shadow across the concrete. Editorial product photography, 85mm lens, very shallow depth of field, archival heritage palette of polished brass, soot black, raw concrete. No logos visible, no readable text.
- **Why:** A heritage detail that lets the Edwards / 1884 callout earn its weight without misrepresenting the actual Edwards Classic post.

## Notes on treatment

The CSS filter applied to all source images:

```css
.archival         { filter: grayscale(0.85) contrast(1.08) brightness(0.96) sepia(0.18); }
.archival-strong  { filter: grayscale(1)   contrast(1.18) brightness(0.88) sepia(0.22); }
```

`.archival-strong` is reserved for the hero image where mood matters most. `.archival` is the default for capability cards and gallery thumbnails. The result reads as a single editorial portfolio rather than a CDN dump from 1996.
