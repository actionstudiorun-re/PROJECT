# SUIVI PROJET — Version 4

Application locale autonome de suivi des projets IRD.

## Nouveautés de cette version

- suppression complète des validations ;
- deux liens dédiés dans chaque projet :
  - ressources fournies par l’IRD ;
  - dossier Dropbox des livrables Action Studio ;
- liens visibles et cliquables dans les rapports HTML destinés à l’IRD ;
- publication automatique du rapport global vers GitHub ;
- création ou remplacement automatique du même fichier `index.html` ;
- test de connexion GitHub ;
- historique des publications ;
- le jeton GitHub est stocké séparément dans le navigateur :
  - il n’est pas inclus dans les sauvegardes JSON ;
  - il n’est pas inclus dans les rapports HTML.

## Configuration GitHub

Dans **Données & réglages > Publication automatique sur GitHub**, renseigner :

- compte ou organisation ;
- dépôt ;
- branche, généralement `main` ;
- fichier publié, généralement `index.html` ;
- adresse publique GitHub Pages ;
- jeton GitHub à permissions fines.

Le jeton doit être limité au dépôt utilisé et disposer de :

- **Repository permissions > Contents: Read and write**.

Pour GitHub Pages gratuit, utiliser un dépôt public et configurer :

- **Settings > Pages** ;
- **Deploy from a branch** ;
- branche `main` ;
- dossier `/ (root)`.

## Utilisation

1. Configurer GitHub une seule fois.
2. Tester la connexion.
3. Depuis le tableau de bord, cliquer sur **Publier le rapport sur GitHub**.
4. Choisir les projets et le niveau de détail.
5. Le fichier configuré est remplacé automatiquement.
6. L’équipe IRD conserve toujours la même adresse publique.

## Sécurité

Le jeton GitHub reste dans le stockage local du navigateur. Ne pas transmettre le dossier complet du logiciel ni donner accès à la session Windows utilisée pour administrer le suivi.

Les rapports IRD excluent toujours :

- heures passées ;
- taux horaire ;
- rentabilité ;
- notes internes ;
- réglages GitHub ;
- jeton GitHub.
