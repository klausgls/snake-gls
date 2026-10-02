# GLS Snake

Classic snake for the GLS company event. You drive a GLS lorry and pick up parcels; every parcel adds a GLS trailer. Hitting a wall or your own trailers ends the game.

- Players enter their name before each game.
- The leaderboard keeps each player's **best** score. Names are matched case-insensitively.
- Scores live in the browser's `localStorage`, so they stay on the machine/browser the game is played on.

## Controls

| Key | Action |
| --- | --- |
| Arrow keys / WASD | Steer |
| Space | Start round / pause |
| P or Esc | Pause / resume |
| Enter or Space (game over) | Play again |
| N (game over) | New player |

## Camilla

`camilla.html` is a Giana Sisters-style platformer. Use the **Snake / Camilla** switch in the header to move between the games. Camilla is red-haired and works for GLS. Run her through 3 levels (Morning round, The warehouse, Rush hour) to the GLS lorry at the end of each one.

- Parcels are worth 100 points, and every 30 parcels gives an extra life. Yellow `?` boxes hold parcels, and one box per level holds the **GLS cap**.
- With the cap, Camilla can smash bricks from below, and an owl hit costs the cap instead of a life.
- Stomp owls for 200 points. Leftover time is added to the score at the end of each level.
- You start with 3 lives, and each level has a checkpoint flag.
- Camilla has its own leaderboard, separate from Snake's.

| Key | Action |
| --- | --- |
| ← → / A D | Run |
| ↑ / W / Space / Z | Jump (hold to jump higher) |
| P or Esc | Pause / resume |
| M | Mute sound |
| Enter or Space (game over) | Play again |
| N (game over) | New player |

## Run locally

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8123
```

## Publish on GitHub Pages

1. Create a repository on GitHub and push this folder to the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. After a minute the game is live at `https://<user-or-org>.github.io/<repo>/`.

## On event day

- Use the same browser on the same machine all day. Scores are tied to that browser and URL.
- Don't use a private/incognito window, because its scores are thrown away when it closes. The page shows a red warning if storage is blocked.
- Press F11 (or Ctrl+Cmd+F on Mac) for full screen.
- **Reset scores** in the footer clears the leaderboard after you type `RESET`. Do this before the event if you've been testing.
