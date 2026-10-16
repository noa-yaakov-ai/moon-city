# Moon City

A SimCity-2000-style Moon colony game. One static file (`index.html`), no build step, no server, no dependencies.

## Publish checklist
- Everything lives in `index.html`. All URLs are relative. Host from the repo root (GitHub Pages, main/root).
- The GoatCounter line must stay as the last line before `</body>`. No other analytics.
- Saves are local only (browser localStorage, 3 slots). Keep the save format compatible between versions.
- Update recipe on github.com: delete old `index.html`, upload the new one, rename `1-index.html` to `index.html`, then check the live site hash matches.
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
