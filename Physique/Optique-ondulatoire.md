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
$\frac{d^2 \xi_n}{dt^2} = \frac{k}{m} a^2 \frac{d^2 \xi_n}{dx^2}$.
On passe à la limite $\frac{m}{a} = \mu$, ...
