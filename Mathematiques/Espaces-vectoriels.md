# Espaces vectoriels
## Définitions
> Soit $\mathbb{K}$ un corps commutatif (de caractéristique quelconque),
> et $(E,+)$ un groupe abélien, $E$ un ensemble et une loi externe $\cdot \in E^{\mathbb{K} \times E}$
> compatible avec l'opération de groupe, $E$ est un espace vectoriel.

- Un $\mathbb{R}$-EV muni d'un endomorphisme tel que $u^2 = - \text{id}$ peut
  être muni d'une structure de $\mathbb{C}$-EV, et sa dimension en $\mathbb{R}$
  est paire
- Un groupe fini dont les éléments sont leur propre inverse est isomorphe à
  $(\mathbb{Z} / 2 \mathbb{Z})^n$.

On caractérise en général les EV et SEV par stabilité par combinaison linéaire,
souvent trivial sauf parfois sur l'addition.

> Une application linéaire (morphisme d'EV) est une application dont l'image d'une
> combinaison linéaire est la combinaison linéaire des images.

On forme ainsi $\mathcal{L}(E,F)$ l'espace vectoriel des morphismes de $E$ à
$F$.

On entend par combinaison linéaire de familles des combinaisons avec au plus une unique
occurrence de chaque élément; il faut faire attention à la préciser.

> Une famille est libre si on ne peut pas obtenir $0$ par combinaison linéaire
> dont tous les coefficients ne sont pas nuls de ses éléments; une famille est
> liée si elle n'est pas libre. Une famille génératrice permet d'obtenir tout $x
> \in E$ par combinaison linéaire de ses éléments.

> Une famille infinie est libre si toute ses sous-familles finies sont libres.

- La famille des monômes de degré dans $\mathbb{N}$ est une famille libre de $\mathbb{R}^{\mathbb{R}}$
- La famille des $f(x) = x^{\alpha}$, $\alpha \in \mathbb{R}$ est libre dans $(\mathbb{R}_{+}^{\ast})^{\mathbb{R}}$,
  de même pour $\alpha \in \mathbb{C}$.

> Une famille infinie est génératrice s'il existe toujours une CL finie qui
> reconstitue tout $x \in E$.

> $\text{Vect}(A)$ est l'ensemble des combinaisons linéaires de $A$. Il s'agit
> aussi du plus petit sous-EV contenant $A$.

> La somme de SEV correspond au sous-espace vectoriel contenant les combinaisons
> linéaires des éléments des SEV. On parle de somme directe (notée avec $\oplus$
> et $\bigoplus\limits_{E}$) lorsque pour tout élément du produit, il existe une
> décomposition unique en éléments de chacun des membres de la somme.

Pour caractériser la somme directe, toutes ces affirmations sont équivalentes et
définissent la somme directe :
- Pour toute combinaison linéaire selon les SEV sommés donnant $0$, les éléments
  pris dans chaque SEV sont $0$
- L'intersection de tout élément sommé avec la somme des autres est $\{0\}$
- $\begin{aligned} \prod F_i &\to \sum F_i \\ (y_i)_i &\mapsto \sum y_i .\end{aligned}$
  est un isomorphisme (elle est toujours surjective, on prouve l'injectivité, ce
  qui est la même chose que les autres)
- En dimension finie, la dimension de la somme est égale à la somme des
  dimensions
- Pour tout élément de la somme, il existe une unique décomposition en éléments
  des membres de la somme

$\begin{aligned} \varphi: \mathcal{L}(A \oplus B, F) &\to \mathcal{L}(A,F) \times \mathcal{L}(B,F) \\ u &\mapsto (u\restriction_{A}, u\restriction_{B}) .\end{aligned}$
est un isomorphisme d'EV.

$A = \mathbb{K} e \mid e \neq 0 \Rightarrow \mathcal{L}(A,F) \cong F$,
ce qui donne d'ailleurs $\text{dim}(E) = n \Rightarrow \mathcal{L}(E,F) \simeq F^n$
et $\text{dim}(\mathcal{L}(E,F)) \Rightarrow \text{dim}(E) \text{dim}(F)$.

Voir aussi la démonstration de la formule de Grassman
($\text{dim}(F + G) = \text{dim}(F) + \text{dim}(G) - \text{dim}(F \cap G)$).

> Un projecteur est une application linéaire $p$ telle que $p^2 = p$.

On a $E = \text{Ker}(p) \oplus \text{Im}(p)$.

Soit $F,G$ deux supplémentaires (en somme directe) de $A$ un SEV de $E$, $F \cong G$.

Pour $p, q$ des projecteurs, $p + q$ est un projecteur si et seulement si $pq = qp = 0$.

## Espaces vectoriels de dimension finie
### Lien avec l'isomorphisme
> Un espace vectoriel admet une base de cardinal $n$ si et seulement si $E$ est en
> isomorphisme avec $\mathbb{K}^{n}$.

On peut alors compléter toute famille libre en une base de cardinal $n$.
De plus toute famille de $n + 1$ vecteurs est liée.

On peut ajouter à un membre d'une famille une combinaison linéaire des autres
membres sans changer le caractère libre ou lié de la famille (permet le pivot de
Gauss).

> Si $E$ admet une famille libre de taille infinie, on note $\text{dim}(E) = \infty$;
> si $E$ admet une base de cardinal $n$, $\text{dim}(E) = n$.

On peut facilement prouver que la dimension d'un espace vectoriel est unique
(toutes les bases sont de même cardinal), et qu'un espace est de dimension soit
finie soit infinie grâce aux résultats précédents sur la taille des familles
libres et génératrices.

> $E \subset F \land \text{dim}(E) = \text{dim}(F) < \infty \Rightarrow E = F$

En effet, les bases de $E$ sont libres dans $F$, et ont la cardinalité d'une
base de $F$, donc sont une base de $F$.

> Soit une application linéaire $u \in F^{E}$ avec $\text{dim}(E) > \text{dim}(F)$,
> $u$ n'est pas injective. De même, si $\text{dim}(E) < \text{dim}(F)$,
> $u$ n'est pas surjective.

### Rang d'une application linéaire
> Le rang d'une application linéaire est la dimension du codomaine de
> l'application.

Il existe alors un isomorphisme entre tout sous-espace $A$ supplémentaire de $\text{Ker}(u)$
et l'image de $u$ (pour toute dimension). En revanche, il faut faire attention
car l'existence d'un supplémentaire n'est pas automatique (c'est une assertion
équivalente à l'axiome du choix).

__Preuve :__ L'application créée est linéaire puisque c'est l'application
induite sur un SEV du domaine. Elle est injective car le seul élément ayant pour
image $0$ dans $A$ doit être $0$, et surjective, car $\forall y \in \text{Im}(u)$,
$y = u(x), u(x) = u(x_A + x_{\text{Ker}(u)}) = u(x_A), x_A \in A$.

L'application la plus simple est le théorème du rang, qui donne en dimension
finie pour $u \in F^{E}$ que $\text{rg}(u) + \text{dim}(\text{Ker}(u)) = \text{dim}(E)$
(par Grassman).

On peut ainsi tracer l'équivalence entre matrices et applications linéaires
(un petit diagramme commutatif entre les espaces vectoriels et leur $\mathbb{K}^n$
isomorphe).

On peut dire que deux matrices ou applications linéaires sont équivalentes
si elles sont de même rang, ou si leur matrices $A$ et $B$ admettent deux
matrices inversibles $P$ et $Q$ telles que $B = PAQ$, ou enfin s'il existe des
matrice de changement de base qui les amènent à $J_r$ (la "forme de référence
des matrices de rang $r$").

On se retrouve ainsi dans l'équivalence générale de tous les espaces vectoriels
de dimension finie et de leurs application/matrices en changeant de bases.

### Exemple : Théorème fondamental de la dimension/Lagrange/Vandermonde

Un exemple d'application est de mettre le théorème, pour $(a_i)_{i \in [\![1;n]\!]} \in \mathbb{K}^{n}$,
sur l'application $\begin{aligned} \mathbb{K}[X] &\to \mathbb{K}^n \\ P &\mapsto (P(a_i))_{i \in [\![1;n]\!]} .\end{aligned}$.
En effet, le noyau de l'application est tous les produits de $\prod\limits_{i = 1}^{n} (x - a_i)$,
et l'un de ses supplémentaires est $\mathbb{K}_{n-1}[X]$. On retrouve par
analyse-synthèse sur les conditions trouvées les polynômes interpolateurs de
Lagrange. La matrice de cet isomorphisme est d'ailleurs la matrice de
Vandermonde. Cet isomorphisme permet ainsi d'inverser les matrices de
Vandermonde.

On peut aller encore plus loin et chercher comment on pourrait faire un
interpolateur qui impose des dérivées et des racines aux points d'interpolation.
On veut donc un isomorphisme entre $\mathbb{K}_{2n-1}$ et $\mathbb{K}^{2n}$. On
l'écrit pareil, et il s'agit d'une application injective car on impose $2n$
racines, et elle est donc surjective.

On peut trouver une base de polynômes qui forme les solutions par combinaison
linéaire, et il reste à déterminer ses éléments (les polynômes qui donnent un
résultat de $1$ en un point avec dérivée $0$, et ceux qui donnent $0$ avec une
dérivée de $1$).
