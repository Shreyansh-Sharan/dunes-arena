# Dunes Arena · Multiplayer FPS

A lightweight browser shooter on six original maps, including three classic-style arenas (Sandstorm, Villa and Bazaar). Five weapons from sidearm to scoped sniper, right-click aiming, AI bots or friends by invite code, plus dash, double jump, overshield and pulse scan.

Built with Unity 6 (WebGL build) with a React lobby. Part of [Shreyansh Sharan's portfolio](https://shreyanshsharan.com/), split into its own site.

```bash
npm install
npm run dev      # http://localhost:5173
npm run build    # production build in dist/
npm run lint     # oxlint
```

The site is a single page: `#/` is the game's menu, and the same query parameters the portfolio used still work
(for example `#/?auto=...` to skip the menu, `#/?join=CODE` for an invite link).

## Controls

- `Space` ×2 Double jump
- `Q` / `Shift` Dash
- `E` Overshield (+50)
- `F` Pulse scan: see enemies through walls
- `1` P9 Sidearm: always carried
- `2` Vespa SMG: fast, accurate on the move
- `3` Kestrel AR: the all-rounder
- `4` Longbow: bolt-action, two-level scope
- `5` Mastiff: pump shotgun, brutal up close

## Ads and gear

Optional AdSense and Amazon affiliate IDs come from environment variables (see `.env.example`). Leave them empty and
no ad or shop code loads.

## The Unity build

`public/games/arena/` is the WebGL build of the shooter (Unity 6, `unity/ArenaShooter` in the portfolio repository). The React page is the lobby and the full-screen player that embeds it in an iframe; launch options go in the URL (`?mode=solo|host|join&bots=&diff=&name=&code=`). Rebuild the game in Unity and copy the `Build/` folder here to update it.
