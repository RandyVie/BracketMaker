# Bracket Maker

A tournament bracket for streams in a single file (`index.html`). Upload images, keep them hidden, and let Twitch chat vote each matchup until there's a champion.
There is no server or database, and no Twitch login is needed.

---

## Tutorials

### 1. Get it running
No installing or hosting needed:
1. On this GitHub page, click the green **Code** button → **Download ZIP**, and unzip it anywhere.
2. Double-click **`index.html`**. It opens in your browser and works right away, including Twitch chat.

> Use **Chrome** or **Edge** for this. Always open the same `index.html` file, because your images and bracket are saved per browser and per file location. If you move the folder, start a new tournament.

### 2. Create your first tournament
1. Double-click `index.html`.
2. Type a **title**, for example *Spooky Emote Tournament 2026*.
3. **Drag your images** into the drop zone. Any number works, and GIFs stay animated.
4. Optionally rename entries. The names come from the file names.
5. Click **Shuffle & create bracket**. Every entry is now a hidden **?**.

### 3. Connect Twitch chat
1. In the controls, type your **channel name** (e.g. `kylabosman`) and click **Connect**.
2. When it says **● Listening to #yourchannel chat**, you're done.
3. Viewers vote by typing **1** or **2** (or **top** / **bottom**) in chat. Each viewer gets one vote, and if they vote again only their last vote counts.

### 4. Set up OBS
1. Click **Open stream window ↗**. A clean window with no controls opens.
2. In OBS, add a **Window Capture** source and pick that window.
3. Put your **webcam source** on top of the empty **camera frame** at the top right.
4. Keep the main browser tab (with the controls) on your second monitor.

> Only one screen? Press **H** to hide the controls and capture the main window instead. The controls button disappears when the mouse is still.

### 5. Run a match
Press **Space** three times:
1. **Reveal** the next matchup. The two images appear big in the VS panel.
2. **Start voting.** The poll and timer start.
3. **End voting** early (optional). Otherwise it ends when the timer runs out.

The winner moves to the next round automatically. Repeat until the 👑 champion gets confetti.

### 6. Fix mistakes
- **Tie?** Press **1** or **2** to pick the winner yourself.
- **Wrong result?** Press **U** to undo.
- **Refreshed the page or browser crashed?** Nothing is lost. Everything saves automatically.

---

## Reference

### Keyboard shortcuts
| Key | Action |
|---|---|
| `Space` | Next step: reveal match → start vote → end vote |
| `1` / `2` | Pick the winner manually (also for ties) |
| `U` | Undo |
| `H` | Show/hide the control panel |
| `Esc` | Close the full-size image |

### More features
- Click any `?` matchup to play it next instead of the default order.
- Click any revealed image to show it **full size** on stream. Click again to close.
- Double-click the title to rename the tournament, or use the **Tournament title** field in the controls.
- **Hide names** shows "Top" / "Bottom" instead of file names.
- The **camera + VS panel** can be turned off for a full-width bracket.
- You can drag the poll box anywhere on screen.
- **Test votes** (+1 / +2) let you try everything without chat.

### Good to know
- Images are stored **only in the browser you uploaded them in**. Set up the tournament on the PC you stream from.
- If the number of entries isn't a power of 2 (e.g. 11), some entries get a free pass (bye) in round 1.
