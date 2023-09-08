# Calcul pratique sur les matrices
## Opérations élémentaires
> Une matrice de transvection $T_{i,j}(\lambda)$ est une matrice de la forme
> $I_n + \lambda E_{i,j}$ pour $i \neq j$ et $\lambda \in \mathbb{K}$
> (on rajoute un coefficient en $(i,j)$ sur l'identité).

> Une matrice de dilatation $D_i(\lambda)$ est de la forme
> $I_n + (\lambda - 1) E_{i,i}$, pour $\lambda \in \mathbb{K}^{+}$
> (on change un coefficient diagonal).

> Une matrice de permutation $P_{\sigma}$, pour $\sigma \in \mathfrak{S}_n$,
> place tout $1$ diagonal en $j$ vers $\sigma(j)$.

On rappelle que $E_{i,j} E_{k,l} = \delta_{j,k} E_{i,l}$.

On obtient les propriétés suivantes sur ces matrices "de transformation" (les
preuves se font facilement et de plusieurs façon différentes):
- $T_{i,j}(\lambda) T_{i,j}(\mu) = T_{i,j}(\lambda + \mu)$
- $D_i(\lambda) D_i(\mu) = D_i(\lambda \mu)$
- $P_\sigma P_\tau = P_{\sigma \circ \tau}$

Attention, les deux dernière matrices n'existent qu'en version matrice carrée
(ce qu'on fera en général). Les matrices de transvection peuvent être
généralisées.

Toutes ces familles sont donc inversibles (en suivant les propriétés montrées
au-dessus), et leur inverse est leur transposée.

### Effet sur les matrices
La multiplication $M T_{i,j}(\lambda)$ ajoute $\lambda$ fois la colonne $i$
à la colonne $j$ et laisse les autres inchangées. La multiplication dans l'autre
sens agit sur les lignes.

Les dilatations multiplient la colonne (ou la ligne quand la dilatation est à
gauche) concernée par $\lambda$.

Les matrices de permutation appliquent la permutation entre les colonnes (ou la
ligne quand la dilatation est à gauche).

## Calcul de rang, déterminant, inversion
### Rang
> Si $A$ est inversible alors $\text{rg}(AB) = \text{rg}(B)$,
> et si $B$ est inversible $\text{rg}(AB) = \text{rg}(A)$.

On peut opérer sur les lignes et colonnes de $A$ sans changer le rang avec les
matrices de transformation vues plus haut.

### Déterminant
Puisque le déterminant est un morphisme pour la multiplication, et que le
déterminant de de $D_i(\lambda)$ est $\lambda$ et $\text{det}(P_\sigma) = \varepsilon(\sigma)$
et $\text{det}(T_{i,j}(\lambda)) = 1$, on obtient aisément
le déterminant d'une matrice tant qu'on peut la ramener par nos opérations (à
droite ou à gauche) à une matrice triangulaire.

Puisque le groupe symétrique est engendré par les transpositions, qui sont
toutes de signature $-1$. Comme la signature est l'unique morphisme de
$(\mathfrak{S}_n, \circ)$ à $(\{-1,1\}, \times)$, on choisira en pratique
d'uniquement faire des échanges de lignes ou colonnes (qui ont pour signature et
donc déterminant $-1$).

Avec ces méthode de calcul, on pourra donc calculer le déterminant par pivot de
Gauss. On peut raccourcir les preuve en montrant que les matrices de permutation
sont engendrées par les matrices de transvection et de dilatation.

On rappelle que $GL_n(\mathbb{K})$ est le groupe des matrices inversibles (qui
est engendré par les matrices de transformation (preuve du pivot de Gauss)) et
$SL_n(\mathbb{K})$ est son sous-groupe qui est le noyau pour le déterminant.
$SL_n(\mathbb{K})$ est engendré par les transvections (et est donc stable par
transvections).

### Résolution de systèmes
Résolution des systèmes par pivot de Gauss (voir première année).
