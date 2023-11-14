## Introduction à l'optique ondulatoire
## Généralité sur les ondes
### Définition et classification
> Définition : Une onde est un grandeur physique intensive
> définie comme un champ spatio-temporel.$s(M,t)$

### Caractéristiques
#### Ondes scalaires et vectorielles
Si $s(M,t)$ est une grandeur scalaire, on parle d'onde scalaire, et si elle est
vectorielle, on parle d'onde vectorielle.

#### Onde transverse ou longitudinale
Si $s(M,t)$ crée une modification du milieu de propagation dans la direction du
sens de propagation de l'onde, on parle d'onde longitudinale. Si la
modification est perpendiculaire à la direction de propagation, on parle d'onde
transverse.

### Différents types d'ondes
#### Équation de propagation
> L'équation d'onde est une équation différentielle spatio-temporelle sur $s(M,t)$
> (avec des dérivées partielles en chaque paramètre).
> On l'obtient en écrivant les lois physiques sur la grandeur qu'on étudie dans le
> milieu de propagation.

##### Exemples d'établissement de l'équation de propagation
On modélise l'oscillation d'une corde, qui à l'équilibre est tendue à
l'horizontale. On étudie la propagation d'un déplacement transversal le long
de la corde, $\overrightarrow{\rm M_0 M} = y(x,t) \overrightarrow{\rm e_y}$.
La corde est supposée souple (donc $\overrightarrow{\rm T} = T(x, t) \overrightarrow{\rm u}$, $\overrightarrow{\rm u}$
étant tangent à la corde, et $\overrightarrow{\rm T}$ étant l'action de la
partie après le point sur la partie avant).\
On applique alors le principe fondamental de la dynamique sur $dx$ de la corde :
$\mu dx \overrightarrow{\rm a}(M(x + \frac{dx}{2})) = \overrightarrow{\rm T}(x + dx,t)$
$- \overrightarrow{\rm T}(x,t) + \mu dx \overrightarrow{\rm g}$, avec $\mu$ la
masse linéïque de la corde, supposée homogène. On supposera la poids
négligeable. En projetant, on obtient $0$ en $\overrightarrow{\rm e_x}$
au premier ordre et sur $\overrightarrow{\rm e_y}$ la valeur
$\mu dx \frac{\partial^2}{\partial t^2} (y(x + \frac{dx}{2}, t))$.\
On obtient ainsi $0 = \frac{\partial}{\partial x} (T \cos(\alpha)) dx$
$\Rightarrow T \cos \alpha = T_0$ (constant), et
$\mu dx \frac{\partial^2}{\partial t^2} (y(x + \frac{dx}{2}, t)) = T_0 \tan \alpha(x + dx,t) - T_0 \tan \alpha(x,t)$.\
Le premier élément, avec un développement de Taylor au premier ordre,
donne $\mu \frac{\partial^2 y}{\partial t^2}(x,t) dx = T_0 \frac{\partial}{\partial x}(\tan(\alpha(x,t))) dx$
et donc $\mu \frac{\partialsr y}{\partial t^2} = T_0 \frac{\partial \tan(\alpha)}{\partial x}$.\
En outre, $\tan \alpha = \frac{y(x + dx,t) - y(x,t)}{dx} \Rightarrow \tan \alpha = \frac{\partial y}{\partial x}$
(voir géométriquement ce résultat), donnant enfin
$\mu \frac{\partial^2 y}{\partial t^2} = T_0 \frac{\partial \tan \alpha}{\partial x} = T_0 \frac{\partial^2 y}{\partial x^2}$,
soit l'équation d'onde sur $y$, $\frac{\partial^2 y}{\partial x^2} - \frac{\mu}{T_0} \frac{\partial^2 y}{\partial t^2} = 0$.

##### Exemple 2
Pour modéliser une onde sonore dans un solide, on prend les atomes du solide,
qui sont régulièrement espacés de $a$ et dont l'intéraction est modélisée par des
ressorts. Soit $\xi_n(t)$ le mouvement du $n$-ième atome en fonction du temps,
suivant $\overrightarrow{\rm e_x}$, on a $m \frac{d^2 \xi_n(t)}{dt^2} = T_{n-1 \to n} + T_{n + 1 \to n}$.
$= -k((a + \xi_n - \xi_{n + 1}) - a) + k ((a + \xi_{n - 1} - \xi_n) - a)$.\
On obtient enfin $m \frac{d^2 \xi_n}{dt^2} = k (\xi_{n + 1} + \xi_{n - 1} - 2 \xi_n)$.\
Si $a$ est petit devant la distance caractéristique du problème (ici d'environ
$10^{-2} mm$), on peut prendre une variable continue $\xi(x,t)$ qui caractérise
le milieu comme continu, et on pourrait alors interpréter
$\xi_{n + 1} + \xi_{n - 1} - 2 \xi_n$ comme $\frac{d^2 \xi}{dx^2} a^2$
par la méthode d'Euler. On peut dériver plus proprement quelque chose de
similaire avec Taylor. La relation de récurrence devient alors
$\frac{d^2 \xi_n}{dt^2} = \frac{k}{m} a^2 \frac{d^2 \xi_n}{dx^2}$.\
On passe à la limite $\frac{m}{a} = \mu$, et comme $k \ell_0$ est une constante,
on considère qu'elle est égale à $ka = E$ l'élasticité du milieu, donnant une
équation continue sur tout le solide $\frac{\partial^2 \xi}{\partial x^2} + \frac{\mu}{E} \frac{\partial^2 \xi}{\partial t^2} = 0$.

