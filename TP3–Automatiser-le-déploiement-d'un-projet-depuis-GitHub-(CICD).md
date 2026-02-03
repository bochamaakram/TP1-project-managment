# TP3 – Automatiser le déploiement d’un projet depuis GitHub (CI/CD)

### Objectif général

- Créer un nouveau petit projet (frontend ou backend léger)
- Le versionner et publier sur GitHub
- Configurer un pipeline CI/CD de bout en bout
- Automatiser les tests (le cas échéant) et le déploiement
- Travailler à deux via GitHub sur des branches différentes
- Rédiger la documentation du projet

---

### Consignes générales

1. Créez un **nouveau projet** :
    - Exemple frontend : une page portfolio en HTML/CSS/JS ou un React Vite
    - Exemple backend : une API Node.js avec au moins deux routes
    - Le projet doit être **fonctionnel et simple** (15-30 min de dev max)
2. Publiez le projet sur GitHub (public) et ajoutez un·e collaborateur·trice
3. Créez un `README.md` dès le départ (description, auteur, instructions, etc.)
4. Travaillez en binôme : une personne crée une feature (branche `feature-X`), l’autre crée une autre (`feature-Y`). Chacun fait sa PR, demande une review, et merge.

---

### Partie CI/CD

Vous devez mettre en place **un pipeline automatique** de déploiement :

### Pour projet frontend :

- Déploiement via **GitHub Pages** ou **Vercel**
- Utilisez un workflow `.github/workflows/deploy.yml` pour déployer à chaque push sur `main`

### Pour projet backend :

- Déploiement sur **Render**, **Railway**, **Fly.io**, ou autre
- Utilisez les GitHub Actions pour :
    - Lancer les tests
    - Déployer automatiquement

> Si le déploiement est manuel, documentez **toutes les étapes de setup** dans un fichier `DEPLOY.md`.
> 

---

### Étapes demandées

- Un pipeline CI simple (tests, build)
- Un pipeline CD (déploiement automatique ou semi-automatique)
- Testez une **Pull Request défectueuse** : le pipeline doit échouer (ex. test cassé)
- Une fois corrigée, il doit passer et déployer automatiquement

---

### Travail collaboratif

- Utilisez des **issues** pour répartir les tâches
- Ajoutez un `CONTRIBUTING.md` si vous réutilisez celui du TP2
- Utilisez un **board GitHub** pour suivre les tâches
- Assurez-vous que chaque membre ait fait au moins une **PR avec review**

---

### Livrables

- Lien GitHub du nouveau projet
- README propre et clair
- `.github/workflows/*.yml` en place et fonctionnel
- Lien vers l’URL de déploiement
- Capture d’écran de l’échec/passage du pipeline
- Exemple d’issue traitée avec PR liée