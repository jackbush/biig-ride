# Bikepacking Tour Planning Site

## Project Overview
Planning website for a 5-month solo bikepacking tour across Europe (May–October 2026). The rider is leaving from the UK, flying to Georgia, and riding through Turkey, Albania, Montenegro, up the Italian Apennines, then doing a counterclockwise loop of the Alps finishing in Nice.

**Built with:** Astro 6, MDX for long-form content, vanilla CSS (no framework). Deployed to GitHub Pages.

## Key Context

### The rider
- NZ passport holder (important for Schengen calculations and France bilateral visa agreement)
- Based in Uzès, France until April 7, 2026 (81 Schengen days used Jan 17 – Apr 7)
- Industrial designer by training, works in product design/management. Loves photography and drawing plants.
- Technically proficient mountain biker, fit. Riding a hardtail with 2.2"+ tires and bikepacking bags.
- Budget: €15-25/day. Wild camping. Minimal spending.
- Has ridden the Torino-Nice Rally before (was pushed to road options by unfit friend — wants to redo off-road sections, especially Little Peru)
- Has ridden Triglav (Slovenia) twice — not interested in Julian Alps detour

### Schengen calculations
- France stay: Jan 17 – Apr 7, 2026 = 81 days used
- Greece transit: ~3 days in mid-July
- Enter Italy for Alps: ~September 5 → ~55 days available
- Alps loop needs ~45 days → comfortable margin
- NZ bilateral agreement with France potentially gives 90 extra days in France after Schengen exhausted (awaiting embassy confirmation)

### Route structure
1. **Georgia** (2 weeks, May 18 – Jun 1) — Caucasus highlights: Kazbegi, Truso, Juta, Shatili, Tusheti
2. **Turkey** (5 weeks, Jun 1 – Jul 10) — Kaçkar Mountains + Cappadocia Delight (bikepacking.com) + train skips
3. **Greece** (3 days, Jul 12-15) — Transit only through Thrace
4. **Albania** (2 weeks, Jul 15 – Aug 1) — Accursed Mountains, Theth, Valbona, Lake Koman
5. **Montenegro** (10 days, Aug 1-12) — Durmitor, Tara Canyon, ferry Bar → Bari
6. **Italy Apennines** (12 days, Aug 13-25) — Wolf's Lair loop (bikepacking.com) from L'Aquila, train to Turin
7. **Alps Loop** (45 days, Aug 26 – Oct 10) — Turin → Veneto → Trans-Dolomiti → Austria → Swiss Alps → French Alps → TNR off-road sections → Nice
8. **Optional France extension** — If bilateral confirmed, keep riding on the extra 90 days

### Key route inspirations / GPX sources
- Caucasus Crossing (bikepacking.com) — used for Georgia sections
- Cappadocia Delight (bikepacking.com) — Turkey loop
- Illyrian Loop / Accursed Race — Albania/Montenegro
- The Wolf's Lair (bikepacking.com) — Abruzzo, Italy
- Trans-Dolomiti (bikepacking.com) — Dolomites loop
- Zillertal Trail (bikepacking.com) — Austrian/Italian Alps
- Swiss Alpine Bike Route 1 — Switzerland
- Torino-Nice Rally (komoot collection) — Western Alps finish
- Alps Divide — French/Italian/Swiss border sections

### Bike setup
- Hardtail MTB, 2.2"+ tires, bikepacking bags (frame/seat/bar)
- Fork: likely Fox 36 SL at 130mm (recommended over RockShox SID for tour reliability)
- Sleep: Big Agnes Fly Creek 1 (2018), Cumulus 350 quilt, R~3 mat, merinos, hooded down jacket

### Design decisions
- Dark, warm editorial aesthetic. Fraunces (serif display) + DM Sans (body).
- Warm charcoal background (#1a1816), cream text (#e8e0d4), amber accent (#c47d2e).
- Content-focused, minimal decoration. Tables styled for readability.
- Sticky nav. Four pages: Overview, Route, Actions, Gear.
- Actions page has localStorage-persisted checkboxes.
- Route page is MDX rendering the full detailed plan.

## File Structure
```
src/
  layouts/
    Layout.astro          — Base layout with nav
    RouteLayout.astro     — Wraps MDX content in prose class
  pages/
    index.astro           — Overview/homepage
    route.mdx             — Full detailed route plan (long)
    actions.astro         — Checklist with localStorage persistence
    gear.astro            — Gear list and shopping
  styles/
    global.css            — All styles, CSS custom properties
```

## Future work
- GPX file generation for each leg (planning to do leg by leg)
- Interactive map showing the full route
- Country-specific info cards (visa rules, currency, emergency numbers)
- Photo/drawing journal integration once on the road
