# Arithmétique dans les anneaux
## Divisibilité
Soit $A$ un anneau intègre (pas $\mathbb{Z}/n\mathbb{Z}$ pour $n$ pas premier)
commutatif.

On appelle idéal de $A$ un sous-groupe additif de $A$ stable par multiplication
externe dans $A$. C'est le cas pour les inversibles d'un anneau, ou encore
l'ensemble des multiples d'un élément.

On dit que $a \mid b$ si $\exists q \in A \mid b = aq$, ce qui est équivalent à
que l'idéal engendré par $b$ $(b)$ soit dans $(a)$.

Un élément irréductible est un élément pour lequel les seuls diviseurs sont
inversibles. On peut vérifier cette définition dans $\mathbb{Z}$ ou
$\mathbb{Z}[X]$. C'est pourquoi un polynôme en $\mathbb{Z}$ irréductible est un
polynôme déjà divisé par son contenu en plus d'irréductible pour les inconnues.

Un anneau factoriel est un anneau dans lequel tout élément est décomposable en
produit d'irréductibles avec unicité (à l'ordre près et aux inversibles près).
On peut alors démontrer le théorème de Gauss et le théorème fondamental de
décomposition de l'arithmétique.

Les irréductibles des entiers de Gauss sont les nombres premiers qui sont $3 [4]$,
et les $\pi$ et sont conjugués tels que les nombres premiers qui sont $1[4]$
sont égaux à $\pi \overline{\pi}$.

Un élément premier (qui est différent d'un irréductible tant que l'on est pas
dans un anneau à PGCD) est un élément $p$ tel que $p \mid ab \Rightarrow p \mid a \lor p \mid b$.

## Exemple de $\mathbb{K}[X]$
On peut considérer $\mathbb{K}[X]$ comme un $\mathbb{K}$-EV avec la base
canonique de la famille échelonnée en degré.
C'est aussi une algèbre car il forme un anneau avec une application bilinéaire.
En tant qu'anneau, les polynômes sont de plus euclidiens (division euclidienne),
ce qui fait que tout idéal de l'anneau est unique à constante multiplicative
près, rendant l'anneau idéal principal (tout idéal est généré par un élément
unique), et donc un anneau factoriel.

En l'occurrence, ses irréductibles sont compliqués à obtenir (les polynômes de
degré 1 dans $\mathbb{C}$, les polynômes de degré $1$ ou $2$ de discriminant
négatif). Sur $\mathbb{Q}$, il en existe de tout degré, et sur $\mathbb{Z}/p\mathbb{Z}$,
on connaît le nombre d'irréductibles de chaque degré.

On peut réécrire la division euclidienne par $D$ de degré $n$ (sur un polynôme
de degré plus grand) comme $\mathbb{K}[X] = (D) \oplus \mathbb{K}_{n-1}[X]$.
Comme pour $a,b \in A$, on a $(a) + (b) = (c)$ avec $c = (a,b)$ (car l'anneau
est idéal principal).

La division Euclidienne permet d'obtenir un algorithme d'Euclide, qui donne de
la même façon que sur les entiers le PGCD.
Le lemme de Gauss est obtenu à partir du théorème de Bézout (qu'on peut prouver
à partir d'un algorithme d'Euclide inversé). On peut aussi prouver le théorème
de Bézout par le fait que dans un anneau idéal principal, la primalité entre
deux éléments entraîne la primalité entre leurs idéaux engendrés.

On peut ainsi prouver que pour tout $u \in \mathcal{L}(E)$ a un polynôme de
degré minimal qui existe pour les annulateurs de $u$. Celui-ci va de plus
diviser le caractéristique (et il a $n$ valeurs propres distinctes quand ils
sont égaux).

L'anneau $\mathbb{K}[X][Y]$ est factoriel, mais pas grand chose de plus. En
effet, pour une seule variable, l'image réciproque d'une valeur est finie, mais
ce n'est pas le cas pour deux (par exemple l'infinité de solutions pour $x^2 +
y^2 = 1$), et on ne peut pas vraiment diviser le polynôme avec la racine.

Petit moment de bullshit Polytechnique, on définit $i$ un multi-indice $(i_k)_{[\![1;n]\!]}$,
et on note $|i| = \sum\limits_{k = 1}^{n} i_k$, $i! = \prod\limits_{k = 1}^{n} i_k!$,
$X^i = \prod\limits_{k = 1}^{n} X_k^{i_k}$ et $\partial^i P = \frac{\partial^{i} P}{\partial X_1^{i_1} \ldots}$,
et on a Taylor : $P = \sum_i \frac{X^i}{i!} \partial^i P(0)$ (utile en topo
dessus derrière).
