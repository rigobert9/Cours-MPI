# Algorithmique des graphes
## Définitions
### Graphes orientés
> Un graphe orienté est un couple $G = (S;A)$ avec $S$ un ensemble fini de sommets
> et $A \subset S^2$ ses arcs.

Si $(x,y) \in A$, on a une arc $x \to y$. Il ne peut exister qu'une unique
arc entre deux sommets (sinon, c'est un multigraphe, avec $A$ un multiensemble).
$x$ est alors un prédécesseur de $y$ et $y$ un successeur ou voisin de $x$.
On appelle une arc $x \to x$ une boucle, et on fera (sauf contre-indication)
l'hypothèse que le graphe n'en comporte pas.

On note $d_+(x)$ le degré sortant de $x$, soit le nombre de successeurs de $x$;
$d_-(x)$ son degré entrant, le nombre de prédécesseurs.

> On dit qu'il existe un chemin entre $x$ et $y$ lorsqu'il existe une séquence
> de sommets commençant par $x$ et $y$ pour laquelle il existe une arc entre
> chaque membre successif de la séquence. La séquence de ces arcs est le chemin.
> La longueur de cette séquence est appelée longueur du chemin. On note $x
> \to^{\ast} y$.

(Il y a donc un élément de moins dans le chemin que dans la séquence de
sommets)

Un chemin simple est un chemin qui ne passe pas 2 fois par un même sommet.
Un cycle est une chemin simple de longueur plus grande que $0$, et un graphe ne
possédant pas de cycle est dit acyclique.

On dit que deux sommets $u$ et $v$ sont connexes si $u \to^{\ast} v$ et $v \to^{\ast} u$.
La relation de connexité est une relation d'équivalence (ce qui n'est pas le cas
de simplement avoir un chemin). Une composante fortement connexe d'un graphe est
une classe d'équivalence pour cette relation. S'il n'y a qu'une seule classe
d'équivalence, on dit que le graphe est fortement connexe.

### Graphes non orientés
> Un graphe orienté est un couple $G = (S;A)$ avec $S$ un ensemble fini de sommets
> et $A$ un ensemble de paires de $S$ ses arêtes.

Comme on représente toujours des couples en informatique, on représente toujours
ces graphes comme des graphes orientés en imposant $x \to y \Rightarrow y \to x$.

Les définitions précédentes sont identiques, mais on remarquera qu'il n'existe
pas de cycle de longueur 2 dans un graphe simple (un graphe qui n'est pas un
multigraphe) et que les degrés sont toujours les mêmes (on parle donc juste de
degré).

De plus, $\to^{\ast}$ est désormais une relation d'équivalence et on parle de
composantes connexes (sans forcément fortes).

### Arbres et forêts
Un arbre est un graphe non orienté connexe et acyclique, et une forêt est un
ensemble d'arbres.

Un arbre a toujours une arête de moins que de sommets (prouvé par récurrence
forte).

### Graphes pondérés
> Un graphe pondéré est un triplet $G = (S,A,\omega)$
> avec $(S,A)$ un graphe orienté et $\omega : A \to E$ une fonction de
> pondération, avec $E$ un ensemble quelconque.

Si $a \in A$, $\omega(a)$ est appelé poids ou étiquette de $a$.

On utilisera souvent $\mathbb{N}$ ou $\mathbb{R}_{+}$ comme codomaine de $\omega$,
mais on verra que les automates utilisent un ensemble différent.

Le poids (ou la longueur) d'un chemin correspond à l'itération d'une opération
de $E$ sur les arcs composant un chemin.

### Graphes bipartis
> Un graphe $G = (S,A)$ est dit biparti si on peut partitionner $S = S_1 \uplus S_2$
> tel pour tout $x,y \in S^2 \mid x \to y \Rightarrow (x \in S_1 \land y \in S_2) \lor (x \in S_2 \land y \in S_1)$.

## Structures de données
On suppose ici sans perte de généralité (par bijection) que les sommets sont
$[\![0;n-1]\!]$ lorsqu'il y a $n$ sommets.

### Matrice d'adjacence
Une matrice d'adjacence est un tableau de tableaux (ou un tableau de taille au
carré), qui ayant une ligne et une colonne pour chaque sommet, encode par `true`
la présence d'un arc et `false` son absence à la position `[x][y]` ou `[x * n + y]`
pour $x \to y$.

Cette technique a une grande complexité en espace (toujours $n^2$ pour un graphe
à $n$ sommet) et prend du temps à s'initialiser, mais permet un accès rapide (et
facile à mettre en cache) à tous les arcs et une bonne généralisation aux
graphes pondérés (tant qu'on choisit une valeur d'étiquette représentant
l'absence d'arc).

Pour les graphes non orientés, cette représentation est inefficace (besoin de
maintenir deux cases à chaque modification), à moins d'implémenter un tableau
triangle (avec une fonction de calcul) qui n'a qu'une seule valeur pour chaque
paire $\{x;y\}$.
