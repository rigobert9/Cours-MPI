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
