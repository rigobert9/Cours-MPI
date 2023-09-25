# Réduction d'endomorphismes
## Généralités
### Valeurs propres, vecteurs propres
Soit $u \in \mathcal{L}(E)$, $x \neq 0$ est un vecteur propre
associé à la valeur propre $\lambda$ si $u(x) = \lambda x$.
On dit que $\lambda$ est une valeur propre si il existe un vecteur propre
associé.

Par exemple, pour l'endomorphisme de shift des suites complexes, toutes les
valeurs $\lambda \in \mathbb{C}^{\ast}$ sont propres, pour les vecteurs des
suites géométriques.

### Sous-espace vectoriel propre
Le sous-espace propre d'un endomorphisme pour une valeur propre est l'espace
$\text{Ker}(u - \lambda \text{id}) = E_\lambda(u) = \{x \mid u(x) = \lambda x\}$,
c'est-à-dire l'ensemble des vecteurs propres associés à $\lambda$
auquel on ajoute $0$. Il existe des vecteurs propres associés à $\lambda$
si et seulement si l'espace propre est non nul.
Comme c'est un $\text{Ker}$, il s'agit d'un SEV.

Le spectre de $u$ $\text{Sp}(u)$ correspond à l'ensemble des valeurs propres de
$u$.

### Polynôme caractéristique
On écrit $P_u(X) = \text{det}(X \text{id} - u)$ (on peut aussi travailler avec
l'équivalent matriciel).
$P_u(X)$ est un polynôme unitaire de degré $n$, et $P_u(X) = X^n - \text{Tr}(u) X^{n-1} + ? + (-1)^n \text{det}(u)$.

En effet, $P_A(X) = \sum\limits_{\sigma \in \mathfrak{S_n}} \varepsilon(\sigma) (X I_n - A)_{\sigma(1), 1} \times \ldots \times (X I_n - A)_{\sigma(n), n}$.
Le contenu de la formule est un polynôme de degré $\leq n-2$ en $X$ si $\sigma \neq \text{id}$ (car au
moins deux éléments sont dérangés) pour les éléments qui ne sont pas $X^n$ et $- \text{Tr}(u) X^{n-1}$.
Ainsi, on trouve aussi que le cardinal du spectre de $u$ est inférieur ou égal
à la dimension de l'espace vectoriel.

### Première CNS de diagonalisabilité
> $u$ est diagonalisable si et seulement si il existe $\mathcal{B}$ telle que $\text{Mat}_\mathcal{B}(u)$
> est diagonale.

Une matrice est diagonalisable si et seulement si elle est semblable à une
matrice diagonale.

Si $\text{Mat}_\mathcal{B}(u)$ est diagonale de coefficients $(\lambda_i)$, les
valeurs propres sont les $\lambda_i$ (en prenant le polynôme caractéristique).

Les espaces propres ont pour intersection $\{0\}$. En effet, en prenant les vecteurs
propres, on obtient la condition de liaison $0 = \sum\limits_{i = 1}^{n} \lambda_i^k x_i$
$\forall k \geq 0$, par linéarité, c'est le cas pour tout polynôme, donc on
obtient par interpolation de Lagrange un polynôme tel que $P(\lambda_{i_0}) = 1$
et $0$ pour les autres, permettant de prouver que l'une des valeurs est nulle,
amenant une contradiction.

Ainsi, les vecteurs propres de ces valeurs propres forment une famille libre.
On retrouve l'assertion sur le cardinal du spectre.

$u$ est diagonalisable si et seulement si ses espaces propres sont en somme
directe donnant $E$ (on peut former une base pratique qui satisfait les
contraintes sur ces espaces).

### Autre CNS de diagonalisabilité
> $u$ est diagonalisable si et seulement si $P_u$ est scindé, c'est à dire que le
> polynôme a autant de racines que de degré.

On peut remarquer que la dimension de chaque espace propre est alors égal à
multiplicité de chaque racine.

Cette CNS se vérifie en pratique (?).
