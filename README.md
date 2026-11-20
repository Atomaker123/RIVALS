# RIVALS

RIVALS is an original, browser-playable solo arena FPS built with Three.js. It takes inspiration from the pace of competitive arena shooters while using original branding and procedural environments.

## Play

Open `index.html` through a local static web server (ES modules and WebGL imports generally do not work from a `file://` URL). For example:

```bash
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000) in a modern desktop browser. Internet access is needed to load Three.js and the optional Google font. Click **Play Match** and allow pointer lock.

## Features

- First-person WASD movement, mouse look, sprint, jump, crouch, and sprint-slide.
- Ten selectable weapons, reloads, magazines, reserve ammo, weapon-specific fire cadence, spread, pellet shot, and melee.
- Bot opponents, hitscan aiming, health, eliminations, respawns, hit markers, match timer, and elimination win target.
- Five procedurally assembled arenas: City Showdown, Desert Facility, Neon Arena, Warehouse Warfare, and Skyline.
- Elimination, timed, and practice match options.
- Local browser XP, levels, wins, and saved sensitivity, FOV, and volume settings.
- Responsive menu and HUD; simple synthesized firing/UI sounds.

## Controls

| Input | Action |
| --- | --- |
| WASD | Move |
| Mouse | Look |
| Left click | Fire (click the canvas again if pointer lock is released) |
| Shift | Sprint |
| Space | Jump |
| Ctrl | Crouch; press while sprinting to slide |
| R | Reload |
| 1 / 2 / 3 | Equip primary / secondary / melee |
| Q or mouse wheel | Cycle weapons |
| Esc | Pause / release mouse |

## Scope and limitations

This version is a local single-player game, not a networked multiplayer service. There is no authoritative remote server, online matchmaking, player-vs-player synchronization, account system, or cross-device progression. Progression is stored in this browser's `localStorage` and can be cleared by browser data cleanup. The 3D environment, opponents, and effects use procedural primitives instead of external art/audio assets. A production multiplayer game requires a separately deployed backend and server-side validation; no multiplayer functionality is claimed here.

## Technology

Static HTML/CSS/JavaScript with Three.js loaded as an ES module from jsDelivr. No build step is required. Serve the repository root over HTTP as described above.
