# Algorithmes pour l'intelligence artificielle
Intelligence artificielle est un terme décrivant un très large panel de
techniques très différentes les unes des autres, pour résoudre des problèmes qui
semblent difficiles pour une machine et plus facile pour un humain. Cela
implique souvent qu'on maîtrise et décrit mal la stratégie et les résolutions de
ces problèmes, empêchant la création d'un algorithme de résolution stricte du
problème.

Nous allons d'abord nous pencher sur les techniques pour résoudre des jeux à deux
joueurs, mais nous parlerons aussi d'autres techniques.

## Théorie des jeux
### Définitions
Dans cette partie, on s'intéresse à des jeux à deux joueurs au tour par tour, où
un joueur ne peut pas joueur deux fois d'affilée (coups asynchrones), sans
hasard (déterministe), à un information complète et parfaite, à coups en nombre
fini, et à somme nulle.

On appelle en général les joueurs Alice et Bob. On peut modéliser de tels jeux
comme des graphes bipartis : on parle de jeux d'accessibilité à deux joueurs.
Dans le graphe, un sommet correspond à un état du jeu et un arc correspond à un
coup possible pour l'un des joueurs. Comme le jeu est à nombre de coups finis,
ce graphe est acyclique. Un sommet sans arc sortant est un état terminal du jeu.
Une partie est un chemin depuis un certain état appelé initial jusqu'à un état
terminal.

On peut par exemple étudier le jeu de Nim qui se prête bien à une représentation
du graphe sur papier.

> Soit $X$ un des joueurs $A$ ou $B$, et $S_X^{> 0}$ l'ensemble des sommets non
> terminaux de $X$, une stratégie pour $X$ est une fonction $f: S^{> 0}_X \to S$
> telle que $\forall s \in S^{> 0}_X$, $s \to f(s)$ (on retourne un coup valide).
> La stratégie $f$ ne prenant ici que $s$ en entrée, on parle du cas particulier
> de stratégie sans mémoire.

Une partie respecte une stratégie si chaque sommet est le suivant du dernier par
la stratégie. Une stratégie est gagnante si quelque soient les coups joués par
l'adversaire, toute partie respectant $f$ pour $X$ conduit à la victoire de $X$.

