# Vitapeps : installer ton appli sur l’iPhone

Dossier à héberger : `index.html`, `manifest.webmanifest`, `sw.js` et le dossier `icons/`.
Garde-les tous dans le même dossier, sans les renommer.

## 1. Mettre les fichiers en ligne (gratuit)

### Option A : Netlify (la plus rapide)
1. Crée un compte gratuit sur netlify.com.
2. Dans « Sites », glisse-dépose le dossier `vitapeps` (le dossier entier, décompressé).
3. Netlify te donne une adresse du type `https://nom-au-hasard.netlify.app`. Tu peux la renommer dans les réglages du site.

### Option B : GitHub Pages
1. Crée un compte gratuit sur github.com, puis un dépôt public nommé `vitapeps`.
2. « Add file » puis « Upload files » : envoie `index.html`, `manifest.webmanifest`, `sw.js` et le dossier `icons`.
3. « Settings » puis « Pages » : choisis la branche `main`, dossier `/ (root)`, puis enregistre.
4. Après une minute environ, ton adresse est `https://TON-PSEUDO.github.io/vitapeps/`.

Le dépôt ne contient que le code de l’appli. Tes données personnelles ne sont jamais envoyées en ligne : elles restent dans ton téléphone.
(Les noms exacts des boutons peuvent varier un peu selon les mises à jour de ces sites.)

## 2. Installer sur l’iPhone
1. Ouvre l’adresse dans **Safari** (pas dans l’appli Claude).
2. Touche **Partager**, puis **Sur l’écran d’accueil**, puis **Ajouter**.
3. Lance Vitapeps depuis l’icône de Peps : l’appli s’ouvre en plein écran, sans barre Safari.

## 3. Récupérer tes données actuelles
Une appli installée a son propre stockage : elle démarre vide. Pour récupérer ce que tu as déjà saisi :
1. Dans l’ancienne page (Safari ou Claude) : onglet **Objectifs**, carte **Sauvegarde**, bouton **Copier mes données**.
2. Dans l’appli installée : onglet **Objectifs**, carte **Sauvegarde**, colle dans la zone de transfert, puis **Importer le texte**.
3. Alternative : **Exporter (fichier)** puis choisis ce fichier dans la zone d’import.

Refais une sauvegarde de temps en temps : si tu supprimes l’appli de l’iPhone, les données disparaissent avec elle.

## 4. Mettre à jour l’appli plus tard
1. Remplace `index.html` en ligne (et les autres fichiers si je t’en fournis de nouveaux).
2. Dans `sw.js`, change `vitapeps-v1` en `vitapeps-v2` (puis v3, etc.). Sans ça, l’iPhone garde l’ancienne version en cache.
3. Ouvre l’appli deux fois : la nouvelle version s’active à la deuxième ouverture.

## 5. Ce que cette version ne fait pas
- **Pas de widget natif iOS.** Il faut une vraie appli Swift (WidgetKit) pour ça. Le bouton 📱 de l’appli ouvre un « mode widget » compact, qui reste une page de l’appli.
- Les données ne se synchronisent pas entre appareils. Utilise la sauvegarde pour les déplacer.
- Hors ligne, tout marche. Seule la police Nunito est remplacée par la police du téléphone si elle n’a jamais été chargée.
