# Cinescope - Part 2

## Membres

- raphael.vazzano
- leo.menaldo

## Constats

### 1. Bouton de reservation

Le bouton de reservation n'est pas atteignable au clavier

### 2. Fermer une modale

Le bouton de fermeture de modale n'est pas atteignable au clavier

### 3. Gestion de la modale

Actuellement, la modale contient plusieurs problemes:

- Le focus ne fonctionne pas
- La touche echap ne ferme pas la modale

### 4. Dialog

Problème : la modale ne s'ouvrait pas correctement et la croix de fermeture n'était pas utilisable au clavier.

Correction :

- Ouverture avec showModal : la page derrière est bloquée, le focus reste dans la modale et Échap la ferme.
- La croix est maintenant un vrai bouton avec le label "Fermer".
- Suppression des attributs inutiles (role, aria-modal) et du fond fait à la main.

### 5. Nom de la modale

Problème : la modale n'a pas de nom, un lecteur d'écran ne sait pas de quoi elle parle quand elle s'ouvre (l'aria-labelledby pointait vers un id qui n'existe pas).

Correction :

- Le titre de la modale a maintenant un id.
- La modale est reliée à son titre avec aria-labelledby, elle est annoncée par exemple "Réserver Orbite 9".

## Justifications

- 1 - Un bouton natif est atteignable avec Tab, s'active avec Entrée et Espace et est annoncé comme bouton, ce qu'un div ne fait pas. C'est mieux que d'ajouter tabindex, role et les touches à la main.
- 2 - Sans le clavier on ne peut pas fermer la modale, donc la croix doit être un vrai bouton. On ajoute le label "Fermer" parce que le symbole × tout seul n'est pas compréhensible pour un lecteur d'écran.
- 3 - Le focus et la touche Échap sont gérés par le navigateur avec showModal, c'est plus fiable que de coder un piège à focus à la main où on risque de faire des erreurs.
- 4 - Un dialog natif sait déjà qu'il est une modale (role et aria-modal sont implicites), donc on enlève du code inutile et le fond est géré par le navigateur avec ::backdrop.
- 5 - Le nom vient du titre déjà visible, donc il n'y a qu'un seul texte à maintenir et ce que voit l'utilisateur est la même chose que ce qu'entend l'utilisateur de lecteur d'écran.
