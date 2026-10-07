# Bracket Maker

A tournament bracket for streams in a single file (`index.html`). There is no server or database, and no Twitch login is needed.

## How it works
- **Images** stay in the streamer's browser (IndexedDB). Nothing is uploaded.
- **Voting:** viewers type `1` or `2` in Twitch chat. The page reads chat through Twitch's anonymous read-only connection, so there is no login, no Twitch app and no API key. Each viewer gets one vote, and their last vote counts.
- **Uneven numbers** are fine. If the count isn't a power of 2 (e.g. 11), some entries get a free pass (bye) in round 1.

## Hosting (free)
**Cloudflare Pages:** dash.cloudflare.com → Workers & Pages → Create → Pages → *Upload assets* → drag this folder in → Deploy. That's it.
(GitHub Pages or Netlify Drop work the same way. You can also run it locally: `python3 -m http.server` in this folder.)

## Streaming setup
1. Open the site, drop in the images, and click **Shuffle & create bracket**.
2. Enter your Twitch channel name and click **Connect**.
3. Click **Open stream window ↗** and add that window to OBS as a *Window Capture*. Keep the main tab open for the controls.
   (Or hide the panel with `H` and capture the main window itself.)

## During the stream
| Key | Action |
|---|---|
| `Space` | Next step: reveal match → start vote → end vote |
| `1` / `2` | Pick the winner manually (also for ties) |
| `U` | Undo |
| `H` | Show/hide the control panel |
| `Esc` | Close the full-size image |

- Click any `?` matchup to play it next.
- Click any revealed image (in the bracket or the VS panel) to show it full size on stream. Click again to close.
- Double-click the title to rename the tournament, or use the **Tournament title** field at the top of the controls.
- **Hide names** replaces all names with "Top" / "Bottom". Viewers can vote with `1`/`2` or `top`/`bottom`.
- You can drag the poll box anywhere on screen.

Everything is saved automatically, so a refresh or crash won't lose the tournament.
