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

Z-Score ? Lol
Monte-Carlo ? Lol
