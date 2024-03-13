# Équations différentielles linéaires
## Syntaxe
> Un système différentiel d'ordre $1$ homogène est de la forme $X'(t) = A(t) X(t)$
> avec $A : I \to \mathcal{M}_n(\mathbb{R}) \in \mathcal{C}^0$ et $X : I \to \mathbb{R}^n \in \mathcal{C}^1$.
> Un système différentiel d'ordre $1$ est de la forme $X'(t) = A(t) X(t) + B(t)$
> avec $B : I \to \mathcal{M}_n(\mathbb{R}) \in \mathcal{C}^0$.

On peut remarquer qu'en produisant les bons vecteurs, on peut facilement ramener
un système différentiel de tout order à un système différentiel d'ordre $1$.

Une application $X$ est solution d'un système différentiel si et seulement si
elle est solution du système intégral, c'est à dire respecte l'équation
$X(t) = x_0 \int\limits_{x_0}^{t} A(s) X(s) + B(s) ds$.

## Théorème de Cauchy-Lipschitz
### Système différentiel homogène
Avec le système différentiel $X'(t) = A(t) X(t)$ avec $A \in \mathcal{C}^0(I \to \mathcal{L}(E))$,
l'ensemble des solutions est un espace vectoriel isomorphe à $E$. Plus
exactement, pour chaque solution correspond bijectivement la valeur de la solution en un certain $t_0$ fixe.
Ainsi, pour ce systèmes, auquel on ajoute la contrainte $X(t_0) = x_0$ il existe
une solution unique.

### Système différentiels non homogènes
Pour un système différentiel non homogène, l'espace des solutions est un espace
affine dirigé par l'espace vectoriel des solutions de l'équation homogène,
auquel on ajoute toute solution particulière.

### Système différentiels non linéaires
> Un problème de Cauchy non linéaire est, pour $f : I \times U \to E$
> avec $U \subset E$ un ouvert, et qui soit de classe $\mathcal{C}^1$,
> est un système $\left\{\begin{matrix} x'(t) = f(t,x(t)) \\ x(t_0) = x_0 \end{matrix}\right.$.

Pour une équation différentielle non linéaire, on a aussi un théorème de
Cauchy-Lipschitz qui garantit l'existence sur un intervalle ouvert $J \subset I$
(existence locale), et l'unicité sur un intervalle commun (des solutions, l'une
sur $J_1$ et l'autre sur $J2$, coïncident sur $J_1 \cap J_2$), d'une solution
maximale, c'est-à-dire d'une solution sur un intervalle ouvert $J$ qui contient
tous les intervalles avec des solutions possibles et le point $x(t_0)$.

Certaines équations admettent une solution qui doit soit diverger en un point
fini, soit être définie jusqu'à l'infini : c'est une explosion en temps fini. Il
s'agit alors de prouver que si la limite en un point fini était finie, on
pourrait étendre la solution, contredisant la maximalité de la solution.

### Système différentiel d'ordre 2
Un problème de Cauchy d'ordre 2 est défini identiquement, mais doit contenir
aussi la valeur de $x'$ en $t_0$ (et pas en un autre point). Il jouit du même
théorème de Cauchy-Lipschitz.

## Wronskien
Le wronskien pour une équation différentielle homogène d'ordre $2$
$x'' + a x' + bx = 0$  correspond au
déterminant de $\begin{pmatrix} y_1 & y_2 \\ y'_1 & y'_2 \end{pmatrix}$, avec
$y_1$ et $y_2$ des solutions.

On obtient par le calcul que $w' = - a w$, donnant la solution
$w(t) = w(t_0) \exp(- \int\limits_{t_0}^{t} -a)$, qui est nulle ou bien ne
s'annule jamais.

On peut généraliser le wronskien en dimension $n$ avec la même forme,
et on a l'équation sur le wronskien $w'(t) = Tr(u(t)) w(t)$.
On obtient ainsi que si le wronskien est nul en $t_0$, les conditions initiales
sur toutes les solutions sont liées.