Un sommet $s \in S$ est appelé position gagnante pour $X$ s'il existe une
stratégie gagnante pour $X$ depuis $s$. Dans un jeu d'accessibilité à $2$
joueurs, résoudre le jeu consiste à calculer les positions gagnantes de chacun
des joueurs, ainsi qu'une stratégie gagnante pour chacun (ou pour un seul le cas
échéant). Par symétrie (quand c'est possible), on s'intéresse toujours
uniquement aux positions d'Alice.

### Attracteurs
> Les attracteurs sont l'union d'une suite de sous-ensemble de $S$ tels que $\mathcal{A}_0 = V_A$
> (les sommets où Alice gagne), et $\forall j \in \mathbb{N}, \mathcal{A}_{j+1} = \mathcal{A}_j$
> $ \cup \{s \in S_A^{> 0} \mid \exists s' \in \mathcal{A}_j, s \to s'\}$
> $ \cup \{s \in S_B^{> 0} \mid \forall s' \in S, s \to s' \Rightarrow s' \in \mathcal{A}_j\}$.

Les membres de la suite des attracteurs incorporent ainsi à chaque fois les
coups depuis lesquels Alice peut aller dans l'attracteur précédent, et les
sommets de Bob qui mènent forcément dans un attracteur.

> Alice possède une stratégie gagnante pour tout sommet de $\mathcal{A}$, et
> uniquement ceux-là.

On le démontre par récurrence forte sur les ordres du premier attracteur
contenant chaque sommet dans l'attracteur, et on montre que ce sommet est une
position gagnante.

Si le jeu ne peut pas finir en match nul, les attracteurs pour Alice sont le
complémentaire des attracteurs pour Bob (dans le cas fini, sinon avec l'axiome
de déterminance (Axiom of determinacy)). Pour calculer les attracteurs, il
suffit d'effectuer un parcours dans le graphe transposé (remontant ainsi les
coups à l'envers). L'algorithme est donc de complexité $O(|S| + |A|)$.

Tout ceci fonctionne très bien dans le cas de jeux à coups possibles finis et
assez petits : pour les échecs, le Go, les dames, des techniques différentes
sont nécessaires pour pouvoir explorer le graphe qui est beaucoup trop grand. On
appelle ces jeux "jeux univers" dans les cas où il est théoriquement impossible
d'avoir assez de mémoire dans l'univers (explosion combinatoire des
possibilités). De façon générale, beaucoup de jeux sont trop difficiles à
explorer entièrement et donc à résoudre de cette façon.

### Algorithme minimax
Lorsque les coups du jeu sont trop nombreux, on fait des approximations en
suivant une heuristique en plus de la recherche en profondeur de coups gagnants.
On introduit un gain (ou score), une heuristique qui donne des points infinis
pour une victoire, - l'infini pour une défaite, 0 pour un match nul, et des
points calculés selon une certaine fonction pour les autres positions.
Celle-ci est plus grande plus la partie semble favorable au premier joueur
(Max), et plus petite plus la partie semble favorable au second (Min).

On définit une extension de la fonction de score, appelée eval, qui renvoie le
score maximal obtenu dans les successeurs de cet état (ou minimum pour un sommet ou Min
joue). Si l'arbre est assez petit, on peut utiliser eval récursivement sur tous les noeuds
et retrouver les attracteurs.

Si l'arbre est trop grand, on se limite en revanche à descendre à une profondeur
fixée. Cela correspond à l'algorithme min-max, qui prend le meilleur score à
chaque fois.

Aux échecs, on peut par exemple prendre pour score une variation des coûts de
matériel (9 pour la dame, 1 pour le pion ...). Améliorer une telle heuristique
sans faire de théorie sur le jeu et sans comprendre comment elle est calculée en
la créant à partir de données d'entraînement à la place a mené à la recherche de
l'apprentissage profond et des réseaux de neurones.

### Élagage $\alpha$-$\beta$
L'algorithme précédent n'est pas encore utilisable pour des jeux comme les
échecs et le Go, sauf avec une profondeur maximale très faible. On ajoute
l'optimisation du $\alpha$-$\beta$ pruning. Pour cela, on ajoute les deux
arguments $\alpha$ et $\beta$, initialisés respectivement à $-\infty$ et $+\infty$;
elles seront ensuite raffinées et passées à travers les appels récursifs, et
être utilisées pour éviter de faire certains appels (on élimine des
sous-arbres).

Si le nœud est un tour de Max, on introduit un minorant $m$ de `eval(n)` : on
initialise $m = -\infty$, puis on le fait prendre la valeur de `eval` à chaque
test, et si $m$ devient supérieur à $\beta$, on fait une coupure $\beta$ (on se
limite à cette valeur minimale intéressante). Sinon, si $m > \alpha$, on met à jour $\alpha$ à
la valeur $m$ (pour les prochains appels récursifs). De même, sur un tour de Min, on fait l'inverse
(coupure $\beta$).

Ainsi, en avançant, la fenêtre $\alpha$-$\beta$ devient de plus en plus étroite,
et tout particulièrement s'il analyse à fond un bon coup dès le début.

## Algorithmes d'apprentissage
Bien qu'il fût inventé dès les années 50 comme l'une des premières techniques
d'apprentissage machine, le réseau de neurone n'a pu être testé que sur des
machines très récentes et des bases de données très grandes, et fait ses preuve
depuis une dizaine d'années. Il permet d'écrire un programme simple dont
l'objectif est de s'entraîner sur des exemples d'un problème (en modifiant des
valeurs de décision internes lorsque celles-ci sont infirmées ou confirmées)
pour résoudre un problème pour lequel on ne trouve pas d'algorithme. On peut
modéliser l'entraînement de ces neurones par une descente de gradian.

On distingue deux types d'algorithmes d'apprentissage :
- L'apprentissage supervisé, quand on a beaucoup d'exemples et qu'on essaie
  d'entraîner la machine a réussir des cas pour lesquels on connaît la réponse.
- L'apprentissage non supervisé, où on entraîne la machine sur des exemples dont
  on ne connaît pas la réponse (et on espère que ça ira)

Dans la suite, une donnée est un élément de $\mathbb{R}^{d}$, avec $d$ une
dimension fixée. On cherche alors à classifier ces données sur $p$ catégories,
numérotées de $0$ à $p - 1$.

### Apprentissage supervisé
Dans cette partie, on suppose disposer d'un ensemble d'entraînement $E$ de
données d'entraînement de la forme $(x,c)$ avec $x \in \mathbb{R}^{d}$ et
$c \in [\![0;p-1]\!]$. On cherche alors à trouver la catégorie de laquelle fait
partie une donnée qui n'était pas dans $E$.

#### Algorithme des $k$ plus proches voisins
On fixe une distance (cet algorithme implique donc qu'on y arrive) $\delta$ sur
$\mathbb{R}^d$, et un entire $k \in \mathbb{N}^{\ast}$. On applique les $k$-PPV :
on calcule la liste $L$ des catégories des $k$ points les plus proches de notre
nouveau point $y$, et on identifie la catégorie majoritaire (système de vote à
la majorité des voisins).

L'approche naïve correspondrait au tri de tous les points en fonction de la
proximité à $y$ ($O(n \log n)$), mais on préfèrera utiliser une file de priorité max qui expulse
les éléments quand ils sont plus petits que $k$ autres ($O(n \log k)$). Comme le
plus souvent $n \gg k$, et dans tous les cas $n \geq k$, le second algorithme
est plus efficace.

Une autre technique est encore possible : les arbres $k$-dimensionnels, qu'on
verra plus loin.

Il reste encore un problème, celui de choix de $k$. On utilise une "matrice de
confusion", qui est la matrice $C$ de taille $p$ fois $p$ telle que
$C_{i,j}$ est le nombre d'éléments des données de test de catégorie $i$ et
classifié $j$ par l'algorithme. Ainsi, les bonnes réponses sont répertoriées sur
la diagonale (et les autres valeurs montrent des mauvais classifications). On
cherche donc à maximiser la trace de cette matrice, ce qui pourrait être
l'objectif d'un rapide script d'entraînement ou d'une autre IA.

### Arbres $k$-dimensionnels
Attention, ici $k$ fait simplement référence à la dimension de l'espace où se
trouvent les données qu'on stock dans l'arbre. C'est simplement l'appellation
standard de la structure.

> Un arbre $k$-dimensionnel est un arbre binaire stockant des éléments de $\mathbb{R}^k$
> en comparant à profondeur $i$ l'étiquette de la racine avec les autres éléments selon la $i [k]$-ème composante.

Si on construit cet arbre de façon équilibrée et qu'on stocke tous les éléments
de $E$ dans le problème des $k$-PPV, on va pouvoir grandement améliorer la
recherche. Pour cela, on cherche les éléments proches de $y$ en feignant de
l'insérer dans l'arbre, puis on garde en mémoire en remontant la plus grande
distance à $y$ des voisins pour l'instant les plus proches. Si on croise en
remontant un nœud tel que la $i [k]$-ème composant est strictement inférieure à
cette valeur, il faut considérer ce nœud et l'autre sous-arbre (sinon, pas
besoin).
