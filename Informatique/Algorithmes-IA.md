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
