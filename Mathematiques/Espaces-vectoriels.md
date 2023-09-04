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
