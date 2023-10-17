# Topologie
On cherche dans ce chapitre à donner un sens aux notions de proximité :
il s'agit de donner un langage à la continuité, puis à l'utiliser en
mathématiques.

## Normes
### Définition
> Une norme $\| \cdot \|$ est une application d'un $\mathbb{K}$-espace vectoriel 
> dans $\mathbb{R}_{+}$ respectant quatre axiomes :
> - Positivité (les valeurs d'arrivée sont toutes positives ou nulle)
> - Homogénéité ($\| \lambda \cdot x \| = |\lambda| \| x \|$)
> - Séparation (le seul vecteur ayant pour image $0$ est le vecteur nul)
> - L'inégalité triangulaire ($\| x + y \| \leq \| x \| + \| y \|$)

On peut en déduire la deuxième inégalité triangulaire habituelle
($| \| x \| - \| y \| | \leq \| x - y \|$). Pour toute partie d'un espace
vectoriel, on ne peut pas toujours définir une "norme" en soi, mais on peut
définir une distance (avec des axiomes classiques) qui est définie comme
$d(x,y) = \| x - y \|$.

### Exemples usuels sur $\mathbb{R}^n$ et $\mathbb{C}^n$
Des normes usuelles sont les $p$-normes, définies pour $x = (x_i)_{i \in [\![1;n]\!]}$
comme $N_p(x) = \sqrt[p]{\sum\limits_{k = 0}^{n} x_k^p}$, et on définit de même
la limite de cette suite, la norme infinie, telle que
$N_\infty(x) = \text{sup}(x_i)_i$. On peut le vérifier.

On peut aussi dériver des normes bizarres dans des espaces normés produit
avec des normes sur $\mathbb{R}^n$ avec $n$ le nombre d'espaces dans le produit
(VÉRIFIER SI TOUJOURS VRAI).

### Sur  $\mathcal{C}^0([0;1];\mathbb{R})$
On définit les $p$-normes sur ces espaces de fonctions comme celles dans les
espaces de dimension finie, mais avec des intégrales à la place des sommes.

On peut trouver que $N(f) = \int\limits_{0}^{1} f^2(t) \pi(t) dt$ est une norme
si et seulement si $\pi(t)$ est $\mathcal{C}^0$ et positive. De même, on trouve
que $(f | g) = \int\limits_{0}^{p_0} f(t) g(t) e^{- t} dt$ est un produit
scalaire.

Pour tout produit scalaire, $(f|f)$ est une norme sur ce même espace. Toutes les
normes ne naissent pas d'un produit scalaire.

### Sur $\mathbb{K}[X]$
On retrouve en général soit $\int\limits_{-1}^{1} |P|$, ou sinon les $p$-normes
sur les coefficients du polynôme.

### Autres espaces
$\ell^{\infty}(\mathbb{R})$ est l'espace vectoriel des suites bornées réelles,
sur lequel une norme est la norme infinie. Sur l'espace des séries réelles
absolument convergentes $\ell^1(\mathbb{R})$, la somme de la valeur absolue des
élément d'une suite est convergente et est une norme.

Sur $\ell^2(\mathbb{R})$ l'espace des suites réelles, $(u|v) = \sum u_n v_n$
est un produit scalaire.

On travaille en général sur les applications linéaires en dimension finie, soit
les applications linéaires continues en dimension infinies.

## Topologie
### Convergence des suites
On peut utiliser les normes pour définir une convergence des suites dans tout
espace normé comme on le faisait dans n'importe quel corps (cette définition, on
le verra, peut se réduire à des concepts plus puissants).

On obtient à nouveau des propriétés comme l'unicité et la linéarité de la
limite (à partir d'un peu d'epsilons et d'inégalité triangulaire).

On étend aussi les notations de Landau $O$, $o$ et $\sim$.

### Ouverts et fermés
Soit $E$ un EVN (espace vectoriel normé).

On définit $B(a,r) = B_o(a,r)$ la boule ouverte de center $a$ et de rayon $r$
comme $\{x \mid \| x - a \| < r \}$, et la boule fermée $B_f(a,r)$ quand
l'inégalité est large ($\leq$).

On dit que $V$ est un voisinage de $a$ si c'est un sous-ensemble de l'espace tel qu'il
existe $B(a,r) \subset V$. Un sous-ensemble est appelé ouvert s'il est voisinage
de chacun de ses points. Une définition équivalente est que pour tout point d'un
ouvert, il existe une boule ouverte de rayon non nul centrée en ce point qui est
incluse dans l'ouvert.

Un fermé est un ensemble complémentaire à un ouvert. Certains sous-ensemble ne
sont ni ouverts, ni fermés, et certains sont l'un et l'autre.

On appelle topologie un ensemble de sous-ensembles d'un espace appelé ensemble
des ouverts, contenant l'ensemble vide, tout l'espace, et les unions et les
intersections finies d'ouverts.

On peut identiquement définir une topologie par les fermés, en incluant $\emptyset$ et
l'espace comme fermés et en ayant la stabilité par intersection quelconques et
unions finies.

### Caractérisation séquentielle des fermés
> $F \subset E$ est un fermé si et seulement si toute suite convergente d'éléments
> de $F$ converge dans $F$.

### Influence de la norme
> Soit $N$ et $\| \cdot \|$ deux normes sur $E$, elles sont dites équivalentes
> (et c'est en effet une relation d'équivalence) si $\exists c,C \neq 0 \mid \forall x, c \| x \| \leq N(x) \leq C \| x \|$.
> Les topologies définies par les deux normes sont alors les mêmes.

Les propriétés qualitatives sont alors les mêmes, bien que les détails
quantitatifs soient différents.

En dimension finie, toutes les normes sont équivalentes.

### Continuité et limites
#### Adhérence, intérieur
> L'intérieur $\mathring{A}$ d'un ensemble $A$ correspond aux points de l'ensemble
> pour lesquels il existe une boule ouverte de rayon non nul contenue dans $A$.

> L'adhérence $\overline{A}$ d'un ensemble $A$ est l'ensemble des points tels
> qu'il existe une suite dans $A$ convergeant vers ce point.

L'intérieur est le plus petit ouvert contenu dans $A$, et l'adhérence est le
plus petit fermé contenant $A$. Ainsi, $A = \mathring{A}$ si et seulement si
$A$ est un ouvert, $A = \overline{A}$ si et seulement si $A$ est un fermé.
