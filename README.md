# Site de l'application Google (page d'accueil + confidentialité)

Mini site statique pour valider le branding OAuth dans Google Cloud Console.

## Fichiers
- `index.html` : page d'accueil de l'application
- `privacy.html` : règles de confidentialité
- `style.css` : mise en forme

## 1. À personnaliser avant publication
Remplacer dans `index.html` et `privacy.html` :
- `MonApp` → le nom exact de votre application (identique à celui de l'écran de consentement)
- `VOTRE_EMAIL@exemple.com` → votre adresse de contact
- Tous les passages entre `[crochets]` → description réelle, données Google et scopes réellement demandés

## 2. Publier avec GitHub Pages
1. Créer un dépôt **public** (ex. `monapp`) et y pousser ces fichiers à la racine.
2. Settings → Pages → Source : `Deploy from a branch` → branche `main`, dossier `/ (root)`.
3. Après quelques minutes, le site est en ligne :
   - Accueil : `https://nyv3s.github.io/monapp/`
   - Confidentialité : `https://nyv3s.github.io/monapp/privacy.html`

## 3. Vérifier la propriété (Google Search Console)
1. Aller sur https://search.google.com/search-console
2. Ajouter une propriété de type **Préfixe d'URL** : `https://nyv3s.github.io/monapp/`
3. Choisir la méthode « Fichier HTML », télécharger `googleXXXXXXXX.html`, le placer à la racine du dépôt, pousser, puis cliquer sur « Valider ».
4. Utiliser le **même compte Google** que celui du projet Google Cloud.

## 4. Renseigner Google Cloud Console
Google Auth Platform → Branding :
- Page d'accueil de l'application : `https://nyv3s.github.io/monapp/`
- Règles de confidentialité : `https://nyv3s.github.io/monapp/privacy.html`
- Domaine autorisé : `nyv3s.github.io`

Les deux URL doivent être différentes, publiques et répondre sans connexion.
Attendre ~24 h après la vérification, puis cliquer sur « Demander une nouvelle validation ».

## Remarque
`nyv3s.github.io` est un domaine partagé GitHub : Google accepte parfois mal ce type de domaine. Si la validation échoue encore, un domaine personnalisé (ex. via un CNAME) vérifié dans Search Console est la solution la plus fiable.
