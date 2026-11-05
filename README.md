# Iris – Bluetooth control for Philips Hue Iris

A web app that controls your Hue Iris lamp directly over Bluetooth, with no Hue Bridge.
Everything fits on one screen:

- **Color:** color wheel, 36-color palette, color code input, recent colors and favorites.
- **White:** warm to cool slider with Candle, Warm, Soft, Neutral, Daylight and Cool presets.
- **Scenes:** steady colors in Christmas, Everyday and Moods sets.
- **Effects:** Christmas lights, Merry cycle, Candy cane, Fireplace, Snowfall, Starry night, Candlelight, Breathe, Aurora, Ocean, Rainbow, Party, Sunrise and Sunset.
- **Timers:** focus timer that flashes the lamp, and a sleep timer that fades it out.
- **Schedule:** colors, whites, effects or off at set times and days.
- **Settings:** theme, page glow, full brightness, install, pairing help, diagnostics, activity, DEV.

Colors and scenes always use full brightness. You can turn this off in Settings.

**Scenes vs effects:** a scene sets one steady color, and the lamp keeps it even after you close Iris.
An effect keeps changing the light on its own, and runs only while Iris is open.

**Smooth changes:** scenes, palette colors, favorites and turning on fade over 3 seconds by default.
Settings → Light → Color changes goes from Instant to Very slow (10 s).

**Automatic reconnect:** Iris reconnects to your lamp when it opens. Chrome and Edge need one
setting for this, and Settings → Light → Turn on automatic reconnect shows how to enable it.

## Install it like a Windows app

1. Open https://anthodupre.github.io/HUE/ in Chrome or Edge.
2. Go to Settings and click **Install Iris**, or click the install icon at the right of the address bar.
3. Iris opens in its own window and appears in the Start menu. Right-click it to pin it to the taskbar.

Right-clicking the taskbar icon offers shortcuts: Christmas lights, Fireplace, Focus and Turn off.

## Developer mode

Settings → Help → DEV, then type the code `BURGER`. It unlocks a simulated lamp (works without
Bluetooth), a command counter, a dropped-connection test, an effects demo and a data reset.

## Mettre le site en ligne (une seule fois)

1. Sur GitHub, ouvre le dépôt, puis **Settings → Pages**.
2. Sous **Build and deployment → Source**, choisis **GitHub Actions**.
3. Va dans l'onglet **Actions**, ouvre « Deploy to GitHub Pages » et clique **Run workflow**
   (ou pousse un commit).
4. L'adresse du site s'affiche à la fin du déploiement, du genre
   `https://anthodupre.github.io/hue/`.

Si le déploiement refuse la branche, va dans **Settings → Environments → github-pages**
et autorise la branche utilisée (ou fusionne dans `main`).

## Utilisation

- Ouvre le site dans **Chrome** ou **Edge** sur un ordinateur avec le Bluetooth activé.
  Safari et Firefox ne gèrent pas le Web Bluetooth. Sur Android, Chrome fonctionne aussi.
- Ferme l'application Hue sur ton téléphone : la lampe n'accepte qu'une connexion à la fois.
- Clique **Connect your Iris** et choisis la lampe. Si elle n'apparaît pas, rends-la
  détectable depuis l'app Hue, ou clique « Show all Bluetooth devices ».
- Si elle se connecte mais ne change pas, appaire-la d'abord dans les réglages Bluetooth
  de l'ordinateur, puis reconnecte-toi.
- Chrome peut installer le site comme une application (icône d'installation dans la barre d'adresse).

Les horaires et le minuteur ne marchent que tant que la page reste ouverte et l'ordinateur allumé.

## Tester en local

Le Web Bluetooth exige HTTPS ou `localhost` :

```bash
python3 -m http.server 8000
```

Puis ouvre `http://localhost:8000` dans Chrome.

## Version

Le numéro de version s'affiche sous le titre « Iris ». Il change à chaque mise à jour,
ce qui permet de voir si la page a bien été rafraîchie. Il se trouve dans `index.html`
(constante `VERSION`).
