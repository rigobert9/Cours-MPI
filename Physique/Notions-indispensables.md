# Quelques notions indispensables
## Fonctions à plusieurs variables
### Définitions
En physique, on ne travaille que sur des valeurs réelles (ce qu'on mesure), sauf
en mécanique quantique ou on travaille avec des valeurs entières et des
fonctions d'onde complexes.

Une fonction de $n$ variables réelles correspond à une fonction $\mathbb{R}^{\mathbb{R}^n}$,
et on pense les fonctions prenant un vecteur de la même façon.

Selon tout problème physique, on utilise les relations connues et on en fait des
fonctions en déterminant les variables qui sont fixées et les
paramètres. Les variables sont aussi rarement indépendantes, difficulté dont on
se libère souvent par des approximations (comme par exemple l'ARQS ou les
homogénéités (iso-trucs) en thermodynamique, qui permettent de rendre les
variables d'état indépendantes de l'espace).

### Dérivée partielle
En physique, on préfère toujours la notation $\frac{d f}{dt}$ à la notation $f'$
pour son sens physique, le rappel des manipulations (un peu acrobatiques)
possibles avec et le rappel de la variable de dérivation.

Pour les fonctions de plusieurs variables, il convient de préciser la variable
de dérivation. Ainsi, $\frac{\partial f(x;y)}{\partial x}$ est la dérivée de $f$
selon $x$ en maintenant $y$ constant. On précise d'ailleurs ces paramètres
restants en cas de besoin en notant $(\frac{\partial f(x;y)}{\partial x})_y$

On utilisera (sans preuve, voir peut-être un jour le cours de maths) le théorème
de Schwarz.

> Théorème de Schwarz : Soit $f \in \mathbb{R}^{\mathbb{R}^2}$
> dont les dérivées secondes sont $\mathcal{C}^2$,
> alors $\frac{\partial^2 f(x;y)}{\partial x \partial y} = \frac{\partial^2 f(x;y)}{\partial y \partial x}$.

On considèrera souvent sans se poser trop de questions que la continuité est
présente, permettant de toujours appliquer le théorème.

### Fonctions composées
On applique la même règle de dérivée de la composition qu'en mathématiques,
traduite comme $(f(u(x)))' = f'(u(x)) \times u'(x) = \frac{d f}{du} \frac{d u}{dx}$, avec
pour $g(x;y) = f(u(x;y);v(x;y);w(x;y))$
le total bourrin $\frac{\partial g}{\partial x} = \frac{\partial f}{\partial u} \frac{\partial u}{\partial x} + \frac{\partial f}{\partial v} \frac{\partial v}{\partial x} + \frac{\partial f}{\partial w} \frac{\partial w}{\partial x}$.

### Différentielle totale
On appelle différentielle totale le différentiel
$df = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy + \frac{\partial f}{\partial z} dz$.
On exprime un beau différentiel qui s'intègre sur n'importe quel chemin d'un
point à un autre sans différence.

> Théorème : Soit $\delta \varphi(x;y;z) = P(x;y;z) dx + Q(x;y;z) dy + R(x;y;z) dz$,
> si $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$,
> $\frac{\partial P}{\partial z} = \frac{\partial R}{\partial x}$
> et $\frac{\partial Q}{\partial z} = \frac{\partial R}{\partial y}$,
> alors il existe $f$ tel que $\delta \varphi = df$ et tel que $\frac{\partial f}{\partial x} = P$, etc.

On ne vérifiera bien évidemment pratiquement jamais ces conditions, on est en
physique et on l'appliquera dès que ça semble avoir du sens.
Typiquement, on l'applique pour trouver si une force est conservative dans
$\delta W = \overrightarrow{\rm F} \cdot d \overrightarrow{\rm OM}$
(en testant pour $F_x dx$ et tous les autres).

Pour retrouver $f$ (le potentiel) une fois le théorème applique, il faudra soit
intégrer sur un chemin de $O$ à $M$ (n'importe lequel puisque la force est
conservative), ou bien on intègre successivement $P$, $Q$ et $R$.

## Mesures physiques
### Généralités
Soit $X$ une grandeur physique, dont on obtient $x$ la mesure avec une unité
identique aux autres grandeurs comparées; on note $X = x$.
On note en général autant de chiffres qu'il y a de chiffres significatifs (même
si ce sont des $0$), par exemple $2,0 m$ pour $2$ mètres au décimètre près.
On peut même rigoureusement interpréter $\ell = 2,0 m$ comme $\ell \in [1,95 m; 2,05 m[$.

### Équations de dimension
On mesure $7$ grandeurs physiques différentes (toutes les autres grandeurs se
dérivant de celles-ci). Un système de mesure se compose donc de $7$ constantes
"formant une base" qui constituent les unités (cube eau, fraction de la taille
de la Terre puis fraction de la vitesse de la lumière, fraction d'une année
puis oscillations entre états superfins pour le système métrique; vitesse de la
lumière et constante gravitationnelle pour les unités de Planck).

On ne peut additionner que deux valeurs homogènes (de même dimension), et la
dimension du produit de deux grandeurs est le produit de leur dimension (avec la
dérivation agissant comme une division et l'intégrale agissant comme un
produit). Seules deux grandeurs de même dimension peuvent être égales. Vérifier
l'homogénéité d'une formule permet souvent de se prémunir contre une erreur.

### Incertitudes
Les concours s'intéressent de plus en plus à la précision et à la métrologie,
fondamentale dans le travail scientifique. Le programme est même assez lourd
dessus.

#### Ordre de grandeurs
Soit $X$ une grandeur, $x$ sa mesure, on note l'incertitude absolue $\Delta x$
si $x - \Delta x < X < x + \Delta x$.

L'incertitude relative correspond à la grandeur $\frac{\Delta x}{X}$, qui évalue
la qualité de la mesure en étant petite.

On écrit donc les résultats sous la forme $x + \Delta x$, avec la précision de
$x$ et de $\Delta x$ avec autant de chiffres, et $\Delta x$ d'au plus deux
chiffres significatifs (sinon c'est ridicule d'avoir autant d'assurance sur
l'erreur sans pouvoir mieux mesurer).

> Lorsqu'on ne connaît pas $\Delta x$ (calculs théoriques), on suppose que $\Delta x \approx \frac{1}{2}$
> de la dernière unité des données, menant à la règle d'avoir un résultat avec le
> même nombre de chiffres significatifs.

#### Erreurs
##### Erreurs systématiques
Une erreur systématique est une erreur induite par un dysfonctionnement de
l'appareil (une balance avec un mauvais zéro), ou une faute de mesure (ne pas se
mettre face au ménisque d'un fluide).

##### Erreur de méthode
Plusieurs méthode peuvent exister, surtout lorsque les appareils de mesure
peuvent influer sur la mesure (en électricité typiquement). Par exemple, dans la
mesure de la résistance d'une résistance à partir de sa tension et de l'intensité,
placer le voltmètre en dérivation de la résistance seule (ce qui fait que
l'ampèremètre mesure l'intensité dedans, donnant $R_\text{mes} = \frac{U_\text{mes}}{I_m} = \frac{U}{I + I_V}$
$= \frac{U}{I + \frac{U}{R_V}} = \frac{R}{1 + \frac{R}{R_V}}$, donnant $\frac{\Delta R}{R} = \frac{R}{R + R_V}$)
donne une mesure plus précise d'autant que $R$ est petite, et
placer le voltmètre en dérivation de la résistance et de l'ampèremètre
(ce qui mesure la tension aux bornes de l'ampèremètre, donnant $R_m = \frac{U_A + U}{I} = R_A + R$,
soit $\frac{\Delta R}{R} = \frac{R_A}{R}$) est d'autant plus efficace que $R$
est grand.

##### Choix du calibre de l'appareil
Le calibre d'un appareil est la valeur maximum mesurable. Il faut toujours
commencer en utilisant le plus grand, puis un par un descendre au plus petit
calibre possible.

#### Évaluation de la propagation des variations
##### Méthode de la dérivée logarithmique
On peut souvent utiliser la méthode facile et puissante de la dérivée
logarithmique, qui permet de dire que $G = X^{\alpha} Y^{\beta} Z^{\gamma}$
$\Rightarrow \ln(g) = \alpha \ln(x) + \beta \ln(y) + \gamma \ln(z)$
$\Rightarrow \frac{dg}{g} = \alpha \frac{dx}{x} + \beta \frac{dy}{y} + \gamma \frac{dz}{z}$,
donnant enfin $\frac{\Delta g}{g} \leq |\alpha| \frac{\Delta x}{|x|} + |\beta| \frac{\Delta y}{|y|} + |\gamma| \frac{\Delta z}{|z|}$.
C'est une méthode qui se généralise en majorant $\Delta g$ par
$|\frac{\partial f}{\partial x}| \Delta x + |\frac{\partial f}{\partial y}| \Delta y + \ldots$.
Cette formule est tombée en disgrâce puisque les concours veulent souvent plus
précis, mais elle est très rapide et efficace, et donne une bonne idée de
l'ordre de grandeur.

##### Variabilité et incertitude type
C'est la méthode qui est au programme, et donne des résultats scientifiques
lorsqu'on fait des expériences. On mesure $X$ d'une certaine méthode avec un
certain instrument de mesure ... de l'exacte même façon $n$ fois, donnant
les résultats $(x_i)_{[\![1;n]\!]}$. On définit $\overline{x}$ la moyenne des
$x_i$ et $u(x) = \sqrt{\frac{\sum(x_i - \overline{x})^2}{n}}$ l'écart type des
$x_i$. On présente alors le résultat sous la forme $X = \overline{x} + u(x)$.
Il s'agit de l'incertitude de type A.

Il faut aussi connaître l'écart normalisé entre deux mesures différentes de la
même grandeur, $E_{1,2} = \frac{|\overline{x_1} - \overline{x_2}|}{\sqrt{u_1(x)^2 + u_2(x)^2}}$.
Si $E_{1,2} \leq 2$, on dit que les deux mesures sont compatibles.

Dans le cas où il n'y a pas de variabilité dans la mesure, on évalue les
incertitudes (type B) à partir de la précision de la méthode et de l'appareil.

On a l'incertitude de $G = \alpha X + \beta Y$ qui est
$u(g) = \sqrt{(\alpha u(x))^2 + (\beta v(y))^2}$,
et celle de $G = X^{\alpha} Y^{\beta}$ qui est
$\frac{u(g)}{g} = \sqrt{(\alpha \frac{u(x)}{x})^2 + (\beta \frac{u(y)}{y})^2}$.

## Équations différentielle linéaires
### Généralités
#### Définition
Une EDL d'ordre $n$ s'écrit sous la forme $\sum\limits_{k = 0}^{n} a_k(x) \frac{d^k y}{dx^k} = C(x)$.
La plupart du temps on étudiera des EDL dont les coefficients $a_k$ est
constant (sans quoi ça se complique beaucoup). On appelle une équation
différentielle non linéaire si elle présente des puissances de dérivées ou des
puissances de la fonction qu'on recherche.

#### Théorème
Les solutions d'une EDL sont la somme d'une solution de
l'équation homogène ($C(x) = 0$) et d'une solution particulière. De plus, pour
$C(x) = C_1(x) + C_2(x)$, on peut décomposer le problème en une recherche de
$y_1(x)$ et $y_2(x)$.

La solution de l'équation homogène, pour une équation différentielle
d'ordre $n$, possède $n$ constantes d'intégration. On détermine les constantes
d'intégration à partir des conditions initiales du problème. Ces constante sont
déterminées sur la solution totale (et pas la solution homogène). On tiendra à
bien justifier ces conditions initiales.

La solution homogène correspond au régime libre ou au régime transitoire du
système. La solution particulière correspond au régime forcé ou permanent
(stationnaire veut dire indépendant du temps, permanent signifie une fois que le
régime transitoire est terminé (au bout de quelques $\tau$)).

### Équations d'ordre 1
#### Cas général
$a_1(x) \frac{d y}{dx} + a_0(x) y = 0 \Rightarrow \frac{dy}{y} = - \frac{a_0(x)}{a_1(x)} dx$
$\Rightarrow \ln(y) = \int - \frac{a_0(x)}{a_1(x)} dx + C$,
donnant $y = e^{\int - \frac{a_0(x)}{a_1(x)} dx + C} = \lambda e^{\int - \frac{a_0(x)}{a_1(x)} dx}$.

#### Cas particuliers à connaître
$a \frac{d y}{dx} + by = 0 \Rightarrow y = A e^{\frac{-b}{a} x}$\\
Pour que $y$ ne diverge pas, il faut $a$ et $b$ de même signe.
Lorsque $y$ diverge, soit la solution n'a pas de sens physique, ou que le
système s'éloigne de la position initiale et sort tout à coup de la
modélisation (par exemple, une hypothèse d'élasticité infinie d'un ressort,
qui en réalité va casser).

### Équations d'ordre 2
$a_2 \frac{d^2 y}{dx^2} + a_1 \frac{d y}{dx} + a_0 y = 0$\\
$\Delta = a_1^2 - 4 a_2 a_0$.

Pour $\Delta$ positif, on a $y = A e^{r_1 x} + B e^{r_2 x}$,
pour $\Delta = 0$ on a  $(A + Bx) e^{r_0 x}$, et pour
$\Delta$ négatif, on a $y = e^{\frac{-a_1}{a_2} x} (A \cos(\frac{\sqrt{- \Delta}}{2 a_2} x) + B \sin(\frac{\sqrt{- \Delta}}{2 a_2} x))$
$= C e^{\frac{-a_1}{a_2} x} (\cos(\frac{\sqrt{-\Delta}}{2 a_2}) + \Phi)$.

Ainsi, pour que $y(x)$ converge, il faut que $a_2, a_1$ et $a_0$ soient de même
signe.

## Repères, déplacements, surfaces, et volumes élémentaires
### Systèmes de coordonnées
#### Repère cartésien
On se repère avec une origine et trois vecteurs formant une base orthonormée
directe; on repère donc les points par trois valeurs (des facteurs de scaling
des vecteurs de base).

#### Repère cylindrique
On repère dans le repère cartésien les points par une longueur radiale (la
distance $OH$ pour le point $M$, dont $H$ est le projeté à $z = 0$), et $\theta$
est l'angle algébrique (en général dans le sens positif, mais attention !) entre
l'une des lignes engendrées par une base. On prend ainsi $\overrightarrow{\rm
e_\theta}$ un vecteur unité orienté dans le sens de l'angle $\theta$ et placé
tangent au cercle de rayon $r$. $z$ est simplement l'axe $z$ du repère
cartésien.

$\theta$ varie de $0$ à $2 \pi$ (le tour du cylindre).

#### Repère sphérique
On repère un point du repère cartésien par sa longueur radiale $r = OM$
pour un point $M$, $\varphi$ l'angle (comme $\theta$ en cylindrique),
et $\theta$ l'angle entre l'axe $z$ et $OM$. Les vecteurs
$\overrightarrow{\rm e_\varphi}$ et $\overrightarrow{\rm e_\theta}$ sont
orientés dans le sens de variation de l'angle.

Ici, $\theta$ varie de $0$ à $\pi$ (du pôle nord au pôle sud, sinon on parcourt
deux fois la sphère), et $\varphi$ de $0$ à $2 \pi$.

#### Repère de Frenet
On connait la trajectoire du point qu'on étudie, avec $s$ l'abscisse curviligne
du point $M$. On définit alors le vecteur $\overrightarrow{\rm u_t}$ tangent à
la courbe et le vecteur $\overrightarrow{\rm u_n}$ orthogonal pointant vers le
centre de courbure de la courbe.

### Déplacements, surfaces et volumes élémentaires
#### Déplacements
Un déplacement $ds$ est un petit déplacement de $M$ à $M'$ très proche.
- Dans le repère cartésien, on a $ds = \sqrt{dx^2 + dy^2 + dz^2}$.
- Dans le repère cylindrique, on a $ds = \sqrt{dr^2 + (r d \theta)^2 + dz^2}$.
- Dans le repère sphérique, on a $ds = \sqrt{dr^2 + (r d \theta)^2 + (r \sin(\theta) d \varphi)^2}$.
- Dans le repère de Frenet, CHERCHER.

#### Surfaces élémentaires
- Dans le repère cartésien, on prend $dx dy$, $dy dz$ ou $dz dx$.
- Dans le repère cylindrique, on prend $dr \times r d\theta$, $dr dz$ ou $r d\theta \times  dz$.
- Dans le repère sphérique, on prend $dr \times r d\theta$, $dr \times r \sin(\theta) d\varphi$ ou $r d\theta \times r \sin(\theta) d\varphi$.
- Dans le repère de Frenet, CHERCHER.

#### Volumes élémentaires
- Dans le repère cartésien, on prend $dx dy dz$.
- Dans le repère cylindrique, on prend $dr \times r d\theta \times dz$.
- Dans le repère sphérique, on prend $dr \times r d\theta \times r \sin(\theta) d\varphi$.
- Dans le repère de Frenet, CHERCHER.

#### Quelques surfaces et volumes élémentaires à connaître
La largeur d'un ruban de largeur $dr$ à partir de $r$ est de $2 \pi r dr$.
L'aire d'un ruban sur une sphère est de $2 \pi r \sin(\theta) \times r d\theta$.
Le volume de la coquille sphérique entre $r$ et $r + dr$
est de $4 \pi r^2 dr$.

Chercher la surface ou le volume le plus grand possible permet de repérer les
symétries du problème et de faciliter le calcul.

## Opérations sur les champs
### Différents types de champs
Un champ scalaire est une fonction associant une grandeur à un point de
l'espace, dépendant du temps. De même, un champ vectoriel renvoie un vecteur.
Au lieu de lier le temps à la position comme en mécanique, ces variables sont
indépendantes.

### Topographie
Pour représenter un champ scalaire, on représente les surfaces équi-$\varphi$
(donc des surfaces paramétrisées par $\varphi(x,y,z,t = c) = \text{constante}$)
(lignes de niveau ou représentation du champ magnétique).
Pour représenter un champ vectoriel, on trace les lignes de champ, les courbes
tangentes en tout point au champ $\overrightarrow{\rm A}(M,t)$ orienté suivant
le sens de $\overrightarrow{\rm A}$. Mathématiquement, cela correspond aux
courbes telles que $\overrightarrow{\rm A}(M) \wedge d\overrightarrow{\rm \ell}(M) = \overrightarrow{\rm 0}$.

### Dérivation spatiale
On veut étudier des opérateurs de dérivation spatiale lié à $\frac{\partial}{\partial x}$,
$\frac{\partial}{\partial y}$ et $\frac{\partial}{\partial z}$, mais qui soit
indépendant du choix de repère.

Il peut être montré qu'il n'existe que trois de ces opérateurs, tous notés avec
l'opérateur Nabla $\overrightarrow{\rm \nabla} = \left|\begin{matrix} \frac{\partial}{\partial x} \\ \frac{\partial}{\partial y} \\ \frac{\partial}{\partial z} \end{matrix}\right.$.
Ils sont $\overrightarrow{\rm \nabla} \varphi$ (le gradian),
$\overrightarrow{\rm \nabla} \wedge \overrightarrow{\rm A}$ (le rotationnel)
et $\overrightarrow{\rm \nabla} \cdot \overrightarrow{\rm A}$ (la divergence).
On peut dériver comme d'habitude pour les autres repères.

### Définition par les propriétés
Le gradient est tel que $\int_{\overline{AB}} \overrightarrow{\rm \text{grad}} \varphi \cdot d \overrightarrow{\rm \ell} = \varphi(B) - \varphi(A)$
(ce qu'on peut voir dans la formule en paramétrisant le chemin).

Ainsi, une intégrale fermée du gradian produit scalaire le déplacement
élémentaire est nulle. Le gradian est de plus perpendiculaire aux surfaces
équi-$\varphi$ (en intégrant le chemin dessus).

La divergence est caractérisée par le théorème d'Ostrogradski :
$\bigcirc \! \! \! \! \! \! \! \iint_S \overrightarrow{\rm A} \cdot d \overrightarrow{\rm S} = \iiint_S \text{div} \overrightarrow{\rm A} d\tau$
(sur la surface fermée définissant le volume fermé).

Le rotationnel est caractérisé par le théorème de Stokes : $\iint_{S} \overrightarrow{\rm \text{rot}} \overrightarrow{\rm A} d\overrightarrow{\rm S} = \oint \overrightarrow{\rm A} d \overrightarrow{\rm l}$
sur la surfacé définie par un contour et un contour fermé. Il faut toujours
faire attention à orienter le contour.

### Opérateurs du second ordre
En appliquant une seconde fois Nabla de l'une des façons possibles.
On peut calculer le divergent ou rotationnel du gradian, le gradian du
divergent, ou encore le rotationnel du rotationnel.

On a des cas particuliers : le rotationnel du gradian est nul, et la divergence
du rotationnel est nulle.

On appelle Laplacien la divergence du gradian, noté $\nabla^2 \varphi$
ou $\Delta \Phi$ (un divergent avec des dérivées secondes).
Enfin, le rotationnel du rotationnel est égal au gradian du divergent
moins le laplacien : $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm \text{rot}} \overrightarrow{\rm A} = \overrightarrow{\rm \text{grad}}(\overrightarrow{\rm \text{div}} \overrightarrow{\rm A}) - \Delta \overrightarrow{\rm A}$.
