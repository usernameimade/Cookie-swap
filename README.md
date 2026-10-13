# Cookie Swap 🍪

Put any picture on the big cookie in **Cookie Clicker**. Works with the **Steam version** (as a mod) and the **browser version** (as console code or a bookmarklet).

Everything runs in your browser. Your image is never uploaded anywhere.

## How to use

1. Open `index.html` (or the GitHub Pages link for this repo).
2. Upload, paste, or drag in a picture. Drag to move it, use the sliders to zoom and rotate.
3. Pick where you play:

### Steam version
1. Click **Download mod (.zip)**.
2. In Steam, right-click **Cookie Clicker** → **Manage** → **Browse local files**.
3. Open `resources/app/mods/local` and extract the zip there.
4. Start the game, go to **Options → Mods**, turn the mod on, and restart.

To go back to the normal cookie, turn the mod off and restart.

### Browser version
1. Copy the generated code.
2. On the Cookie Clicker tab, press `F12`, open **Console**, paste, and press `Enter`.

Or save it as a bookmark and click it on the game tab. Reloading the page restores the normal cookie.

## How it works

The tool crops your image to a 256×256 PNG and uses the game's built-in image swap:

```js
Game.Loader.Replace("perfectCookie.png", yourImage);
```

The Steam mod wraps that in `Game.registerMod(...)` so it runs every time the game starts. It only changes a picture, so it doesn't touch your save, and the mod allows Steam achievements.

## Credits

Made by Sean Gudmundson. Cookie Clicker is made by Orteil and Opti (DashNet). This project isn't affiliated with them.
