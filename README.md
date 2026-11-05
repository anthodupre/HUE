# Iris – contrôle Bluetooth pour Philips Hue Iris

Une page web qui pilote ta lampe Hue Iris directement en Bluetooth, sans pont Hue.
Couleur, blanc chaud/froid, luminosité, favoris, horaires et minuteur de concentration.

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
