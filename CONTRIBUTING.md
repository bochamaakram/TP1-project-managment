# Contributing

Merci de vouloir contribuer à ce projet ! Voici quelques règles pour assurer une collaboration fluide.

## Règles de nommage des branches

Utilisez les préfixes suivants pour vos branches :

- `feat/nom-de-la-feature` : Pour une nouvelle fonctionnalité.
- `fix/nom-du-bug` : Pour correction de bug.
- `hotfix/nom-du-fix` : Pour une correction urgente.

Exemple : `feat/contact-section`

## Convention de commit

Nous suivons la convention **Conventional Commits**.
Format : `type: subject`

Types courants :
- `feat` : Nouvelle fonctionnalité
- `fix` : Correction de bug
- `docs` : Documentation
- `style` : Formatage (espaces, points-virgules, etc.)
- `refactor` : Refactoring du code

Exemple : `feat: ajout du formulaire de contact`

## Workflow

1. **Fork** le dépôt.
2. **Cloner** votre fork localement.
3. Créer une nouvelle branche (`git checkout -b feat/ma-feature`).
4. Faire ses modifications et **commit**.
5. **Push** la branche (`git push origin feat/ma-feature`).
6. Ouvrir une **Pull Request** vers la branche `develop`.

## Politique de validation

- Toute Pull Request doit être revue par au moins **1 validateur** avant merge.
- Les tests (si présents) doivent passer.
