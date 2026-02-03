# Notes de Résolution de Conflit

## Contexte
Un conflit a été simulé entre la branche `develop` et la branche `sim-conflict` sur le fichier `index.html`.

- **develop** : `<title>Projet TP2 - Version B</title>`
- **sim-conflict** : `<title>Projet TP2 - Version A</title>`

## Résolution
Le conflit a été résolu en choisissant un titre qui combine les deux versions ou en sélectionnant la version la plus appropriée.
Choix final : `<title>Projet TP2 - Gestion de Projet (Final)</title>`

## Commandes utilisées
```bash
git checkout develop
git merge sim-conflict
# Conflit détecté
# Modification manuelle de index.html
git add index.html
git commit -m "chore: merge sim-conflict and resolve title conflict"
```
