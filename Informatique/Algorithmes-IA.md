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
