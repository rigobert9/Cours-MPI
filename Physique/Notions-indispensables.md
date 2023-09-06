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
> alors $\frac{\partial^2 f(x;y)}{\partial x \partial y} = \frac{\partial^2 f(x;y)}{\partialyx \partial x}$.

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
dimension du produit de deux grandeurs est le produit de leur dimension.
