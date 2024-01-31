# Espaces préhilbertiens, hermitiens et produits scalaires
## Espaces préhilbertiens
### Définition
> Soit $E$ un espace vectoriel de dimension quelconque, un produit scalaire est
> une application $E \times E \to \mathbb{R}$ symétrique, bilinéaire, et définie
> positive.

> Un produit hermitien est un produit $E \times E \to \mathbb{C}$, qui est
> sesquilinéaire en le premier argument ($(\lambda x + x'|y) = \overline{\lambda}(x | y) + (x' | y)$),
> linéaire en le deuxième, hermitien ($(x|y) = \overline{(y|x)}$) et défini
> positif.

Les produit canonique sur $\mathbb{C}^n$ est $(X|Y) = X^{\ast} Y$, avec $X^{\ast}$
l'adjoint de $X$, c'est à dire $X^{\ast} = \overline{X}^{\top}$.

### Norme associée
On peut toujours associer une norme, appelée norme euclidienne, à un espace
préhilbertien à partir du produit scalaire : $\|x\| = (x|x)$. Les axiomes de la
norme tiennent alors, et pour les normes dérivées d'un produit scalaire, les
identités de polarisation permettent d'obtenir à nouveau le produit scalaire :
- $\| x + y \|^2 = \| x \|^2 + 2 (x|y) + \| y \|^2$
- $\| x + y \|^2 - \| x - y \|^2 = 4 (x|y)$
- $\| x + y \|^2 - \| x \|^2 - \| y \|^2 = 2 (x|y)$
- (Égalité du parallélogramme) : $\| x + y \|^2 + \| x - y \|^2 = 2 \| x \|^2 + 2 \| y \|^2$,
  la norme est Euclidienne si et seulement si cette identité est respectée

On peut d'ailleurs obtenir le théorème de Pythagore ou le théorème d'Al-Kashi
avec ces formules.

### Orthogonalité
Deux vecteurs sont orthogonaux si leur produit scalaire est nul. Une base est
appelée normée si la norme euclidienne induite par le produit scalaire de chaque
vecteur est de $1$, et est orthonormée si tous ses vecteurs sont mutuellement
orthogonaux.

On prouve l'existence d'une base orthonormée de façon constructive par
l'algorithme de Gram-Schmidt, par récurrence sur le cardinal de la base.
Après avoir fabriqué une base orthonormée d'un sous-espace, on peut aisément
construire un projecteur orthogonal dessus.

### Matrice d'un produit scalaire
On note ici $A = ((e_i | e_j))_{i,j}$. Le produit scalaire $(x | y)$
est alors égal à $X^{\top} A Y$. Une matrice représente donc un produit scalaire
si elle est symétrique, et "définie positive" (on va chercher à caractériser les
produits scalaires par leurs matrices).

Soit $u$ un endomorphisme de $E$, et $A = \text{Mat}_\mathcal{B} u$ avec
$\mathcal{B}$ une base orthonormée, $(u(x) | y) = X^{\top} A^{\top} Y$
$(x | )$ avec $z = v(y)$, où $\text{Mat}_\mathcal{B} v = A^{\top}$.
On définit cette application linéaire comme l'adjoint de $u$, noté $u^{\top}$.
On pourra remarquer que $\text{Mat}_\mathcal{B} u^{\top} = (\text{Mat}_\mathcal{B})^{\top}$.
L'adjoint se généralise aussi au produits hermitiens, qu'on note en général
$u^{\ast}$.

## Adjonction
### Définition de l'adjoint 
On définit l'adjoint quasiment uniquement en dimension finie, sans quoi on se
heurte à des difficultés majeures de topologie.

Soit $\mathcal{B}$ une base orthonormée, et $M = \text{Mat}_\mathcal{B} u$, on
définit $u^{\top}$ par l'application associée dans $\mathcal{B}$ à $M^{\top}$.
Il reste cependant pour cette définition à prouver l'indépendance du résultat
du choix de la base orthonormée, ce qui se trouve normalement par le fait que
les matrices de passage sont orthogonales et donc des isométries, et qu'elles
sont donc telles que $P^{-1} = P^{\top}$.

Une autre définition est l'identité $(u(x) | y) = (x | u^{\top}(y))$, et on peut
prouver l'équivalence en décomposant les produits matriciels.

Encore autrement, en exploitant l'isomorphisme canonique entre un espace de
dimension finie et son dual, pour un $u \in \mathcal{L}(E)$ fixe, on définit
l'adjoint par l'équation $(u( \cdot ) | x) \in E^{\ast} = (y | \cdot )$ pour un
$y$ unique, donnant par extensionnalité $u^{\top}(x) = y$. On peut dans tous les
cas voir par linéarité du produit scalaire que ce $u^{\top}$ est linéaire et
déterminé par ses valeurs sur une base.

### Propriétés
> L'adjonction est une application linéaire involutive, avec
> $(uv)^{\top} = v^{\top} u^{\top}$, et la matrice de l'adjoint est la transposée
> de la matrice de $u$ quand la base est orthonormée.

### Adjonction hermitienne
Les propriétés et définitions sont les mêmes pour l'adjonction hermitienne
$u^{\ast}$, à la différence que $u \mapsto u^{\ast}$ est semilinéaire :
$(\lambda u)^{\ast} = \overline{\lambda} u^{\ast}$.