Ces deux derniers exemples donnent des équations très similaires : c'est
l'équation décrivant les ondes de petite amplitude sans absorbance du phénomène
(pas d'atténuation). On a de plus fait les approximations et calculs nécessaires
pour ramener les équations aux paramètres de l'espace ambiant.

#### Équation d'onde de D'Alembert
Dans de nombreux cas, sans pertes, de propagation unidirectionnelle et où les
oscillations sont de faible amplitude, on obtient une équation d'onde de la
forme $\frac{\partial^2 s}{\partial x^2} - \frac{1}{c^2} \frac{\partial^2 s}{\partial t^2} = 0$,
avec $c$ une constante homogène à une vitesse.

Résolution (hors programme) : Soit $s(x,t) = (u(x,t),v(x,t))$,
avec $u(x,t) = x - ct$, et $v(x,t) = x + ct$,
donc $\frac{d s}{dx} = \frac{d s}{du} \frac{d u}{dx} + \frac{d s}{dv} \frac{d v}{dx}$
$= \frac{d s}{du} \times 1 + \frac{d s}{dv} \times 1$,
donnant $\frac{\partial^2 s}{\partial x^2} = \frac{\partial^2 s}{\partial u^2} + 2 \frac{\partial^2 s}{\partial v \partial u} + \frac{\partial^2 s}{\partial v^2}$.
De même, $\frac{\partial^2 s}{\partial t^2} = c^2 (\frac{\partial^2 s}{\partial u^2} - 2 \frac{\partial^2 s}{\partial v \partial u} + \frac{\partial^2 s}{\partial v^2})$.
En appliquant Schwarz, on a $\frac{\partial^2 s}{\partial x^2} - \frac{1}{c^2} \frac{\partial^2 s}{\partial t^2} = 0$
et donc $4 \frac{\partial^2 s}{\partial u \partial v} = 0$, donc $\frac{\partial s}{\partial v}$
est une constante $\alpha(v)$ par rapport à $u$, donnant
$s(u,v) = \int \alpha(v) dv + \int \beta(u) du = f(u) + g(v)$,
donnant pour solution finale $s(x,t) = f(x - ct) + g(x + ct)$ avec
$f$ et $g$ quelconques.

#### Onde progressive
Physiquement, on interprète $f(x - ct)$ comme un signal qui se translate sans
déformation d'une distance $ct$ en un temps $t$ : c'est une onde progressive de
vitesse $c$ dans la direction des $x$ croissants. (Dans le cas de $g(x + ct)$,
c'est une onde dans la direction des $x$ décroissants.)

> Une surface d'onde est l'ensemble des points contigus qui vibre de la même
> manière. $S_\text{onde} = \{M \mid S(M,t) = \text{constante}(t)\}$.

Les modèles suivants nécessitent une énergie infinie pour maintenir leur surface
d'onde : en réalité, l'énergie nécessaire est proportionnelle au carré de la
vibration générée. En l'absence de perte, elle se répartit sur la surface.

##### Onde plane
Une onde plane a pour surfaces d'ondes des plans. On caractérise les plans par
une composante connexe de la classe d'équivalence pour la valeur du produit
scalaire du vecteur normal au plan. L'équation d'onde s'écrit alors
$s(M,t) = f(\overrightarrow{\rm OM} \cdot \overrightarrow{\rm u} - ct)$ :
elle se déplace dans la direction et dans le sens de $\overrightarrow{\rm u}$.
Une vraie onde plane ne peut pas exister car elle nécessiterait une énergie
infinie, mais elles sont simples à modéliser et sont une bonne approximation
locale d'ondes réelles.\
Ces ondes planaires sont en fait les solutions de l'équation d'Alembert en trois
dimensions : $\Delta s - \frac{1}{c^2} \frac{\partial^2 s}{\partial t^2} = 0$,
qu'on ramène au vecteur normal.

##### Onde sphérique
Les ondes sphériques ont des sphères pour surfaces d'onde, soit
$s(M,t) = s(r, t) = \frac{1}{r} f(r - ct)$.

##### Onde plane sinusoïdale (harmonique, monochromatique, ...)
C'est une onde $s(M,t) = s_0 \cos(\overrightarrow{\rm k} \cdot \overrightarrow{\rm r} - \omega t + \varphi_0)$.
On appelle $s_0$ l'amplitude, et le reste est uniquement déterminé par la phase,
qui comprend le déphasage $\varphi_0$, la phase spatiale
$\overrightarrow{\rm k} \cdot \overrightarrow{\rm r}$ et
$- \omega t$ la phase temporelle, avec $\omega$ la pulsation de l'onde.
On appelle $\overrightarrow{\rm k}$ le vecteur d'onde.

On retrouve les mêmes résultats sur les ondes que l'année précédente :
$\lambda$ est la longueur d'onde, $k$ lorsqu'il est unidimensionnel est la
pulsation spatiale de valeur $\frac{2 \pi}{\lambda}$. Pour $T$ la période
temporelle ou $f / \nu = \frac{1}{T}$ la fréquence, on a $\omega = \frac{2 \pi}{T}$.
Enfin, la vitesse de l'onde est $c = \frac{\omega}{k} = \frac{\lambda}{T}$.
De plus, celle-ci dépendant du milieu et $T$ dépendant uniquement de la
source (qui impose l'oscillation), le milieu fait varier $\lambda$
et $k$ (qui sont donc caractéristique d'une onde dans un certain milieu, et pas
un invariant de l'onde). On définit donc l'indice de réfraction $n$
comme ayant la valeur $\frac{\lambda_\text{vide}}{\lambda}$.
