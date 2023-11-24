# Suites et séries de fonctions
On notera dans tout le cours que $f_n, u_n : A \subset E \to F$.

## Rappels théoriques
### Continuité
Pour $E$ et $F$ des espaces de dimension finie, et $A \subset E$ un compact,
$\mathcal{C}^0(A,F)$ avec la norme $N_{\infty}$ est un espace complet,
donnant que "la convergence uniforme d'une suite de fonctions $\mathcal{C}^0$
est $\mathcal{C}^0$ dans un compact".

### Dérivation
$\mathcal{C}^1(I,F)$ avec $I \subset \mathbb{R}$ un segment peut se munir d'une
norme $N(f) = N_\infty(f) + N_{\infty}(f')$ ou
$\| f \| = \| f(x_0) \| + N_{\infty}(f')$ avec $x_0 \in A$;
ces deux normes sont équivalentes et $\mathcal{C}^1(I,F)$
est complet pour ces normes.

### Intégration
Si $f_n$ converge uniformément vers $f$, une intégrale de $f_n$ converge
vers l'intégrale de $f$. En effet, $\| \int\limits_{a}^{b} f_n - f \| \leq N_\infty(f_n - f) (b - a)$.

## Étude d'une limite d'une suite/série de fonctions
### Différents modes de convergence
Les suites de fonctions peuvent converger de deux manières : simplement et
uniformément. La convergence simple correspond à la convergence en chaque point
$x \in A$ de $f_n(x)$ vers $f(x)$. La convergence uniforme, elle est la
convergence pour $N_\infty$ de $f_n$ vers $f$. Elle implique la convergence
simple, mais pas l'inverse.

On peut reformuler la convergence uniforme comme la possibilité de restreindre
tous les points en même temps : $\forall \varepsilon > 0, \exists n_0 \mid \forall x \in A, \forall n \geq n_0, \| f_n(x) - f(x) \| \leq \varepsilon$.

Pour une série, la convergence simple peut s'appliquer de la même façon que la
convergence habituelle de la série en chaque point (il peut y avoir convergence
absolue ou pas). La convergence normale correspond à la convergence de $\sum N_\infty(u_n)$,
elle implique la convergence simple. Enfin, la convergence uniforme est définie
comme la convergence uniforme de sa somme partielle. On définit comme les autres
séries le reste et les sommes partielles.

Une série $\sum u_n$ converge si et seulement si $S_n$ converge uniformément,
si et seulement si $R_n = S - S_n$ converge uniformément vers $0$, si et seulement si
$N_\infty(R_n)$ tend vers $0$. Ainsi, la convergence normale implique la
convergence uniforme.

### Continuité
On peut, sur toutes ces preuves sauf contre-indication, remplacer les
convergences uniformes par la convergence uniforme sur tout compact de $A$.

#### Suites
> Si les membres de la suite $f_n$ sont continus, et que la suite converge
> uniformément, alors sa limite $f$ est continue sur $A$.

On ne requiert pas que $A$ soit un compact ici; il nous suffit de prendre un
voisinage compact autour de chaque point de $A$ pour faire la preuve.

En fait, il nous suffit d'avoir la convergence uniforme sur tout compact de $A$.

#### Séries
> Soit $\sum u_n$ convergeant uniformément ou normalement sur tout compact de $A$,
> et où chaque $u_n$ est $\mathcal{C}^0$, $\sum u_n$ est $\mathcal{C}^0$ sur $A$.

#### Dérivabilité
> Soit $f_n$ une suite de $\mathcal{C}^1(I \subset \mathbb{R}, F)$, telle que
> $f_n$ converge uniformément sur $I$ vers $f$ et $f_n'$
> converge uniformément sur $I$ vers $g$,
> alors $f$ est $\mathcal{C}^1(I,F)$ et $f' = g$.

> Soit $f_n$ une suite de $\mathcal{C}^1(I \subset \mathbb{R}, F)$, telle que
> $f_n$ converge simplement en un point de $I$ et $f_n'$
> converge uniformément sur $I$ vers $g$,
> alors $f_n$ converge simplement vers $f$ sur $I$,
> et converge uniformément sur tout compact de $I$; de plus,
> $f$ est $\mathcal{C}^1(I,F)$ et $f' = g$.

Cette propriété provient directement de l'équivalence de normes qu'on a
mentionné dans la première partie.

#### Séries et dérivabilité
Grâce à la linéarité de la dérivation, on obtient des propriétés analogues sur
les séries.

> Soit $u_n$ une suite de $\mathcal{C}^1(I \subset \mathbb{R}, F)$, telle que
> $\sum u_n$ converge uniformément sur $I$ vers $f$ et $\sum u_n'$
> converge uniformément sur $I$ vers $g$,
> alors $\sum u_n$ est $\mathcal{C}^1(I,F)$ et $f' = g$.

> Soit $u_n$ une suite de $\mathcal{C}^1(I \subset \mathbb{R}, F)$, telle que
> $\sum u_n$ converge simplement en un point de $I$ et $\sum u_n'$
> converge uniformément sur $I$ vers $g$,
> alors $\sum u_n$ converge simplement vers $\sum u_n$ sur $I$,
> et converge uniformément sur tout compact de $I$; de plus,
> $f$ est $\mathcal{C}^1(I,F)$ et $f' = g$.

#### Dérivées successives
> Soit $f_n$ une suite de $\mathcal{C}^k(I \subset \mathbb{R}, F)$, telle que
> $f_n^{(i)}$ converge uniformément sur $I$ vers $g_i$ pour tout $i \in [\![0;k]\!]$
> alors $g_0$ est $\mathcal{C}^k(I,F)$ et $g_0^{(k)} = g_i$ pour tout $i \in [\![0;k]\!]$.

> Soit $f_n$ une suite de $\mathcal{C}^k(I \subset \mathbb{R}, F)$, telle que
> $f_n^{(i)}$ converge simplement sur $I$ vers $g_i$ pour tout $i \in [\![0;k - 1]\!]$
> et $f_n^{(k*)}$ converge uniformément sur $I$ vers $g_k$,
> alors $g_0$ est $\mathcal{C}^k(I,F)$ et $g_0^{(k)} = g_i$ pour tout $i \in [\![0;k]\!]$.

On peut remarquer que, pour des $(x_i)_{[\![0;k]\!]}$ deux à deux distincts, la
norme $N(f) = \sum\limits_{i = 0}^{k} N_\infty(f^{(i)})$ est équivalente à
$\| f \| = \sum\limits_{i = 0}^{k - 1} \| f(x_i) \| + N_\infty(f^{(k)})$
(dans la somme, seulement des valeurs de $f$ sur des points !), et
$\mathcal{C}^k$ est complet pour ces deux normes. On aboutit à un théorème hors
programme similaire. On peut aussi dériver un résultat pour des $(x_i)_{[\![0;k]\!]}$
pas nécessairement distinct avec $\| f \| = \sum\limits_{i = 0}^{k - 1} \| f^{(i)}(x_i) \| + N_{\infty}(f^{(k)})$.

On obtient des propriétés analogues pour les séries.

#### Continuité infinie
$\mathcal{C}^{\infty}$ n'est pas un espace normé complet

#### Primitivation
Soit $f_n \to f$, on veut $\int\limits_{0}^{x} f_n \to \int\limits_{0}^{x} f$ :
pour cela, on a besoin de la compacité de $[0;x]$ et la convergence uniforme.

On peut aussi travailler sur les primitives en obtenant leur convergence simple
ou leur convergence en un point et sur la convergence uniforme de la fonction
grâce aux théorèmes sur la dérivation vu plus haut.
