# TP1 – Créer un projet collaboratif complet sur GitHub

### Objectifs

- Créer un mini-projet local (frontend ou backend léger)
- Le versionner avec Git
- Publier sur GitHub
- Ajouter un·e collaborateur·trice
- Rédiger une documentation
- Initier le travail collaboratif (branche, PR, merge)
- Déployer (si applicable)

---

### Partie 1 – Créer un projet local

1. Créer un projet simple :
    - Si le profil est frontend : une landing page HTML/CSS/JS
    - Si le profil est fullstack : un petit projet Node.js/Express qui affiche “Hello World” sur `/`
2. Initialiser un dépôt Git local :
    
    ```bash
    git init
    git add .
    git commit -m"Initial commit"
    
    ```
    

---

### Partie 2 – Publier sur GitHub

1. Créer un **dépôt public** sur GitHub : nom `tp1-github-collab-prenom-nom`
2. Associer le dépôt local :
    
    ```bash
    git remote add origin https://github.com/<utilisateur>/tp1-github-collab-prenom-nom.git
    git branch -M main
    git push -u origin main
    
    ```
    

---

### Partie 3 – Ajouter un collaborateur

1. Aller dans le dépôt GitHub → Settings → Collaborators
2. Ajouter un collaborateur par son nom d’utilisateur GitHub
3. Demander à cette personne de valider l’invitation

---

### Partie 4 – Travail collaboratif : branche et Pull Request

1. Créer une nouvelle branche :
    
    ```bash
    git checkout -b feature-header
    
    ```
    
2. Ajouter un élément au projet (ex : un header HTML ou une nouvelle route dans Express)
3. Commit et push :
    
    ```bash
    git add .
    git commit -m"Add header section"
    git push origin feature-header
    
    ```
    
4. Sur GitHub : créer une **Pull Request** vers la branche `main`
5. Assigner le collaborateur comme reviewer
6. Simuler un processus de validation et merger la PR

---

### Partie 5 – Documentation

Créer un fichier `README.md` contenant :

- Titre du projet
- Description du projet
- Technologies utilisées
- Instructions d’installation
- Auteur et collaborateurs
- Lien vers le déploiement (si applicable)

---

### Partie 6 – Déploiement

1. **Frontend** : utiliser GitHub Pages
    - Aller dans Settings → Pages
    - Branch: `main`, Folder: `/root`
    - Publier et ajouter le lien dans le README
2. **Backend** : documenter la future publication via Render, Railway, etc. (à faire dans TP3/4)

---

### Partie 7 – Livrables attendus

- Lien GitHub du projet
- README complet
- 1 Pull Request créée et mergée
- Capture d’écran de l’ajout du collaborateur
- Lien vers la page déployée (si applicable)