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

## Méthodes pratiques
### Convergence uniforme pour une suite
Soit $f_n$ convergeant simplement vers $f$, majorer $|f_n - f|(x)$ par une
constante indépendante de $x$ tendant vers $0$. On peut ainsi trouver la
convergence uniforme, ou éventuellement la convergence uniforme sur un
intervalle.

### Non convergence uniforme
On peut chercher à calculer la borne supérieure de $|f_n - f|$ sur un intervalle
bien choisi, minorer le sup par une valeur en un $x_n$ (par exemple, $x_n = \frac{1}{n^2}$
pour travailler sur $n^2 x (1 - x)^{n^2}$), ou encore nier un
théorème sous hypothèse de convergence uniforme.

### Convergence normale d'une série
Il faut bien choisir l'ensemble pour chaque paramètre sur lequel on peut espérer
la convergence simple, uniforme, et enfin normale. Pour cela, il est souvent
utile de refaire la convergence simple proprement et montrer les points à
problèmes.

### Convergence uniforme sur une série
A priori, on peut l'établir par convergence normale, ou encore en trouvant un
bon majorant de $|R_n|$ tendant vers $0$. On peut aussi l'obtenir, en trouvant
quand c'est possible, avec le critère des séries alternées.

Une fois de plus, on peut nier un théorème, notamment celui d'interversion des
limites.

### Rédaction - Une béquille classique
On s'imagine l'étude d'une fonction $F(x) = \sum u_n(x)$.

1. Continuité : on trouve la convergence simple pour un $x$ fixé, avec la
   convergence simple ou absolue, un équivalent, le CSSA, d'Alembert, ou même
   Abel ... Puis on cherche à obtenir sa convergence uniforme sur des
   intervalles fermés. Ne pas essayer de faire des développement asymptotiques
   sur plusieurs variables (sauf après avoir rendu l'expression dépendante d'une
   variable unique). Enfin, on rédige la continuité de $F(x)$.

2. Classe $\mathcal{C}^1$ : On peut d'abord réutiliser les mêmes techniques, en
   se concentrant cette fois sur la convergence normale et uniforme pour obtenir
   les théorèmes de ce cours.

3. Classe $\mathcal{C}^{\infty}$ : Tout d'abord vérifier les dérivées $k$-ièmes
   pour voir si ça marche, puis obtenir la convergence simple ou uniforme pour
   un $k$ fixé. Cela peut aussi être le moment de sortir les séries entières,
   sur les $u_n$ en appliquant Fubini, afin de montrer que $f_n$ est lui-même
   une série entière et donc $C^{\infty}$.

### Théorème d'interversion des limites
> Soit $F = \sum u_n$ convergente uniformément au voisinage de $a$, et telle que
> $u_{n} \xrightarrow[a]{} \ell_n$, alors $\sum \ell_n$ converge et
> $F \xrightarrow[a]{} \sum \ell_n$.

En général, on devra s'occuper du cas où $\ell_n = 0$.

### Théorème d'interversion somme-limite
> Soit $f_n$ convergeant simplement vers $f$, toutes des fonction
> $\mathcal{C}^0_m$ sur $I$, et $|f_n| \leq g$ sur $I$, avec $g \in L^1$,
> alors $\int\limits_{I} f_n \to \int\limits_{I} f$.

On peut remplacer l'hypothèse de convergence dominée, qui exige une fonction
$L^1$, pour la compacité de $I$ avec la convergence uniforme de la suite si on
peut la déterminer.

> Soit $\sum u_n$ convergeant simplement sur $I$, $u_{n}$ et $\sum u_{n}$ étant
> $\mathcal{C}^0_m$ sur $I$, et $\sum \int\limits_{I} |u_{n}|$ convergente,
> on a $\int\limits_{I} \sum u_{n} = \sum \int\limits_{I} u_{n}$.

En pratique, on pourra utiliser le théorème pour calculer des intégrales de
fonctions en les divisant en sommes finies (qui marchent toujours) ou en séries.

On peut avoir une sorte de remplacement de la convergence dominée par la
monotonie de fonctions, l'un des moyens de trouver la convergence dominée.

> Soit $f_n$ convergeant simplement vers $f$, toutes des fonction
> $\mathcal{C}^0_m$ sur $I$, et tous les $f_n$ des fonctions croissantes,
> $\int\limits_{I} f_n$ converge si $f$ est $L^1$, et si oui,
> $\int\limits_{I} f_n \to \int\limits_{I} f$.

Soit $\sum u_n$ convergeant simplement sur $I$, $u_{n}$ et $\sum u_{n}$ étant
$\mathcal{C}^0_m$ sur $I$, et tous les $u_{n}$ sont positifs, alors $\sum \int\limits_{I} u_{n}$
converge quand $\sum u_{n}$ est $L^1$ sur $I$, et le cas échéant
on a $\int\limits_{I} \sum u_{n} = \sum \int\limits_{I} u_{n}$.
