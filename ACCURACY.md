# Accuracy Review — NJP Sports Inc

Cross-referenced against [njpsports.com](http://www.njpsports.com/) homepage and sub-pages: `mesh.html`, `vinyl.html`, `nets.html`, `tennispost.html`, `courtcleaning.html`, `ballmachines.html`, `chairs.html`, `paddletennis.html`, `volleyball.html`. Source site is plain HTTP only — HTTPS does not resolve.

## Verified

Pulled directly from the source site and confirmed in the mockup:

- **Business name** — "NJP Sports Inc" / "N.J.P. SPORTS INC." ✓
- **Tagline** — "Windscreen & Tennis Specialists" / "Windscreen and Tennis Accessories" ✓
- **In business since 1971** ✓ (homepage: "IN BUSINESS SINCE 1971")
- **On the web since 1996** ✓ (homepage: "ON THE WEB SINCE 1996")
- **Toll-free phone 800-773-4657** ✓
- **Local phone 818-247-3914** ✓
- **Fax 818-247-2605** ✓
- **Email njpsports@earthlink.net** ✓
- **Shop address** — 548 W. Arden Ave., Glendale, CA 91203 ✓
- **Mailing address** — Box #1469, Glendale, CA 91209-1469 ✓
- **Contractor's License No. 284844 C-13** ✓
- **Greater Los Angeles install + worldwide ship** ✓ ("AS A CONTRACTOR, WE INSTALL WITHIN THE GREATER LOS ANGELES AREA. WE SHIP THROUGHOUT THE WORLD.")
- **Wholesale supplier + manufacturer** ✓ ("NJP SPORTS IS A WHOLESALE SUPPLIER AND MANUFACTURER")
- **Custom-fabricated windscreen for tennis courts, baseball fields, yard fences, privacy fences, wrought iron, front gates, overhead** ✓
- **Edwards (England) tennis nets distributor** ✓ (nets.html: "imported from England... manufactured tennis equipment since 1884")
- **Edwards used at Wimbledon, Olympics, ATP tour** ✓ (nets.html)
- **Tennis net regulation specs** ✓ (nets.html: "A tennis net is 42' wide and 3'6" tall on the sides... 3'3" tall in the middle before a center strap is installed - 3' after")
- **Edwards Classic posts: 3-inch round steel, internal brass winder** ✓ (tennispost.html: "round, 3-inch-diameter steel tubing with an internal brass winder mechanism")
- **Post sleeves set 42'6" to 43' apart for doubles** ✓ (tennispost.html)
- **Post sleeves "usually about 30" deep" with 2'×2' cement footing** ✓ (tennispost.html)
- **Authorized Playmate sales & service for SoCal** ✓ (ballmachines.html: "We are the authorized sales and service center for Playmate ball machines for the Southern California region.")
- **Playmate website link `playmatetennis.com/products/`** ✓
- **Pepperdine University 1999 NCAA Tennis Finals court** ✓ (mesh.html: "This court is at Pepperdine University where the 1999 NCAA Tennis Finals were played.")
- **UCLA / LA Open / Marcelo Rios reference** ✓ (nets.html: "This is at UCLA during the LA Open with Rios working out and making lots of noise!")
- **Studio City Golf and Tennis Club green vinyl on 12' fence** ✓ (vinyl.html: "This court is at the Studio City Golf and Tennis Club.")
- **Hollywood Hills hillside privacy install** ✓ (vinyl.html: "This screen is in the Hollywood Hills where privacy is important.")
- **Indian Wells Stadium image** ✓ — image file `Indian Wells Stadium.jpg` is named on the homepage and we use the file the brand serves itself
- **University of Redlands** ✓ — image file `University of Redlands Field.jpg` similarly served from the brand's own site
- **Pickleball / USAPA conversion info link** ✓ (paddletennis.html: "The USAPA is a great source for info for rules and layout: https://www.usapa.org/")
- **Mesh + vinyl + temporary screen + nets + posts + court cleaning + ball mowers + ball machines + umpire chairs + benches + paddle tennis + volleyball + basketball backboards + baseball/golf netting + padding/polycap** — all 14+ product categories present ✓

## Flagged for Daddy

Items written to fill gaps where the source site is silent. Confirm or replace before client delivery:

- **Hours: Mon–Fri 7am–4pm Pacific** — *Sourced from external listing (Yelp result in Web Search)*. Not stated on the source site itself. Confirm with NJP directly before any client uses these hours.
- **"54 years" since-1971 stat** — derived from current year (2026) minus 1971 = 55. The site copy says "over 50 years"; mockup uses **54** rounded to the most recent full-year figure assuming 1971 founding mid-year. Could be 54 or 55; either is honest. If founder records show a specific month, swap.
- **Mesh wind-block ratios "~70% (open) / ~95% (closed)"** — these are typical industry figures for open vs. closed mesh windscreen, not numbers the source site quotes. Plausible filler. Confirm against NJP's spec sheet before client uses.
- **"Same numbers as 1996. Same workshop as 1971."** — copy I wrote for the contact section. Numbers and address match what's on the current site, but I can't independently verify they are unchanged since 1996. Confirm.
- **Tagline "WINDSCREEN & TENNIS SPECIALISTS."** — derived from "Windscreen and Tennis Specialists" (homepage h2) and "Windscreen & Tennis Accessories" (subpage banner). I joined the two and uppercased. Faithful but not a direct quote.

## Fixed during review

Caught and corrected before publishing:

- Email card on mobile was breaking `njpsports@earthlink.net` mid-character because `display-tight text-4xl break-all` was too wide for the 375 px column. Switched to `font-mono text-base` and added a `<wbr>` between handle and domain so the line break (when it does happen) lands at the `@`. Also added a "Same address since '96." display line beneath the email to make the heritage callback intentional.
- Several specifications quoted on the source site as "Note - currently only available in GREEN" (the court hose) and other inventory-state remarks were intentionally not surfaced in the mockup — they're transient stock conditions, not brand truths.

## Source pages fetched

```
http://www.njpsports.com/                       homepage (200, 9.4 KB)
http://www.njpsports.com/mesh.html              200, 47 KB
http://www.njpsports.com/vinyl.html             200, 36 KB
http://www.njpsports.com/tempscreen.html        200, 24 KB
http://www.njpsports.com/photo.html             200, 17 KB
http://www.njpsports.com/padbunt.html           200, 12 KB
http://www.njpsports.com/netting.html           200, 15 KB
http://www.njpsports.com/nets.html              200, 28 KB
http://www.njpsports.com/tennispost.html        200, 23 KB
http://www.njpsports.com/tennispostnetinstall.html  200, 15 KB
http://www.njpsports.com/courtcleaning.html     200, 17 KB
http://www.njpsports.com/courtorder.html        200, 17 KB
http://www.njpsports.com/ballbaskets.html       200, 12 KB
http://www.njpsports.com/ballmachines.html      200, 9 KB
http://www.njpsports.com/chairs.html            200, 17 KB
http://www.njpsports.com/paddletennis.html      200, 18 KB
http://www.njpsports.com/volleyball.html        200, 20 KB
http://www.njpsports.com/basketball.html        200, 16 KB
http://www.njpsports.com/measure.html           200, 14 KB
http://www.njpsports.com/photoc.html            200, 12 KB
```
