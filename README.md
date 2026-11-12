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

## Design and search (v3)

- **Atelier look:** warm light and dark themes, frosted glass panels, a glass lamp with a brightness
  ring, and a page that glows softly in the lamp's color. Laid out first for a window snapped to half
  the screen.
- **Search everything:** press Ctrl+K (or /) to find and run any scene, effect, white, favorite,
  timer or action.
- **Named favorites:** "Save current" asks for a name. Favorites appear under Scenes → Mine.
- **Back up and restore:** Settings → Help saves favorites, schedule and settings to a file.

## New modes (v3.1)

- **Effect builder:** Effects → Mine → New effect. Pick 2 to 6 colors and a movement (Glide,
  Hold & glide, Breathe, Twinkle), try it on the lamp, then save it with a name. Saved effects can be
  scheduled and found in search.
- **Screen sync:** Effects → Live. The lamp follows the main color on your screen, like a monitor
  backlight. Chrome asks which screen or window to share.
- **Music:** Effects → Live. The lamp pulses with the bass and changes color on the beat, using the
  microphone. Nothing is recorded or sent anywhere.
- **Pomodoro:** in Timers, the focus timer can chain breaks (green light) and focus periods, with a
  long break after every fourth focus.
- Effects are grouped: Everyday, Christmas, Cozy, Party, Live and Mine.

## More functions (v3.2)

- **Two-way sync:** when the lamp is changed from the Hue app, Alexa or a switch, Iris notices
  and updates itself.
- **Sunrise and sunset schedules:** a change can run at sunrise or sunset, shifted by up to an
  hour. Follow the day also uses the real sun times. Both need your city in Settings → Weather.
- **Colors from a photo:** Color → From a photo, or drop a picture on Iris. Click a color to send
  it to the lamp, or turn the set into an effect.
- **Busy light:** press B for a red "busy" light, and B again to go back.
- **Undo:** Ctrl+Z returns to the previous color, white or power state.

## Sound, stats and more (v3.3)

- **Soundscapes:** Effects → Sound. Rain, Ocean waves, Crackling fire and Deep focus (brown noise),
  each with a matching light. The sounds are generated live by Iris, with a volume slider. With the
  sleep timer on, the sound fades out with the lamp.
- **Timer glow:** in Timers, the lamp can show the focus time left by warming toward amber.
- **Usage stats:** Settings → Help → Stats shows time on per day this week, an energy estimate and
  your most used scenes and effects.
- **Surprise me:** Color → Surprise me, or press R, for a random color.
- **Christmas countdown** in Scenes → Christmas.

## Office features

- **Follow the day:** an effect that shifts the white with the clock, warm in the morning and
  evening and bright cool white around midday.
- **Weather:** an effect that colors the lamp with the sky or the temperature where you are.
  Set your city in Settings → Weather. Data comes from Open-Meteo, free and with no account.
- **Away from desk:** two separate switches in Settings → Away from desk. One fades the lamp out
  when you lock the computer (Windows + L). The other fades it after a set time without the mouse
  or keyboard. It fades back when you return.
- **Weather colors:** Settings → Weather → What the colors mean shows the legend.
- **Mini player:** a small always-on-top window with power, brightness and favorites. Open it with
  the button next to the status, or press M. Turn the button off in Settings → App.
- **Start with Windows:** Settings → App → Start Iris with Windows shows the steps.
- Effects that were running when you closed Iris start again when it reconnects.

## Stay awake (Awake tab)

- **Stay awake mode:** bright 6500K white at full brightness. Every 10 to 45 minutes the lamp pulses,
  suggests a quick break and asks you to tap "I'm awake". With no answer in 45 seconds it alternates
  red and white once a second and beeps. It also keeps the screen from sleeping.
- **Coffee nap:** drink a coffee, then nap 10 to 25 minutes. The lamp goes dark, a 2-minute sunrise
  starts near the end, then bright white and a beep wake you.
- **Quick boosts:** Energy breath, Energy burst (an effect cycling cool white, cyan and violet) and
  Cold white blast.
- **Energy breath:** a large circle on screen grows as you breathe in and shrinks as you breathe out,
  with the phase, a seconds countdown and the breath number. The lamp follows the same rhythm.
  Paces: Slow (5-2-7), Steady (4-2-6, default), Box (4-4-4-4) and Quick (3-1-4), for 1 to 5 minutes,
  with an optional soft sound at each change.

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