### Endomorphismes particuliers
> Pour $x,y \in E$, On dit qu'un endomorphisme $u$ est :
> - symétrique si $(u(x) | y) = (x | u(y))$, donc $u^{\ast} = u$
> - antisymétrique si $(u(x) | y) = - (x | u(y))$, donc $u^{\ast} = - u$
> - orthogonal si $(u(x) | u(x)) = (x | y)$ (isométries), donc $u^{\ast} = u^{-1}$
> - normal si $u u^{\ast} = u^{\ast} u$

Pour $E$ euclidien, $u$ est symétrique si et seulement si $u$ est diagonal en
base orthonormée. Pour $E$ hermitien, $u$ est diagonal en base orthonormée si et
seulement si $u$ est normal.

En effet, pour $u$ normal, c'est une symétrique si elle est "diagonalisable en
base orthonormée" avec des valeurs propres réelles, antisymétrique pour des
valeurs propres imaginaires, et orthogonal pour des valeurs propres de norme $1$.

Cette dernière remarque entraîne qu'un matrice antisymétrique réelle se réécrit
en base orthonormée comme une diagonale de matrices de la forme
$\begin{pmatrix} 0 & - \alpha \\ \alpha & 0 \end{pmatrix}$.

### Projecteurs orthogonaux
> Soit $p$ un projecteur, $p$ est dit orthogonal si pour tous $x,y \in E$,
> $(p(x) | y) = (x | p(y))$, si et seulement si $p$ est symétrique.

Ne pas confondre les transformations orthogonales et les projecteurs
orthogonaux, seule l'identité fait les deux.

$p$ est un projecteur orthogonal si et seulement si son image et son noyau sont orthogonaux.
Une autre caractérisation à prouver soi-même est que $p$ est orthogonal si et seulement si
sa norme d'opérateur pour la norme Euclidienne est inférieure ou égale à $1$,
si et seulement si $\| p(x) \| \leq \| x \|$ pour tout $x$.

### Isométries
> Les propositions suivantes sont équivalentes pour $u \in \mathcal{L}(E)$ :
> - $u$ conserve la norme euclidienne
> - $u$ conserve le produit scalaire
> - L'image d'une base orthonormée est une base orthonormée
> - L'image de toute base orthonormée est une base orthonormée
> - $u^{\top} = u^{-1}$
>
> Pour un tel $u$, on dit que $u \in \mathcal{O}(E)$ est une isométrie, ou fait
> partie du groupe orthogonal de $E$.

$\mathcal{O}(E)$ et $S \mathcal{O}(E)$ (le groupe spécial orthogonal, dans
lequel les matrices sont de déterminant $1$) sont des groupes compacts.

Si $F$ est un sous-espace stable par une isométrie, $F^{\top}$
est stable par cette isométrie.

### Théorème spectral : réduction des matrices symétriques
On cherche à prouver que $u$ est diagonalisable en base orthonormée,
si et seulement si $u$ est symétrique. On le prouve par la série de lemmes
suivants, dont on peut trouver la preuve détaillée facilement.

- Si $u$ est symétrique, et que $F$ est stable par $u$, $F^{\top}$ est stable
  par $u$, et $u\restriction_{F}$ est symétrique (en utilisant la définition par
  le produit scalaire de la symétrie (qu'un endomorphisme symétrique est son
  propre transposé)).
- Les valeurs propres d'un endomorphisme symétrique sont réelles, ce qu'on
  montre en passant au produit hermitien du produit scalaire sur des matrices
  complexes, et on trouve alors pour les vecteurs propres des valeurs propres
  (encore une fois avec la caractérisation au produit scalaire).
- On fait la preuve finale par récurrence sur la dimension de l'espace, qu'on
  sépare ensuite en $F$ l'espace orthogonal à tous les espaces propres et
  $F^{\top}$, sur lesquels $u$ est diagonalisable en BON, ce qui contredit la
  définition de $F$ et permet de diagonaliser sur tout l'espace.

Les matrices symétriques peuvent devenir un produit scalaire sont les matrices
symétriques définies positives $S^{++}$, pour lesquelles $(u(x)|x) > 0$ pour
tout $x$ non nul. On définit les matrices symétrique positives $S^+$ comme
celles pour lesquelles $(u(x)|x) \geq 0$ pour tout $x$.

Une matrice est symétrique (définie) positive si et seulement si
son spectre est réel (strictement) positif.

On peut poser certaines questions en notant $u \geq v$ quand
$u - v \in S^+$, et en étudiant des suites ou les particularités de cet ordre.

Pour $u$ symétrique, $\text{Ker} u = (\text{Im} u)^{\top}$.

### Rayon spectral
Pour $u$ une matrice symétrique, on définit $\rho(u) = \text{sup} Sp(u)$. On
peut remarquer que cette valeur est celle de la norme triple de $u$ associée à
la norme euclidienne. On va pouvoir, plus précisément, déterminer que la norme
triple d'un endomorphisme quelconque $u$ est de $\sqrt{\rho(u^{\top} u)}$.

On retiendra l'identité $\| u(x) \|^2 = (u(x) | u(x)) = (u^{\top} u(x) | x)$.
