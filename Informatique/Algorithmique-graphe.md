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

### Listes d'adjacence
On initialise une liste chaînée pour chaque sommet dans un tableau. Ces listes
chainées contiennent dans leurs nœuds les sommets vers lesquels il y a un arc.
La complexité en mémoire est ainsi conservée (avec un multiplicateur plus grand
néanmoins) à un facteur de $m$ (le nombre d'arcs dans le graphe) (c'est donc une
représentation creuse des arcs).

L'accès aux arcs (obtenir leur étiquette et vérifier leur présence) devient en
revanche $O(n)$, bien qu'un parcours de tous les voisins d'un sommet soit plus
court (seuls les voisins sont présents, pas les non-voisins), linéaire en le
degré sortant du sommet. L'ajout et le retrait de voisins sont aussi linéaires
en le degré sortant dans le pire des cas.

### Graphes pondérés
Dans le cas de la matrices d'adjacence, on peut mettre les valeurs d'étiquettes
dans le graphe, tant qu'on a des valeurs particulières réservées à l'absence
d'arc et à la valeur pour soi-même (sauf si elle est omise). Ainsi, il est utile
de choisir des flottants pour les poids, puisqu'ils sont munis de valeurs
spéciales (0, NaN, $+\infty$, $-\infty$).

Pour les listes d'adjacence, il s'agit simplement d'adjoindre l'étiquette au
nœuds qui représentent un successeur.

## Algorithmique du graphe
(Voir le polycopié pour les implémentations)

Pour trouver les chemins les plus courts d'un sommet à tous les autres avec
utilisation d'une queue. On peut ensuite utiliser ce même processus pour le
calcul des distances ou pour le tableau de prédécesseurs dans le chemin, sans
coût en temps supplémentaire. La complexité en temps de l'algorithme est de
$O(|S| + |A|)$.

### Graphes pondérés
L'information supplémentaire des poids demande des algorithmes plus complets,
comme Dijkstra qui permet de trouve les chemins de moindre poids.

