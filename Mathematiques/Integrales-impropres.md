# Intégrales impropres
Le but va être de faire des intégrales qui convergent vers des bornes ouvertes,
ou encore qui continuent jusqu'à l'infini.

## Définition
On travaille sur des fonction continues ou continues par morceaux, définies sur
un intervalle de $\mathbb{R}$ à valeurs dans $\mathbb{R},\mathbb{C}$ ou $E$ un
espace de dimension finie.

> Une fonction continue par morceaux sur $[a;b]$ est une fonction possédant un
> ensemble fini de points, dont le premier est $a$ et le dernier $b$, tels que
> la fonction restreinte aux intervalles $]x_i;x_{i+1}[$ se prolonge en une
> fonction continue en $[x_i;x_{i+1}]$. De façon équivalente, elle est continue
> sur $[a;b]$ privé des $x_i$ et admet des limites à droite et à gauche pour ces
> points.

Ainsi, $\left\lfloor \frac{1}{x} \right\rfloor$ est continue par morceaux sur
$]0;1]$ mais pas sur $[0;1]$. Pour définir l'intégrale sur des fonctions
$\mathcal{C}^0_m$, il faut utiliser la relation de Chasles. De plus, on ne peut
pas considérer que l'intégrale est une primitive, contrairement aux fonctions
continues.

## Convergence
Soit $f$ $\mathcal{C}^0_m$ sur $I$, avec $I = [a;b[$,
on note $F(x) = \int\limits_{a}^{x} f(t) dt$.
Si $F$ admet une limite $L$ en $b$, on dit que $\int\limits_{a}^{b} f$ converge
vers $L$.

> Si $\int\limits_{a}^{b} \| f \|$ converge, on dit que $\int\limits_{a}^{b} f$
> est absolument convergente.

Celle-ci entraîne la convergence de $\int\limits_{a}^{b} f$.

On étudie, comme pour les séries, des "sommes partielles"
$\int\limits_{a}^{x} f$ avec $x$ qui tendra vers $b$,
et des "restes partiels" quand l'intégrale converge, sous la forme
$\int\limits_{x}^{b} f$.

> Si $c \in [a;b[$, $\int\limits_{a}^{b} f$ converge si et seulement si
> $\int\limits_{c}^{b} f$ converge, et on peut alors appliquer la relation de
> Chasles. De plus, la propriété conserve aussi la convergence absolue.

De plus, on a l'assurance que peu importe le $c$, le résultat soit le même.

Lorsqu'on cherche à intégrer sur $]a;b[$, on dit que l'intégrale est (absolument)
convergente quand $\int\limits_{a}^{c} f$ et $\int\limits_{c}^{b} f$
sont (absolument) convergentes.

$f$ est dite intégrable sur $I$ (ou appartenant à $L^1(I)$)
si $\int\limits_{a}^{b} |f|$ est absolument convergente.

Dans le cas de $\mathbb{C}$ ou d'espaces vectoriels, une intégrale est
(absolument) convergente si et seulement si les intégrales sur les composantes de
l'espace d'arrivée sont (absolument) convergentes.

## Exemples
$f(t) = \frac{1}{t^\alpha}$ est $L^1$ sur $[a;+\infty[$ si et seulement si
$\alpha > 1$, et ne l'est pas sinon; elle est $L^1$
sur $]0;a]$ si et seulement si $\alpha < 1$ et ne l'est pas sinon.

$\int\limits_{0}^{+\infty} e^{a t} dt$ convergence si $a < 0$,
et diverge sinon.

Contrairement aux séries, il n'existe pas de divergence grossière :
la convergence ne permet pas d'affirmer que la fonction converge vers $0$
ou qu'elle est bornée. Par exemple, en prenant une fonction qui a à chaque $n$
un pic triangle de hauteur $n$ et de largeur $\frac{1}{n^3}$, et est nulle
autrement, alors $\int\limits_{n - \frac{1}{n^3}}^{n + \frac{1}{n^3}} f = \frac{1}{n^2}$,
donnant $\int\limits_{0}^{A} f \leq \sum\limits_{n = 1}^{+\infty}  \frac{1}{n^2}$
qui converge et donc majore l'intégrale pour tout $A$, donnant la convergence
absolue de l'intégrale.

## Comparaison
On a une règle des équivalents de même forme que celle des séries :
pour $f,g \in \mathcal{C}^0_m([a;b[)$, avec $g \geq 0$ au voisinage de $b$
et $f \underset{b}{\sim} g$ :
- Si $\int\limits_{a}^{b} g$ converge (absolument), alors $\int\limits_{a}^{b} f$
  converge (absolument) et leurs restes sont équivalents au voisinage de $b$.
- Si $\int\limits_{a}^{b} g$ diverge, alors $\int\limits_{a}^{b} f$ diverge et
  leurs sommes partielles sont équivalentes au voisinage de $b$.

Pour la négligeabilité, on a avec les mêmes hypothèse et $f = o(g)$
au voisinage de $b$ :
- Si $\int\limits_{a}^{b} g$ converge (absolument), alors $\int\limits_{a}^{b} f$
  converge (absolument) et $\int\limits_{x}^{b} f = o(\int\limits_{x}^{b} g)$
  au voisinage de $b$.
- Si $\int\limits_{a}^{b} g$ diverge, on a seulement
  $\int\limits_{a}^{x} f = o(\int\limits_{a}^{x} g)$.

## Changement de variable
Soit $f \in \mathcal{C}^0_m$ sur $[a;b[$ et $\varphi$ un difféomorphisme de
$[\alpha;\beta[$, alors
$\int\limits_{\alpha}^{\beta} f \circ \varphi(t) \varphi'(t) dt$
est convergente / absolument convergente / divergente
si et seulement si $\int\limits_{a}^{b} f(u) du$
est convergente / absolument convergente / divergente.
