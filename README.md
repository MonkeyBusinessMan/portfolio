# Portfolio — Quentin Féret, Product Designer UX/UI

Site statique (HTML + images, sans dépendance ni étape de build) : trois cas d'étude autour du design system — SNCF Gares & Connexions, Île-de-France Mobilités, Conseil d'État — et une page À propos.

## Structure

```
index.html                 Accueil / table des matières
cas01-resume.html          SNCF G&C — résumé
cas01.html                 SNCF G&C — parties 01 à 09
cas01-realisations.html    SNCF G&C — réalisations
cas01-produits.html        SNCF G&C — produits et presse
cas02-*.html               Île-de-France Mobilités
cas03-*.html               Conseil d'État
apropos.html               À propos
assets/                    Images
.nojekyll                  Indique à GitHub Pages de servir les fichiers tels quels
```

## Voir le site en local

Ouvrir `index.html` dans un navigateur suffit. Ou, depuis ce dossier :

```
python3 -m http.server 8000
```
puis http://localhost:8000

## Déployer sur GitHub Pages

1. Créer un dépôt sur GitHub, par exemple `portfolio` (ou `<votre-identifiant>.github.io` pour une adresse à la racine).
2. Déposer le contenu de ce dossier à la racine du dépôt :
   - via l'interface : **Add file → Upload files**, glisser tous les fichiers et le dossier `assets`, puis **Commit changes** ;
   - ou en ligne de commande :
     ```
     git init
     git add .
     git commit -m "Portfolio"
     git branch -M main
     git remote add origin https://github.com/<identifiant>/portfolio.git
     git push -u origin main
     ```
3. Dans le dépôt : **Settings → Pages → Build and deployment**, Source = **Deploy from a branch**, Branch = `main` / `/ (root)`, puis **Save**.
4. Après une à deux minutes, le site est en ligne à `https://<identifiant>.github.io/portfolio/`.

Le fichier `.nojekyll` est caché sur certains systèmes : vérifier qu'il est bien envoyé (il est inclus si vous déposez le dossier entier en ligne de commande).

## Modifier

Chaque page est un fichier HTML autonome, styles inclus. Pour remplacer une image, garder le même nom de fichier dans `assets/`.
