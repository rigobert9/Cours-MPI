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

On utilise cette CNS en pratique, en obtenant les coefficients du polynôme
caractéristique et en testant la correspondance entre la multiplicité des
racines et la dimension des espaces propres.

## Action de $\mathbb{K}[X]$
On définit facilement l'évaluation de polynômes sur des endomorphismes (avec la
puissance appliquée sur la composition).
L'application associant à un polynôme son action sur un certain $u$ est un morphisme d'algèbres (en les polynômes).

### Polynôme minimal
L'ensemble des polynômes annulant $u$ est un idéal et donc est engendré par un
unique polynôme unitaire noté $\pi_u$ (qui divise alors tous les polynômes
annulateurs). L'espace vectoriel $\mathbb{K}[u]$ est alors de dimension du degré
de $\pi_u$.

### Lemme des noyaux/Théorème de décomposition des noyaux
> Soit $P$ et $Q$ des polynômes premiers entre eux, $\text{Ker}(PQ)(u) = \text{Ker}(P(u)) \oplus \text{Ker}(Q(u))$.

__Preuve :__ Puisque $P$ et $Q$ sont premiers entre eux, on a une relation de
Bézout entre eux, ce qui signifie que $x = (U(u) P(u))(x) + (V(u) Q(u))(x)$.
Si $x \in \text{Ker}(P(u)) \cap \text{Ker}(Q(u))$, alors $x$ est donc $0$.
Soit $x_1 = (U(u) P(u))(x)$ et $x_2 = (V(u) Q(u))(x)$, en retrouve l'inclusion
$\subset$, et on fait facilement l'autre inclusion.

Le théorème se généralise facilement à une famille plus grande de polynômes
premiers entre eux.

### Stabilité
> Si $uv = vu$, alors $\text{Ker}(u)$ et $\text{Im}(u)$ sont stables par $v$.

De même, les espaces propres et les $\text{Ker}$ des polynômes
en $u$ sont stables.

### Diagonalité
> $u$ est diagonal si et seulement si $\pi_u$ est un polynôme scindé à racine
> simples si et seulement si $u$ admet un polynôme annulateur à racines simples.

En effet on a ainsi l'espace vectoriel qui est la somme directe des espaces
propres de l'endomorphisme par le lemme des noyaux.

> Les racines racines du polynôme minimal sont exactement les valeurs propres.

__Preuve :__ On a facilement le fait que les valeurs propres sont annulées par
le polynôme minimal. Dans l'autre sens, si $\lambda$ est racine de $\pi_u$,
on montre que $\text{Ker}(u - \lambda \text{id}) \neq \{0\}$. Comme $\pi_u(\lambda) = 0$,
il est égal à $(X - \lambda) Q$, et comme $\pi_u$ est minimal, il ne divise pas
$Q$ et donc $Q$ ne s'annule pas en $\lambda$, donc $u - \lambda \text{id}$ n'est
pas inversible.

Puisque le polynôme caractéristique s'annule en l'endomorphisme, il est
divisible par le polynôme minimal. Leurs racine étant les mêmes, la multiplicité
est forcément plus grande ou égale dans le polynôme caractéristique.

Attention en manipulant des complexes pour les espaces sur des sous-corps de $u$
: il n'est pas possible de parler de vecteurs propres complexes puisque $\mathbb{C}$
n'agit pas sur l'espace.

> $u$ est diagonalisable si et seulement si le caractéristique est scindé et que
> les espaces propres sont de dimension de la multiplicité de leur valeur propre
> comme racine.

## Trigonalisation
Une matrice $M$ est trigonalisable s'il existe une matrice $P \in GL_n(\mathbb{K})$
telle que $P M P^{-1}$ soit triangulaire. On le dit de la même façon pour un
endomorphisme lorsqu'il est triangulaire dans une base.

Soit un drapeau (une suite croissante pour l'inclusion de SEV) tel que la
dimension du $i$-ème élément soit $i$, on définit un drapeau associé à une base
comme la suite des espaces vectoriels générés par les $i$ premiers éléments de
la base.

> $Mat_{\mathcal{B}} u$ est triangulaire supérieure si et seulement si le
> drapeau associé à $\mathcal{B}$ est stable par $u$.

Un endomorphisme est trigonalisable si et seulement si $\pi_u$ est scindé si et
seulement si $\Chi_u$ est scindé. La seule existence d'un annulateur scindé
suffit.

### Nilpotents
> Un endomorphisme nilpotent d'indice $n$ est un endomorphisme tel que $u^{n-1} \neq 0$
> et $u^n = 0$.

$\lambda id - u$ est toujours inversible si $\lambda \neq 0$ (car $\pi_u = X^\ast$).

Ces caractérisations sont toutes équivalentes :
- $u^n = 0$
- $\Chi_u = X^n$
- $\pi_u = X^p$, $p \leq n$
- $\exists \mathcal{B} \mid Mat_\mathcal{B} u$ est une matrice triangle
  supérieure
- La trace de $A^k$ est nulle pour tout $k \geq 1$

### Commutant
On note le commutant $\mathcal{C}(u) = \{v \mid uv = vu\}$.

La classe de similitude de $u$ est l'ensemble des endomorphismes semblables à $u$.
C'est un fermé si et seulement si $u$ est diagonalisable. Sur $\mathbb{C}$, deux
endomorphismes sont semblables si et seulement si $\forall \lambda,\mu$
$\text{rg}(u - \lambda id)^{\mu} = \text{rg}(v - \lambda id)^{\mu}$.
