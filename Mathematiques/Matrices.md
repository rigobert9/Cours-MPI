# Matrices
## Structure de $\mathcal{M}_{n,m}(\mathbb{K})$
Les éléments de $\mathcal{M}_{n,m}$ sont des collections de $n \times m$
coefficients. On note alors $A = (a_{i,j})_{i \in [\![1;n]\!], j \in [\![1;m]\!]}$,
et $\mathcal{L}_i = (a_{i,j})_j$, $\mathcal{C}_j = (a_{i,j})_j$.

Il s'agit d'un espace vectoriel (avec pour addition l'addition terme à terme et
pour multiplication extérieure celle terme à terme). On appelle sa base
canonique $(E_{i,j)})_{i,j}$.

Le produit de matrices $A \times B = C$ est définie comme
$C_{i,k} = \sum\limits_{j = 0}^{m} a_{i,j} b_{j,k}$. Ce produit est bilinéaire,
associatif, et est bien compatible avec la multiplication externe, faisant de
$\mathcal{M}_{n} = \mathcal{M}_{n,n}$ une algèbre (la multiplication n'est pas
définie pour toutes les matrices si elles ne sont pas carrées de même taille).
On peut le redéfinir entièrement par bilinéarité par $E_{i,j} \times E_{k,l} = \delta_{j,k} E_{i,l}$.

On définit aussi la transposée de $A$ comme ${}^t \! A$ telle que $({}^t \!
A)_{i,j} = A_{j,i}$, et sur les matrices carrées l'opération trace $Tr$, somme
des coefficients diagonaux. La transposée est nilpotente (pour la composition),
et transforme la i-ème ligne en i-ème colonne et inversement. On obtient de plus
${}^t \! (AB) = {}^t \! B {}^t \! A$. La trace est linéaire et commutative.

On identifie $\mathbb{K}^n$ à $\mathcal{M}_{n-1, 1}(\mathbb{K})$.
On peut associer à $A \in \mathcal{M}(n,m)$ l'application linéaire canoniquement
associée $\begin{aligned} u_A: \mathbb{K}^m &\to \mathbb{K}^n \\ X &\mapsto AX .\end{aligned}$.
On peut prouver la linéarité de l'opérateur par bilinéarité du produit
matriciel.

## Applications linéaires et matrices
Soit $u \in \mathcal{L}(E,F)$, $\mathcal{B}$ une base de $E$ et $\mathcal{C}$
une base de $F$, on a $\text{Mat}_{\mathcal{B},\mathcal{C}}(u)$
la matrice canoniquement associée, qui est celle des $(a_{j,i})_{j,i}$
tels que $u(e_i) = \sum\limits_{j} a_{j,i} f_j$.
$\text{Mat}$ est un foncteur contravariant : on peut voir que la composition des
matrices pour $v \circ u$ est alors $\text{Mat}_{\mathcal{B},\mathcal{D}}(v \circ u)$
$= \text{Mat}_{\mathcal{C},\mathcal{D}}(v) \times \text{Mat}_{\mathcal{B},\mathcal{C}}(u)$.

La matrice de changement de base $P_{\mathcal{B},\mathcal{B'}}$ correspond à
celle de $\text{Mat}_{\mathcal{B'},\mathcal{B}}(id)$.

## Matrice par blocs
En séparant une matrice par blocs, on peut effectuer le produit matriciel par
ces blocs sous condition de cohérence entre la taille des blocs qui sont
multipliés.
