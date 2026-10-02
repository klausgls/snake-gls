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

## Partners

`partners.html` is Partners, the Danish Ludo variant played with cards, using the official rules and card deck by Game Inventors. 4 players form 2 teams, and partners sit opposite each other: Team 1 is Red and Green, Team 2 is Yellow and Blue. Each player gets 4 parcels to deliver from their depot around the road and into their finish lane. The first team to deliver all 8 parcels wins.

- **Setup:** each seat can be Human or Computer. Computer players can be Easy or Normal. With **Hidden** hands, a handoff screen hides the table between human turns so the laptop can be passed around. This screen is skipped when only one human plays. **Open** shows every hand. There is no leaderboard.
- **How to play** (on the setup screen and in the footer) opens an easy-to-read rules page you can check at any time, even mid-game. Hover over a card to see what it does.
- **Cards** (the Partners deck, 52 cards: 13 kinds × 4): ♥ = bring a parcel out · ♥/8 and ♥/13 = out, or move 8 / 13 · 1/14 = move 1 or 14 · −4 = 4 backwards · 7 = split 7 steps over any number of parcels · Swap = swap any two parcels on the road · 2, 3, 5, 6, 9, 10, 12 = move that many. Only heart cards bring parcels out.
- **Rounds:** everyone gets 4 cards. Each dealer shuffles once and deals 3 times, and then the next player deals. Partners swap 1 card before each deal is played. If you can't play any card, you put down your hand until the next deal. Once your own parcels are delivered, you move your partner's.
- **Board:** landing on a single parcel of another colour (partner included) knocks it home. Two parcels of the same colour on one square are protected, so a parcel landing on them goes home itself. Parcels on their own start square block every other colour from passing and can't be swapped. Finish lanes fill from the inside, and too high a count bounces back.

| Key / mouse | Action |
| --- | --- |
| Click card → parcel → square | Choose a move |
| Enter | Confirm move / show cards on the handoff screen |
| Backspace or Esc | Undo |
| M | Mute sound |

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
