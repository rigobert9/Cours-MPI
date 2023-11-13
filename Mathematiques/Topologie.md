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

#### Cauchy-Schwarz en dimension finie
Soit $( \cdot | \cdot )$ un produit scalaire d'un espace préhilbertien, Cauchy-Schwarz
est un théorème sur la norme associée, donnant
$|(x|y)| \leq N_2(x) N_2(y)$ (attention à ne définir ceci que sur une norme
dérivée d'un produit scalaire, qui est en dimension finie la norme 2).

REVOIR PREUVE PAR TRAVAIL SUR LES ESPACES PRÉHILBERTIENS

### Continuité et limites
#### Adhérence, intérieur
> L'intérieur $\mathring{A}$ d'un ensemble $A$ correspond aux points de l'ensemble
> pour lesquels il existe une boule ouverte de rayon non nul contenue dans $A$.

> L'adhérence $\overline{A}$ d'un ensemble $A$ est l'ensemble des points tels
> qu'il existe une suite dans $A$ convergeant vers ce point.

L'intérieur est le plus petit ouvert contenu dans $A$, et l'adhérence est le
plus petit fermé contenant $A$. Ainsi, $A = \mathring{A}$ si et seulement si
$A$ est un ouvert, $A = \overline{A}$ si et seulement si $A$ est un fermé.

#### Limite
> Soit une fonction $f : A \subset E \to F$, avec $E$ et $F$ des espaces
> vectoriels de dimension finie, soit $a \in \overline{A}$
> $\lim\limits_{x \to a, x \in A} f(x) = \ell$
> si $\forall \varepsilon > 0, \exists \alpha > 0, \| x - a \| \leq \alpha \Rightarrow \| f(x) - \ell \| \leq \varepsilon$.

> Une définition équivalente (celle en topologie générale), est que pour tout
> voisinage $V$ de $\ell$, il existe un voisinage $U$ de $a$ tel que
> $f(U \cap A) \subset V$.

Grâce à cette définition plus complète, on peut définir systématiquement la
limite à l'infini ou les limites en l'infini.

On définit de même la limite des suites. Attention comme toujours à ne pas
présupposer l'existence de la limite.

#### Continuité
> $f$ est dite continue en $a \in A$ si $\lim\limits_{x \to a} f(x) = f(a)$.

#### Lipschitzianité
> $f : A \subset E \to F$ est dite $K$-lipschitzienne si
> $\forall x,y \in A, \| f(x) - f(y) \| \leq K \| x - y \|$.

Une fonction lipschitzienne est toujours continue (au moins de classe $\mathcal{C}^0$)
car on peut toujours prendre $\alpha = \frac{\varepsilon}{K}$.

#### Caractérisation globale de la continuité
> Une fonction est continue si et seulement si pour tout ouvert du codomaine,
> l'application réciproque dessus est un ouvert si et seulement si pour tout
> fermé du codomaine, l'application réciproque dessus est un fermé.

Cette définition générale et fondamentale de topologie est équivalente à notre
définition sur les espaces normés, répétée en chaque point.

#### Continuité et linéarité
> Soit $u \in \mathcal{L}(E,F)$, ces propriétés sont équivalentes :
> - $u$ est continue sur $E$
> - $u$ est continue en $0$
> - $u$ est uniformément continue
> - $u(B_f(0,1))$ est borné
> - $u$ est lipschitzienne
> - $\exists K \mid \forall x, \|u(x)\| \leq K \| x \|$

#### Norme d'opérateur/triple/d'endomorphisme
On prend une nouvelle norme $| \!| \!| u | \!| \!|$ pour $u$ une application de
$\mathcal{L}_{\mathcal{C}}(E,F)$ (une application linéaire continue) qui est
la valeur $\text{sup}_{x \neq 0} \frac{\| u(x) \|}{\| x \|} = \text{sup}_{x \in S(0,1)} \| u(x) \|$.
On l'appelle norme d'opérateur associée à $\| \cdot \|$ (il est important de le
préciser). En plus d'être une norme, elle satisfait l'inégalité des normes
d'algèbre, $| \!| \!| uv | \!| \!| \leq | \!| \!| u | \!| \!| | \!| \!| v | \!| \!|$.

Cette propriété permet beaucoup d'inégalités très pratique, utiles pour la
convergence de séries sur des objets étranges.

#### Continuité uniforme
> $f$ est une fonction continue uniforme si et seulement si
> $\forall \varepsilon > 0, \exists \alpha > 0 \mid \forall x,y \in A$
> $\| x - y \| \leq \alpha \Rightarrow \| f(x) - f(y) \| \leq \varepsilon$.

Une fonction lipschitzienne est ainsi uniformément continue. Lorsque $f$ n'est
pas uniformément continue, on ne peut pas déduire de $x_n - y_n \to 0$ que
$f(x_n) - f(y_n)$. $f$ est uniformément continue si elle est continue sur un
compact (par l'absurde sur ce précédent exemple).

On généralise en fait le théorème des accroissement finis, qui est vrai sur $\mathbb{R}$
car une fonction continue sur un intervalle fermé est uniformément continue.
C'est le théorème d'Heine : toute application continue sur un compact est
uniformément continue.

## Suites
### Valeurs d'adhérence
> Une sous-suite extraite de $(u_{n})$ est la même suite, indexée par une fonction
> strictement croissante d'entiers (une injection croissante).

Si $(u_{n})$ converge vers une limite $\ell$, ses sous-suites extraites
convergent aussi vers cette limite.

Le cas réciproque est bien plus riche (par exemple pour une suite alternant
entre deux valeurs), et motive la définition des valeurs d'adhérence.

> Une valeur d'adhérence de la suite est une valeur vers laquelle converge une
> sous-suite extraite de la suite.

L'ensemble des valeurs de la suite rassemblé avec les valeurs d'adhérence de la
suite correspond à l'adhérence de l'ensemble des valeurs de la suite.

## Homéomorphismes
> Un homéomorphisme est une application continue bijective dont la réciproque est
> continue.

> $f$, une application de classe $\mathcal{C}^k$ est un $\mathcal{C}^k$-difféomorphisme si elle
> est bijective et que sa réciproque est de même classe.

## Points isolés, d'accumulation
> Un point isolé dans $A$ est un point dont l'un des voisinages intersectés avec
> $A$ est son singleton.

De façon équivalente, cela signifie que pour toute suite dans $A$ convergeant
vers un point isolé, la suite est égale à ce point à partir du certain rang.

> Un point d'accumulation $a \in A$ est un point tel que pour tout voisinage,
> l'intersection avec $A$ contient une infinité de points.

Cela signifie que les ouverts contenant $a$ contiennent toujours un nombre
infini de points. De façon équivalente, il existe une suite convergeant vers $a$
dont aucun point n'est $a$.

TODO: Définitions générales/pointless ?

## Connexité
### Connexité générale
> Soit un ensemble $A \subset E$ les propriétés suivantes sont équivalentes :
> - $A$ est connexe
> - Toute fonction continue localement constante sur $A$ est constante
> - Toute fonction continue vers $\{0,1\}$ avec la topologie discrète est constante

Cette propriété se conserve par l'image par une fonction continue.

### Connexité par arcs
> Une partie $A \subset E$ est connexe par arcs si pour tout points $a,b \in A$
> il existe une fonction continue $\gamma$ depuis $[0;1]$ telle que
> $\gamma(0) = a$ et $\gamma(b) = 1$.

Ceci implique la connexité. De plus, c'est impliqué par la convexité. Seule
cette notion est au programme, pas la connexité générale.

La réciproque est fausse, la courbe sinus des topologues est connexe mais pas
connexe par arcs. La propriété est conservée par l'image d'une fonction continue.

Un ouvert d'un espace métrique connexe est en revanche connexe par arcs, car
l'ensemble des points reliables à un point est ouvert et fermé.

## Suites
### Sous-suites, valeurs d'adhérence
> Une sous-suite ou suite extraite d'une suite $u_k$ est la suite $u_{\sigma(k)}$,
> avec $\sigma \in \mathbb{N}^{\mathbb{N}}$ une fonction injective strictement
> croissante.

> Une valeur d'adhérence de $(u_k)$ est la limite d'une sous-suite convergente de $(u_k)$.

### Compacité
> Une partie $A \subset E$ est compacte si toute suite d'éléments de $A$ admet une
> valeur d'adhérence dans $A$.

Cette définition est la définition de la compacité séquentielle, différente
d'autres notions de compacité en topologie générale. La définition de la
compacité est que tout recouvrement ouvert de la partie peut être réduit à un
recouvrement fini. La compacité séquentielle implique la compacité (par
l'absurde en construisant une suite de points qui sont dans la partie de $A$ pas
couverte par un recouvrement fini), et la compacité implique la compacité
séquentielle dans les espaces métriques avec l'axiome du choix dénombrable.

Les intervalles fermés de $\mathbb{R}$ sont des compacts, car on peut procéder
par dichotomie pour encercler des sous-intervalles de proche en proche contenant
un nombre infini d'indices de la suite : il s'agit du théorème de
Bolzano-Weierstrass.

On a donc un équivalent des ensembles finis, et plus exactement du principe des
tiroirs : toute suite à valeurs dans un ensemble fini/compact admet une valeur
atteinte/approchée une infinité de fois.

Pour $A$ compact, pour toute suite de fermés non nuls décroissante pour
l'inclusion de $A$, leur intersection est non nulle.

> Un compact est fermé et borné.

On obtient ceci car si une suite converge, comme elle admet une valeur
d'adhérence dans $A$, sa limite est dans $A$. La bornitude s'obtient avec cette
même valeur d'adhérence.

La réciproque ne se prouve que pour les espaces de dimension finie.

### Construction de compacts
> Soit $A,B$ des compacts, $A \times B$ est un compact.

On peut le généraliser à tout produit fini, et les produits infinis sont prouvés
par le Théorème de Tychonoff (qui fait les deux sens), juste un peu moins fort
que l'axiome du choix (et qui l'utilise souvent dans ses preuves). Attention
néanmoins à définir la topologie produit, qui est celle où les ouverts sont les
produits d'un nombre fini d'ouverts des espaces du produit avec le produit de
tous les autres espaces entier (contrairement à la topologie coproduit qui prend
tous les produits, et où ce théorème échoue).

On définit ici la norme produit comme la norme associant la borne supérieure des
valeurs de normes sur chaque coordonnée.

> Soit $A$ compact, $B \subset A$ est compact si et seulement si $B$ est fermé.

> $A \subset \mathbb{K}^n$ est compact si et seulement si il est fermé et borné

Le sens direct est déjà prouvé, et on montre la réciproque avec le théorème du
produit plus haut (s'il est borné en $M$, alors toutes les coordonnées sont
contenues dans $[-M;M]$, alors ce sont des compacts).

### Compacité et continuité
> L'image directe d'un compact par une fonction continue est compacte.

(Dans le cas de la topologie générale, c'est vrai seulement si l'espace
d'arrivée est séparé.)

> L'image d'un compact par une fonction continue est bornée et atteint ses bornes.

En effet c'est un compact donc elle est bornée, puis pour un suite tendant à
travers $f$ vers la borne, celle-ci a pour unique valeur d'adhérence une valeur
en laquelle la borne est atteinte et qui est dans le compact par compacité.

Pour être un homéomorphisme, il faut non seulement la bijection mais aussi la
continuité, donc que les images réciproques des ouverts soient des ouverts, donc
pour une bijection que la fonction soit ouverte et fermée (l'image directe d'un
ouvert est ouverte). Pour toute fonction bijective entre deux parties, on a donc
leur restriction à un compact qui est un homéomorphisme (car les fermés à
l'intérieur sont compacts).

> La restriction d'une bijection continue d'un compact à son image est un homéomorphisme.

Puisque la sphère unité pour la $N_\infty$ est compact, et que toute norme $N$ est
continue pour $N_\infty$, $N$ est bornée et atteint ses bornes. Sa borne
inférieure $m$ est supérieure à $0$ par séparation; ainsi, $N_\infty(x) = 1 \Rightarrow N(x) \geq m$.
Or, par homogénéité $N(x) \geq m N_\infty(x)$ (car $\frac{x}{N_\infty(x)} \in S$).
Ainsi, les normes en dimension finie sont équivalentes.

### Compacité et suites
> Une suite dans un espace de dimension finie converge si et seulement si elle a
> une unique valeur d'adhérence.

Une suite de Cauchy est une suite dans laquelle la distance entre les points
devient arbitrairement petite ($d(u_{p}, u_{q}) \to 0$ POUR TOUT P ET Q
AU-DESSUS D'UN $n_0$) (cette notion est très forte, voir la suite $\ln(n)$ qui montre
que $d(u_{n+1} - u_{n}) \to 0$ ne suffit pas). Dans tout espace métrique, une
suite convergente est de Cauchy. Un espace est complet quand la réciproque est
vraie.

> Tout espace normé de dimension finie est complet.

__Preuve :__ On fait, sans vraiment de perte de généralité, la preuve dans
$\mathbb{R}^n$. La preuve se résume alors à la séparation des coordonnées dans
$\mathbb{R}$, qui est complet (par construction).

Si un espace est fermé dans un espace complet, on obtient immédiatement que le
sous-espace est complet.

L'espace $L^\infty$ des fonctions bornées sur $[0;1] \to \mathbb{R}$ avec la
norme $N_\infty$ (la borne supérieure sur $[0;1]$) est complet. En prouvant
que $\mathcal{C}^0([0;1],\mathbb{R})$ avec $N_\infty$ est fermé dedans, on
obtient que cet espace est complet. En effet, on a pour $f_n \in \mathcal{C}^0 \to f \in L^{\infty}$
$|f(x) - f(x_0)| \leq |f(x) - f_n(x_)| + |f_n(x) - f_n(x_0)| + |f_n(x)- f(x_0)|$
$\leq 2 N_\infty(f - f_n) + |f_n(x) - f_n(x_0)|$. On peut alors faire tendre
arbitrairement petitement les deux parties, la première en augmentant $n$ et la
deuxième en rapprochant $x$ de $x_0$.

## Densité
### Densités classiques
Soit $\mathcal{E}$, l'espace vectoriel des fonctions en escalier sur $[0;1]$,
$\mathcal{A}$, l'espace vectoriel des fonctions affines par morceaux sur $[0;1]$,
$\mathcal{P}$, l'espace vectoriel des fonctions polynomiales sur $[0;1]$,
le théorème de Stone-Weirstrass donne que ces deux espaces sont denses
dans $\mathcal{C}^0([0;1];\mathbb{R})$ pour $N_\infty$. Plus précisément,
$\overline{\mathcal{A}} = \overline{\mathcal{P}} = \mathcal{C}^0 \subset \overline{\mathcal{E}} = \mathcal{C}^0_m$
(les fonction continues par morceaux) pour $N_\infty$.

### Sommes de Riemann
Une somme de Riemann $S_n(f)$ est la somme $\frac{1}{n} \sum\limits_{k = 0}^{n} f(\frac{k}{n})$.
Si $f \in \mathcal{C}^0([0;1],a\mathbb{R})$, $S_n \to \int\limits_{0}^{1}  f$
(de façon générale $S_n \to \frac{1}{b - a} \int\limits_{a}^{b} f$).
Ce n'est possible que pour l'espace de départ étant un compact (on peut s'en
sortir dans tous les cas si $f$ est monotone).

Soit $x_k = \frac{k}{n}$, et $I_k = \int\limits_{x_k}^{x_{k+1}} f dt$, avec $x \in [\![0;n-1]\!]$,
et cela approche $\frac{1}{n} f(x_k)$.
$\int\limits_{x_k}^{x_{k+1}} f dt - \frac{1}{n} f(x_{k}) = \int\limits_{x_k}^{x_{k+1}} f(t) - f(x_{k}) dt$,
et $f$ est uniformément continue sur le compact $[x_k;x_{k+1}]$,
donc $\| f(x) - f(y) \| \leq \varepsilon$ si $|x - y| \leq \alpha \Rightarrow |x - y| \leq \frac{1}{n}$.
On obtient finalement que la norme de chaque $I_k - \frac{1}{n} f(x_k)$ est
majorée par $\frac{\varepsilon}{n}$, majorant l'intégrale moins la somme par $\varepsilon$
(il ne manque que $\frac{1}{n} f(1)$, qui tend vers $0$).

> Lemme de Riemann-Lebesgue : Soit $f \in \mathcal{C}^0_m$ intégrable sur un
> sous-intervalle de $[0;+\infty[$, $\hat{f}(\lambda) = \int\limits_{a}^{b} f(t) e^{i \lambda t}$
> tend vers $0$ en $+\infty$.

__Preuve :__
1. Densité : $f = 1$ sur $]\alpha;\beta[$, donc $\hat{f}(\lambda) = \int\limits_{\alpha}^{\beta} e^{i \lambda t} = O(\frac{1}{\lambda})$
   car $f \in \mathcal{E}$, et on conclut par linéarité. Dans le cas plus
   général de la fonction continue par morceaux, on peut conclure par le
   théorème interversion des limites en montrant que le $\hat{\cdot}$ de chaque
   morceau converge pour $N_\infty$ vers $\hat{f}$ par convergence uniforme.
2. Intégration par parties : On fait l'intégration par parties pour calculer
   $\hat{f}$, donnant $[\frac{e^{i \lambda t}}{\lambda} f(t)]\limits_0^\lambda - \frac{1}{\lambda} \int\limits_{0}^{1} f'(t) e^{i \lambda t} dt$,
   donnant $\hat{f}(\lambda) = O(\frac{1}{\lambda})$. On peut aussi utilise la
   densité des fonction polynomiales.
