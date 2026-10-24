# Moon City

A SimCity-2000-style Moon colony game. One static file (`index.html`), no build step, no server, no dependencies.

## Publish checklist
- Everything lives in `index.html`. All URLs are relative. Host from the repo root (GitHub Pages, main/root).
- The GoatCounter line must stay as the last line before `</body>`. No other analytics.
- Saves are local only (browser localStorage, 3 slots). Keep the save format compatible between versions.
- Update recipe on github.com: edit `index.html` in place in the web editor (never delete/replace), commit on a scratch branch, open a PR, merge, then check the live site hash matches.
- Free only: no paid services.

## Phone performance
- Canvas pixel ratio is capped at 1.5 on phones.
- When the game is paused and nothing moves, drawing drops to about 10 frames per second. Any touch wakes it.
- Hidden tabs stop drawing. Zoomed-out view skips small details. Smoke and walking figures are capped.

## Controls
- Drag to pan, pinch or wheel to zoom, tap to inspect or place.
- Bottom tabs: Zones, Power, Life, Tubes, Civic, Sights, Tools.
- `! N` button shows what is missing. Level terrain tool flattens craters and mountains.

## Features added since v1.3
- Visuals: roof beacons, welding sparks, stars, Earth, dust, 8 looks each for industry and tourism, Starship-style rocket on the spaceport, per-zone colour palettes, surface rovers (no outdoor people).
- Zone-colour view button, City advisors window (Builder, Treasurer, Engineer), power panel shows MW short and how to fix it.
- Power rebalance: solar 50 MW, small reactor 212 MW, fission reactor 500 MW, Battery Bank 18750 MWh, new Large Battery 62500 MWh, charging 37.5 percent faster.
- Fullscreen button, installable (manifest.json, icons). Bottom Start over removed; Menu has My cities and Start over.
- Undo last action (round arrow, right column). Bulldozing is free, no refund.
- Mini-map at left: tap or drag to jump the camera.

See `BACKLOG.md` for the idea list.


## Version history
- v0.84 (24.10.2026): services go local - medical, security/police, fire and kindergarten coverage are measured per home by walking distance along tubes; schools use city-wide capacity. Three new service map layers (security, medical, education); every map legend now uses three colour bands (low/medium/high at 33/67) with explicit ranges like 67-100. Home card lists what would improve that home ('up to +N' when the benefit is capacity-limited). Placement helper previews service radius and homes in range. Promenade moved to the Civic tab with drag-build and live price. Old saves convert gradually over 12 in-game months. Saves compatible.
- v0.82 (24.10.2026): five academies named after scientists (Hypatia, Comenius, Curie, Turing, Franklin) with info cards and sources; education moves to kindergartens (30%, 250 capacity) and schools (70%, 800), academies no longer count as an education service; happiness map shows the local-happiness breakdown per home with a legend fix. Old saves with over 5 academies keep the generic look. Saves compatible.
- v0.81 (23.10.2026): 'Did you know?' fact cards in building info cards (Deep Ice-Water Mine, Solar Array, reactors). Saves compatible.
- v0.80 (20.10.2026): Horizon Space & AI Academy; education services repeatable; education and health advisors; items page gains an academy card and education coverage lines. Saves compatible.
- v0.79 (19.10.2026): gameplay rebalance from live-city feedback: 3x3 towers now count as weak land-value sources (radius 5); industry dust fades smoothly - full effect within 2 tiles, gone at 6 (was a flat 4-tile square with a hard edge); demand now responds directly to taxes (+-0.03 per point from 9%), happiness (continuous, replacing the low-happiness cliff), blackouts (-0.3 commerce/industry) and land value. Battery chip plainly states night coverage (green 'battery supply OK', or red days-vs-night). Happiness map is a smooth gradient so dusty streets read visibly dimmer. RCI demand panel ~25% smaller with the mini-map attached under it. Land-value map renders ~50x faster on big cities and counts towers (legend: sights and towers). Map legend Hebrew RTL fix. Saves compatible, no migration.
- v0.78 (18.10.2026): local happiness - every home has its own happiness from nearby parks, sights, promenades, dust, smell and the military base, with a new Happiness map layer and a Nearby places line in the city sheet; growth slows in unhappy streets and speeds up in happy ones. New Deep Ice-Water Mine look. Advisors warn early (water/oxygen margin under 15%, power reserve under 20%) and the red ! panel shows how many residents are short of water, oxygen and power. Lava caves 7% larger for new games. Hebrew UI, saves compatible.
- v0.77 (18.10.2026): save safety - autosave failure now warns instead of failing silently; every save keeps the previous state as a restorable backup in Saved cities; Continue opens the most recently saved city.
- v0.76 (18.10.2026): HUD credits abbreviated (K/M/B) with the full total in the city sheet; 13 new scientist monuments with faces (pop gates 5000-9800, Copernicus through Fermi); tap a built monument in Sights to jump to it, plus a My monuments bar. Hebrew UI, saves compatible.
- v0.75 (18.10.2026): next-milestone line under the population counter; 4 new late-game event cards (settler shuttle, static storm, Earthrise festival, rest day demand). Hebrew UI, saves compatible.
- v0.74 (18.10.2026): one military base per city, cracked-building finder chip with jump, page fade-in, favicon.
