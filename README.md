# Cinescope - Part 2

## Membres

- raphael.vazzano
- leo.menaldo

## Constats

### 1.

### 2.

### 3.

### 4. Dialog

Problème : la modale n'avait pas de nom pour les lecteurs d'écran et la croix de fermeture n'était pas utilisable au clavier.

Correction :

- Ouverture avec showModal : la page derrière est bloquée, le focus reste dans la modale et Échap la ferme.
- Le titre de la modale est relié à la modale avec aria-labelledby.
- La croix est maintenant un vrai bouton avec le label "Fermer".
- Suppression des attributs inutiles (role, aria-modal) et du fond fait à la main.

### 5.

## Justifications

- 1 - X
- 2 - Y
- 3 - Z
- 4 - Un vrai dialog avec showModal gère déjà le focus, le blocage de la page et Échap, donc c'est plus fiable que de le refaire à la main. Un vrai bouton est utilisable au clavier et annoncé comme bouton, ce qui n'était pas le cas d'une croix en span.
