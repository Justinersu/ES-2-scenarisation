# Scénarisation d'un projet multimédia

## L'idée

### Concept
Dans une installation divisée en deux pièces, deux utilisateurs sont chacun devant un clavier. Lorsqu'un utilisateur appuie sur une touche, une lumière bleue s'illumine sous la touche du clavier de l'autre. Si les deux utilisateurs appuient sur la même touche, une note de musique résonne dans les deux espaces et une lumière rose s'illumine sous la touche des deux claviers.

### Scénario
````mermaid
graph TD;
    A[Utilisateur 1] -->B{Appuie sur une touche}
    B --> |Différente touche?| F[Lumière bleue s'illumine sous la touche du clavier 2]
    E --> |Même touche?| C[Lumière rose s'illumine sous la même touche des deux claviers]
    B --> |Même touche?| C
    C --> H[Note de musique résonne dans les deux pièces]
    D[Utilisateur 2] -->E{Appuie sur une touche}
    E --> |Différente touche?| G[Lumière bleue s'illumine sous la touche du clavier 1]
````

### Schéma

### Objectif
L'objectif est simple : écrire un mot ensemble. Chaque pression sur une touche doit être réfléchie et enchaînée pour créer une harmonie. Lorsqu'ils parviennent à composer un mot successif, une douce mélodie retentit, les encourageant à continuer.

La tension monte alors qu'ils tentent de synchroniser leurs gestes, découvrant la magie de la collaboration à travers la musique et la lumière. La pièce se remplit de joie et d’énergie, transformant un simple mot en une véritable œuvre d’art collective.

## Moodboard

### Palette de couleurs
![palette](images/palette_de_couleurs.jpg)

### Pièces
![piece](images/moodboard_piece.png)

- Éclairages neutres (blanc/beige) tout autour de la pièce pour mettre l'emphase sur le clavier
- Murs et sols complètement noirs pour encore une fois poser l'attention sur le clavier
- Les pièces sont séparées par un rideau à peine translucent pour laisser faiblement paraître les mouvements de l'autre personne et reproduire une certaine intimité

### Clavier tactile
![clavier](images/moodboard_clavier.png)

- Le clavier est posé sur un piédestal
- Les touches s'illumine avec un éclairage bleu et un effet flou lorsque appuyées
- Si elles sont appuyées en même temps par les deux utilisateurs, elles s'illuminent en rose
- Choix du rose et des effets flous pour reproduire la connection humaine 

### Audio
[Peaceful Solitude - Eternal Warriors](https://www.youtube.com/watch?v=K0EITpmtfZ0)<br>
- Les notes de musique sont mêlées à la musique d'ambiance
- Notes qui jouent en boucle

[Cosmic Harmony - Connectionist](https://www.youtube.com/watch?v=vYFaDiqx-e8)
- Musique d'ambiance relaxante pour
- Simple afin de mettre de l'avant les notes qui jouent lorsque les utilisateurs appuient sur la même touche

## Technologie

### Matériaux
- 8-12 Lumières LED
- 1 grand rideau translucent
- 26 [M5 Unit Keys](https://shop.m5stack.com/products/mechanical-key-button-unit)
- 2 [Atom Lite ESP32](https://shop.m5stack.com/products/atom-lite-esp32-development-kit)
- 2 [ATOM PoE](https://docs.m5stack.switch-science.com/en/atom/atom_poe)
- 2 piédestals
- 8 haut-parleurs

### Logiciels
| **Logiciel**                    | **Technique**                                                              |
|---------------------------------|----------------------------------------------------------------------------|
| **Max**                         | Manipulation audio en temps réel                                           |
| **QLC+**                        | Contrôle des lumières de la pièce                                          |
| **OSC Bridge**                  | Transfert de données en temps réel entre Max et Arduino                    |
| **Arduino**                     | Configuration des lumières du clavier                                      |
