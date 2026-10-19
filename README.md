# Cinescope - Part 2

## Membres
- raphael.vazzano
- leo.menaldo

## 1. Bouton de réservation
- **Problème :** Impossible d'accéder au bouton avec le clavier.
- **Impact :** Certains utilisateurs ne pouvaient pas réserver.
- **Vérification :** Tester avec `Tab`, `Entrée` et `Espace`.

## 2. Fermeture de la modale
- **Problème :** La croix ne fonctionnait pas au clavier.
- **Impact :** Difficile de fermer la fenêtre sans souris.
- **Vérification :** Utiliser `Tab` puis `Entrée` sur la croix.

## 3. Gestion de la modale
- **Problème :** Le focus était mal géré et `Échap` ne fermait pas la fenêtre.
- **Impact :** L'utilisateur pouvait se perdre dans la navigation.
- **Vérification :** Tester le focus, `Échap` et l'annonce du titre avec un lecteur d'écran.

## Corrections
- Utilisation de `showModal()`.
- Ajout d'un vrai bouton "Fermer".
- Correction du titre avec `aria-labelledby`.