#### Algorithme de Dijkstra
L'algorithme de Dijkstra utilise une file de priorité minimale (une structure de
laquelle on peut extraire le plus petit élément). On peu
utiliser un simple tableau ($O(n)$ pour l'extraction du minimum) ou un tas
($O(\log n)$) (avec plus ou moins d'efficacité de chaque opération selon
l'implémentation : les plus simples sont la binary heap (pas mal) et la pairing
heap (très bonne)). La structure utilisée pour "la meilleure performance" sont
les tas de Fibonacci, qui peuvent être assez compliqués à implémenter mais
conviennent parfaitement car la modification de priorité peut se faire en $O(1)$
(cette structure a d'ailleurs été spécialement inventée pour Dijkstra).

L'algorithme de Dijkstra est ainsi de complexité en temps $O(|S| + |A|) \log(|S|))$
(et $O(|S| \log(|S| + |A|))$ avec un tas de Fibonacci).

#### A*
L'algorithme de Dijkstra avance le mieux possible, mais dans le noir. On peut
essayer d'obtenir plus d'information dans les situations concrètes pour guider
la recherche.

Une heuristique est ici une fonction entre deux sommets (une distance, d'une
certaine façon). On impose que $h(s,s) = 0$. On choisit souvent la distance
Euclidienne ou la distance de Manhattan dans les problèmes de recherche de
chemin. Si on utilise l'heuristique toujours nulle, on retombe sur Dijkstra.

> Une heuristique est dite admissible lorsqu'elle ne surpasse jamais la distance
> entre deux sommets. Elle est dit monotone si $\forall t \in S, \forall u \to v \in A$,
> $h(u,t) \leq \omega(u,v) + h(v,t)$. Si elle est monotone, alors elle est
> admissible (on le prouve par récurrence sur les chemins).

L'algorithme A* finit en temps polynomial (comme pour les algorithmes
précédents, le fait qu'on ne repasse jamais par les mêmes sommets assure qu'on
ne tourne pas en rond).

> Si $h$ est monotone, alors l'algorithme A* calcule la distance entre deux
> sommets et permet de reconstituer le plus court chemin.

En corollaire, cela prouve que l'algorithme de Dijkstra est correct.

#### Algorithme de Floyd-Warshall
Pour calculer les chemins entre tous les sommets, il est plus efficace
d'utiliser l'algorithme de Floyd-Warshall que de lancer $n$ fois Dijkstra.
Le principe set de calculer successivement les matrices des longueurs des
chemins les plus courts entre les sommets en utilisant seulement les sommets
$[\![0;k-1]\!]$ comme sommets intermédiaires.

On peut passer facilement d'une matrice à la suivante, en mettant dans chaque
case à chaque passage le minimum entre le chemin déjà calculé et le chemin
passant par $k$.

### Parcours en profondeur
Les parcours en profondeur sont souvent réalisés avec une pile, ou de façon
équivalent avec une fonction récursive.

Il est de complexité en temps $O(|S| + |A|)$

#### Composantes connexes d'un graphe non orienté
On lance un parcours en profondeur depuis un premier sommet, ce qui explore la
composante connexe du sommet. On recommence ensuite jusqu'à ce qu'on ait tout
listé.

#### Différents parcours du graphe
On peut parcourir le graphe en ordre préfixe, postfixe ou infixe (en fonction de
si on relève d'abord le sommet par lequel on passe, celui dans lequel on
descend, ou si on donne le sommet actuel entre plusieurs dans lesquels on
passe).

#### Détection de cycles
On fait un parcours en profondeur en colorant de trois couleurs les sommets :
pas visité, croisé (mais dans un appel pas terminé), et visité (dans un appel
terminé). Si on retombe sur un sommet gris en passant dans les graphe, un cycle
existe.

#### Tri topologique
(voir polycopié algorithme)
Le tri topologique permet d'obtenir un ordre topologique sur un graphe
acyclique, c'est à dire un ordre de sommets tel qu'on peut atteindre un sommet
par les sommes précédents. On peut trouver cet ordre en même temps qu'on
applique l'algorithme précédent.

### Calcul des composantes fortement connexes d'un graphe orienté : algorithme de Kosaraju
Pour calculer les composantes fortement connexes d'un graphe orienté, on combine
les deux algorithmes précédents. On utilise d'abord un parcours en profondeur sur le
graphe et on obtient l'ordre postfixe, puis on utilise le graphe transposé (le
graphe avec les arêtes à l'envers), sur lequel on lance les parcours en
profondeur dans l'ordre postfixe obtenu comme l'algorithme de composantes
connexes vu précédemment.

Le graphe des CFC de $G$ est le graphe ayant pour sommets les composantes fortement connexes
et ayant pour arêtes les arêtes existant entre ces composantes. C'est donc un
graphe acyclique.

Cet algorithme s'applique en temps $O(|S| + |A|)$.

### Arbre couvrant de poids minimum
#### Structure union-find
On cherche à pouvoir efficacement voir si deux sommets sont dans une même
classe, et à pouvoir fusionner deux classes. Pour ceci, on utilise un
union-find.

On utilise des arbres et forêts. Lorsqu'on rassemble des classes, on accroche
une des racines à l'autre. En conservant la hauteur avec chaque racine, on peut
grandement améliorer les opérations en accrochant toujours l'arbre le moins haut
au plus haut. De plus, on ajoute la "compression de chemin" : à chaque find, on
obtient la racine de l'arbre, et on accroche du même coup tous les nœuds
rencontrés comme enfants directs de la racine trouvée.

On peut atteindre une complexité amortie pour les opérations d'union et find
de $O(d(n))$, avec $d(n)$ la fonction réciproque de $A(n,n)$, avec $A$ la
fonction d'Ackermann (la preuve est admise dans le programme).

#### Algorithme de Kruskal
On s'intéresse ici à des graphes pondérés acyclique non orientés et connexes.

> Un arbre couvrant d'un graphe est un sous-ensemble des arcs du graphe tels que
> ce sous-ensemble soit un arbre et aie tout sommet dans au moins l'une des
> extrémités de ses arcs.

Dans un graphe pondéré, on s'intéresse à la recherche de l'arbre couvrant
minimal, celui dont la somme des poids des arcs est minimale. L'algorithme de
Kruskal permet de trouver cet arbre, en une complexité temporelle $O(|A| \log(|A|))$,
en utilisant un union-find des sommets, et en déroulant une file de priorité
minimale avec tous les arcs dedans, on met dans la même classe lorsqu'on peut
avec le nouvel arc jusqu'à ce que l'arbre contienne tous les sommets.
