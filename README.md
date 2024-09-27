# Scénarisation d'un projet multimédia

## L'idée

### Concept
Dans une installation interactive divisée en deux pièces, deux utilisateurs sont chacun devant un clavier tactile. Lorsqu'un utilisateur appuie sur une touche, une lumière s'illumine sur le clavier de l'autre. Si les deux utilisateurs touchent la même touche, une note de musique résonne dans les deux espaces.

````mermaid
graph TD;
    A[Utilisateur 1] -->B{Appuie sur une touche}
    B --> F[Lumière s'illumine sur le clavier 2]
    E --> |Même touche?| C[Note de musique résonne dans les deux pièces]
    B --> |Même touche?| C
    D[Utilisateur 2] -->E{Appuie sur une touche}
    E --> G[Lumière s'illumine sur le clavier 1]
````

### Objectif
L'objectif est simple : écrire un mot ensemble. Chaque pression sur une touche doit être réfléchie et enchaînée pour créer une harmonie. Lorsqu'ils parviennent à composer un mot successif, une douce mélodie retentit, les encourageant à continuer.

La tension monte alors qu'ils tentent de synchroniser leurs gestes, découvrant la magie de la collaboration à travers la musique et la lumière. La pièce se remplit de joie et d’énergie, transformant un simple mot en une véritable œuvre d’art collective.
