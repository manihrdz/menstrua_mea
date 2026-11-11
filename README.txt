# Mes cycles — application iPhone

## Ce que contient le projet
- `index.html` : application autonome, interface en français.
- `manifest.webmanifest` : métadonnées d'installation PWA.
- `sw.js` : cache hors connexion.
- `icon-192.png` et `icon-512.png` : icônes.

## Installation sur iPhone
Une PWA doit être servie depuis une adresse HTTPS. Ouvrir le site dans Safari sur l'iPhone, puis :
1. toucher le bouton **Partager** ;
2. choisir **Sur l'écran d'accueil** ;
3. activer **Ouvrir comme app web** si l'option est proposée ;
4. toucher **Ajouter**.

Pour rendre le dossier accessible en HTTPS, il faut le publier sur un hébergement statique (par exemple GitHub Pages). Le projet n'utilise aucune bibliothèque externe ni service d'analyse. Une fois chargé et mis en cache, il fonctionne hors connexion.

## Confidentialité et sauvegardes
Les données sont stockées dans `localStorage` du navigateur / de l'app web sur cet appareil. Elles ne sont pas envoyées à un serveur par le code de l'application. Elles ne se synchronisent pas automatiquement entre appareils. Utiliser l'onglet **Sauvegarde** pour exporter régulièrement le fichier JSON et le conserver dans un endroit sûr.

Attention : la suppression des données du site, la désinstallation ou la réinitialisation de l'appareil peut faire perdre les données locales. La sauvegarde exportée est donc importante.

## Algorithme
Les intervalles entre premiers jours de règles sont calculés. Pour les statistiques et prédictions, les intervalles de 15 à 90 jours sont retenus. La prédiction utilise la médiane des six derniers intervalles valides et une marge indicative liée à leur dispersion. Ce n'est ni un diagnostic ni une méthode contraceptive.


ESTIMATION CALENDAIRE DE L'OVULATION
L'application estime la prochaine date de règles à partir de la médiane des
6 derniers intervalles de cycle valides (15 à 90 jours). Elle estime ensuite
l'ovulation environ 14 jours avant cette date, et affiche une fenêtre fertile
théorique de 5 jours avant à 1 jour après cette date. Une plage élargie tient
compte de la variabilité récente des cycles.

Cette méthode reste une approximation : la durée de la phase entre ovulation
et règles varie, et l'ovulation peut être décalée ou ne pas avoir lieu. Le
calendrier ne confirme pas l'ovulation et ne doit jamais être utilisé comme
méthode contraceptive.
