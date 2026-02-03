# TP2 – Gestion de projet + automatisation CI/CD sur GitHub

### Objectifs

- Gérer un projet collaboratif avec des issues et projets GitHub
- Documenter les contributions avec un `CONTRIBUTING.md`
- Configurer une intégration continue simple avec GitHub Actions
- Structurer les branches avec conventions
- Apprendre à résoudre un conflit lors du merge

---

### Partie 1 – Mise à jour du projet

1. Reprendre le projet du **TP1**
2. Créer une nouvelle branche `develop` à partir de `main`
    
    ```bash
    git checkout -b develop
    git push origin develop
    
    ```
    
3. Travailler désormais sur cette branche pour les futures fonctionnalités

---

### Partie 2 – Mise en place des Issues

1. Créer au moins 3 issues (exemples) :
    - Ajouter une section contact
    - Mettre en place un système de logs
    - Corriger un bug ou améliorer le responsive
2. Assigner une issue à un·e collaborateur·trice
3. Lier l’issue à une branche créée pour la corriger :
    - Exemple de nom de branche : `fix/contact-form`
    - Utiliser une convention de type `type/description`, ex : `feat/navbar`, `fix/footer`, etc.

---

### Partie 3 – Ajout d’un fichier CONTRIBUTING.md

1. À la racine du projet, créer un fichier `CONTRIBUTING.md`
2. Inclure :
    - Règles de nommage des branches
    - Convention de commit (`Conventional Commits` ou simple `feat:`, `fix:`…)
    - Étapes pour forker, cloner, créer PR, et vérifier l'intégrité du code
    - Politique de validation (ex : au moins 1 reviewer)

---

### Partie 4 – GitHub Project Board

1. Activer l’onglet **Projects** dans le dépôt
2. Créer un projet de type **Kanban** avec les colonnes :
    - To do
    - In progress
    - Done
3. Lier chaque issue à ce board

---

### Partie 5 – Ajout d’un workflow GitHub Actions (CI)

### Pour un projet **HTML/CSS** :

1. Créer un dossier `.github/workflows` avec un fichier `build.yml`
2. Exemple de contenu minimal :

```yaml
name:HTMLValidation

on:
push:
branches: [main,develop ]
pull_request:
branches: [main,develop ]

jobs:
validate-html:
runs-on:ubuntu-latest
steps:
-uses:actions/checkout@v3
-name:HTML5Validator
uses:Cyb3r-Jak3/html5validator-action@v0.5.0

```

### Pour un projet **Node.js** :

```yaml
name:Node.jsCI

on:
push:
branches: [main,develop ]
pull_request:
branches: [main,develop ]

jobs:
build:
runs-on:ubuntu-latest
strategy:
matrix:
node-version: [16.x]
steps:
-uses:actions/checkout@v3
-name:UseNode.js${{matrix.node-version}}
uses:actions/setup-node@v3
with:
node-version:${{matrix.node-version}}
-run:npminstall
-run:npmrunlint
-run:npmtest

```

---

### Partie 6 – Gestion des conflits

1. Simuler un conflit :
    - Modifier une même ligne sur `develop` et `main`
2. Créer une PR et résoudre le conflit manuellement
3. Documenter l’étape de résolution dans le README ou dans un fichier `NOTES.md`

---

### Partie 7 – Livrables attendus

- Nouveau fichier `CONTRIBUTING.md`
- Issues créées, assignées et reliées aux branches
- Projet GitHub actif (board)
- 1 Pull Request issue-based avec review
- Workflow GitHub Action fonctionnel
- Résolution de conflit simulée et commentée