# Phone Monitor PWA

Mini PWA statique pour GitHub Pages. Elle affiche uniquement les métriques exposées par le navigateur : CPU logiques, RAM approximative si disponible, quota/usage de stockage du site, réseau, écran, batterie si supportée et plateforme.

## Publier sur GitHub Pages
1. Créez un dépôt GitHub et placez ces fichiers à sa racine.
2. Commit + push sur la branche `main`.
3. GitHub : **Settings > Pages > Build and deployment > Deploy from a branch**.
4. Sélectionnez `main` et `/ (root)`, puis **Save**.
5. Ouvrez l’URL HTTPS Pages sur Android avec Chrome, puis **Ajouter à l'écran d'accueil / Installer l'application**.

## Limites
Une PWA web standard ne peut pas fournir le pourcentage CPU système, la RAM Android utilisée, les températures CPU, ni parcourir le filesystem Android complet. `deviceMemory` et Battery API peuvent aussi être absentes selon le navigateur.

## Test local
Les Service Workers nécessitent HTTPS ou localhost. Utilisez par exemple `python3 -m http.server 8080`, puis ouvrez `http://localhost:8080` sur la machine de développement.
