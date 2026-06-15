# Care Board

A talking communication board for a tablet or phone. Tap a big square and it speaks the sentence out loud. Runs in any browser, no install.

## How to use
Open `index.html` in a browser (Chrome on Android works great). Tap a square — it speaks and shows the words. "I'm in pain" opens a second screen: pick a side (left / right / head & neck), then the body area, and it speaks a full sentence like *"My left shoulder is hot and in pain."*

The very first tap on a page may be silent — that one tap "wakes up" the phone's voice. After that every tap talks. Turn the volume up.

## Adding or changing buttons
Open `index.html` in any text editor and find the `SCREENS` section near the bottom. Each button is one line:

```
{ label:"Water", emoji:"💧", class:"c-drink", say:"I would like some water please." }
```

- `label` = text on the square
- `emoji` = the picture
- `say` = what it speaks (if left out, it just says the label)
- `class` = color (c-drink, c-comfort, c-action, c-feel, c-nav, c-yes, c-no)
- `screen` = use this instead of `say` to open another screen

To add a whole new screen, copy one of the existing screen blocks and give it a new name, then point a button at it with `screen:"yourname"`.

## Hosting free on GitHub Pages
1. Make a free account at github.com and create a new **public** repository (e.g. `care-board`).
2. Upload `index.html` (drag it into the repo's "Add file → Upload files").
3. Go to **Settings → Pages**, set **Source = Deploy from a branch**, branch **main**, folder **/ (root)**, Save.
4. Wait ~1 minute. Your site is live at `https://YOURNAME.github.io/care-board/`.
5. Open that link on the tablet/phone. (GitHub Pages uses https, which the voice feature needs.)

Tip: in Chrome on Android, use the menu → **Add to Home screen** to make it open like an app.
