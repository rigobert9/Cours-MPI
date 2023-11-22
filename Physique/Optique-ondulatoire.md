# Introduction à l'optique ondulatoire
# Généralités sur les ondes
## Définition et classification
> Définition : Une onde est un grandeur physique intensive
> définie comme un champ spatio-temporel.$s(M,t)$

## Caractéristiques
### Ondes scalaires et vectorielles
Si $s(M,t)$ est une grandeur scalaire, on parle d'onde scalaire, et si elle est
vectorielle, on parle d'onde vectorielle.

### Onde transverse ou longitudinale
Si $s(M,t)$ crée une modification du milieu de propagation dans la direction du
sens de propagation de l'onde, on parle d'onde longitudinale. Si la
modification est perpendiculaire à la direction de propagation, on parle d'onde
transverse.

## Différents types d'ondes
### Équation de propagation
> L'équation d'onde est une équation différentielle spatio-temporelle sur $s(M,t)$
> (avec des dérivées partielles en chaque paramètre).
> On l'obtient en écrivant les lois physiques sur la grandeur qu'on étudie dans le
> milieu de propagation.

#### Exemples d'établissement de l'équation de propagation
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
et donc $\mu \frac{\partial^2 y}{\partial t^2} = T_0 \frac{\partial \tan(\alpha)}{\partial x}$.\
En outre, $\tan \alpha = \frac{y(x + dx,t) - y(x,t)}{dx} \Rightarrow \tan \alpha = \frac{\partial y}{\partial x}$
(voir géométriquement ce résultat), donnant enfin
$\mu \frac{\partial^2 y}{\partial t^2} = T_0 \frac{\partial \tan \alpha}{\partial x} = T_0 \frac{\partial^2 y}{\partial x^2}$,
soit l'équation d'onde sur $y$, $\frac{\partial^2 y}{\partial x^2} - \frac{\mu}{T_0} \frac{\partial^2 y}{\partial t^2} = 0$.

#### Exemple de l'onde sonore dans un solide
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

### Équation d'onde de D'Alembert
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

### Onde progressive
Physiquement, on interprète $f(x - ct)$ comme un signal qui se translate sans
déformation d'une distance $ct$ en un temps $t$ : c'est une onde progressive de
vitesse $c$ dans la direction des $x$ croissants. (Dans le cas de $g(x + ct)$,
c'est une onde dans la direction des $x$ décroissants.)

> Une surface d'onde est l'ensemble des points contigus qui vibre de la même
> manière. $S_\text{onde} = \{M \mid S(M,t) = \text{constante}(t)\}$.

Les modèles suivants nécessitent une énergie infinie pour maintenir leur surface
d'onde : en réalité, l'énergie nécessaire est proportionnelle au carré de la
vibration générée. En l'absence de perte, elle se répartit sur la surface.

#### Onde plane
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

#### Onde sphérique
Les ondes sphériques ont des sphères pour surfaces d'onde, soit
$s(M,t) = s(r, t) = \frac{1}{r} f(r - ct)$.

#### Onde plane sinusoïdale (harmonique, monochromatique, ...)
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

> Les surfaces telles que $\varphi(\overrightarrow{\rm r}, t) = \overrightarrow{\rm k} \cdot \overrightarrow{\rm r} - \omega t + \varphi_0$
> est de valeur constante à un instant donné sont les surfaces équiphases.

Pour une OPPM, une surface équiphase est une surface d'onde car elle est
entièrement définie par sa phase. En revanche, pour l'onde
$s(\overrightarrow{\rm r},t) = s_0 e^{- \frac{y}{\delta}} \cos(\omega t - kx)$
ce sont les plans pour lesquels $x$ est constant mais ce ne sont pas des
surfaces d'onde.

Pour une OPPM $s(x,t) = A \cos(\omega t - k x + \varphi_0)$, on peut utiliser
les complexes avec la fonction $\underline{S}(r,t) = \underline{S}(\overrightarrow{\rm r}) e^{j \omega t}$
où $\underline{S}(\overrightarrow{\rm r}) = r_0 e^{j (\overrightarrow{\rm k} \cdot \overrightarrow{\rm r}) + \varphi_0}$.

Ces grandeurs sont très pratiques pour les calculs avant de revenir à une onde
réelle en prenant la partie réelle, mais il est donc INTERDIT D'UTILISER DES
GRANDEURS QUADRATIQUES (par exemple les grandeurs énergétiques). En effet,
$\cos^2(\omega t)$ ne donne pas $\cos(2 \omega t)$.

### Ondes stationnaires
#### Définition et condition d'apparition
> Une onde stationnaire set une onde où les variables de temps et d'espace sont
> découplées, et qui s'écrit donc comme le produit d'une fonction du temps et d'un
> champ.

Une onde stationnaire dépend toujours du temps, attention à son nom. En
revanche, elle ne se propage pas au cours du temps.

Elles apparaissent principalement lorsqu'on limite la propagation d'une onde
progressive, en étudiant la superposition de l'onde et de sa reflection.

Par exemple : On envoie une OPPM $s_i$ selon les $x$ croissants depuis $x = -\infty$,
vers un obstacle tel que pour $x \geq 0$ l'onde ne peut se propager. On ajouter
la condition à la limite que $s(0,t) = 0$.\
On prouve l'existence d'une onde réfléchie par l'absurde, car s'il n'y a pas de
reflection, $s(0,t) = s_i(0,t) = s_0(x) \cos(\omega t)$, ce qui est vrai pour tout $t$
donnant $s_i = 0$ (donc pas d'onde incidente).\
Ainsi, une onde réfléchie $s_r$ existe bien. En $x = 0$, le total des deux ondes
est à $0$, et on peut déduire de la même façon que leurs pulsations sont égales,
nous permettant de déduire que $s_{0,r} = - s_{0, i}$. Les deux ondes se
déplaçant dans le même milieu, leurs $k$ sont les mêmes (car leur vitesse est la
même, comme leur $\omega$), nous donnant que $s_r(x,t) = - s_0 \cos(\omega t + k x)$
et donc que $s(x,t) = 2 s_0 \sin(k,x) \sin(\omega t)$, qui est stationnaire.

On peut d'ailleurs remarquer dans ces expressions l'existence de nœuds tous les
$\frac{p \lambda}{2}$ et de ventres.

#### Cavité résonante
Une cavité résonante est un milieu de propagation de taille fini, dans laquelle
une OPPM doit respecter une condition aux deux limites comme l'exemple précédent
: $s_\text{tot}(- L, t) = s_\text{tot}(0,t) = 0$. Ces conditions entraînent que
les seules ondes qui peuvent y exister sont de longueur d'onde de la forme $\frac{2L}{n}$.
Ainsi, seules une certaine fréquence et ses harmoniques peuvent exister.

### Vitesses liées à l'onde
On a vu que si $s(x,t) = f(x - v t)$, l'onde progressive se déplace vers les $x$
croissants à la vitesse $v$.

On peut aussi définir la vitesse de phase d'une OPPM, en sachant qu'elle est
entièrement définie par sa phase $\varphi(\overrightarrow{\rm r},t) = \overrightarrow{\rm k} \cdot \overrightarrow{\rm r} - \omega t + \varphi_0$,
faisant se déplacer la phase à la vitesse $v_\varphi = \frac{\omega}{k}$
vers les $x$ constants. Celle-ci peut parfois être supérieure à $c$
dans le calculs; encore une fois, les OPPM n'existent pas.

$k$, et donc aussi $v_\varphi$, dépendent du milieu car sa longueur d'onde dépend
du milieu. On définit l'indice optique du milieu tel que $\lambda = \frac{\lambda_0}{n}$,
permettant d'obtenir $k = n k_0$ et $v_\varphi = \frac{c}{n}$. Cet indice est
pris comme $1$ dans le vide, et supérieure à $1$ autrement.

Une conséquence de l'existence de cet indice, aussi appelé indice de réfraction,
et sa dépendance à la fréquence, rend les milieux où c'est le cas dispersifs.
Cela explique l'expérience du prisme de la couverture de "Dark side of the moon".

#### Vitesses liées aux ondes réelles
La transformée de Fourier nous monter que d'une certaine façon, les OPPM forment
une base des ondes réelles. En effet, si la source $s(O,t) = f(t)$,
alors Fourier en ce point donne $f(t) = \int\limits_{0}^{+\infty} g(\omega) \cos(\omega t) d \omega$
avec $g(\omega) d \omega$ l'amplitude de la composante $\omega$
et $g(\omega)$ sa densité spectrale. On appelle la fonction
$g(\omega)$ le spectre de $f(t)$. On rappelle que $\Delta \omega \tau \approx 2 \pi$.

Chacune de ces composantes se propage comme une OPPM, et a sa propre vitesse de
phase, qui sont les mêmes si le milieu est non dispersif. Si le milieu est
dispersif, l'onde se déforme avec l'avancée à une vitesse différente de chaque
composante.

On admet que pour un paquet d'onde (si $\Delta \omega$ n'est pas trop grand, et
est centré sur $\omega_0$), le sommet de l'enveloppe se déplace à la vitesse de
groupe $V_f = \frac{d \omega}{d k}$. On verra que $V_g$ est aussi la vitesse de
déplacement de l'énergie (et donc qu'elle est aussi inférieure à la vitesse de
la lumière). (De plus, on prouvera que $\tau$ augmente avec $\frac{d^2 \omega}{d k^2}$.)

### Caractère vectoriel d'une onde lumineuse
Les ondes lumineuses sont des ondes électromagnétiques, donc vectorielles.
On caractérise ses propriétés vectorielles par sa polarisation.

La polarisation d'une onde caractérise son aspect vectoriel : elle est liée à la
forme de la trajectoire qu'effectue la pointe du champs $\overrightarrow{\rm E}$
dans un plan perpendiculaire à la direction de propagation quand on regarde
venir l'onde vers soi.

Par exemple, on caractérise un champ électromagnétiques $\overrightarrow{\rm E}(x,t)$
$= \left\{\begin{matrix} E_y = E_{0 y} \cos(\omega t - kx) \\ E_z = E_{0 z} \cos(\omega t - k x + \varphi) \end{matrix}\right.$.
Alors, si $\varphi = 0$,la trajectoire de $\overrightarrow{\rm E}$ se fait sur
une ligne droite : on a une polarisation rectiligne. Idem pour $\varphi = \pi$
sur une autre droite. Pour $\varphi = \pm \frac{\pi}{2}$, on parle de
polarisation elliptique : la trajectoire suit une ellipse passant par les deux
autres cas, dans un sens selon le signe de $\varphi$.

La seule chose à savoir selon le programme est la suivante :
pour $\overrightarrow{\rm E} = E_0 \cos(\omega t - k x) \overrightarrow{\rm e_y}$,
$\overrightarrow{\rm E}$ est une onde plane progressive vers les $x$ croissants
à la vitesse $\frac{\omega}{k}$ polarisée rectilignement suivant $\overrightarrow{\rm e_y}$

# Rappels d'optique géométrique et lien avec l'optique ondulatoire
## Construction d'Huygens
À partir d'une surface d'onde à l'instant $t$, on construit la surface d'onde à
l'instant $t + dt$ en considérant chaque point de la surface initiale comme une
source ponctuelle secondaire qui émet des ondelettes sphériques. La surface
d'onde en $t + dt$ est l'enveloppe des ondelettes. On peut alors expliquer la
diffraction.

On peut aussi utiliser cette construction pour retrouver les lois de Descartes
(voir TD).

> Théorème de Malus : Après un nombre quelconque de réflexions et de réfractions,
> les surfaces d'onde sont localement perpendiculaires avec les rayons lumineux.

Celui-ci n'est plus valable après une diffraction, contrairement à ce que
pensait Huygens : en effet, la tache de diffraction est plus forte au centre de
la diffraction que sur les bords, montrant les limites de la construction.

### Conséquences directes
> Principe du retour inverse de la lumière (PRIL) :
> La lumière se déplace suivant le même rayon dans les deux sens.

> Dans un milieu homogène (dont l'indice optique est le même partout), les rayons
> lumineux sont rectilignes.


## Conditions de Gauss, loi de Descartes et stigmatisme
### Loi de Descartes
> Rayon incidents, réfléchis et réfractés sont tous dans un même plan (le plan
> d'incidence) perpendiculaire au dioptre.

> L'angle de réflexion $\alpha_r$ est l'opposé de l'angle d'incidence $\alpha_i$; l'angle de réfraction
> $\alpha_t$ est tel que $n_1 \sin(\alpha_i) = n_2 \sin(\alpha_t)$,
> avec $n_1$ l'indice optique du milieu du rayon incident et $n_2$ l'indice
> optique du milieu du rayon réfracté (au-delà du dioptre).

### Conditions de Gauss
> Un dispositif optique formateur d'image (comme une lentille ou un miroir)
> est dans les conditions de Gauss si les rayons incidents sont paraxiaux; c'est à
> dire faiblement éloignés de l'axe optique et faiblement inclinés par rapport à
> l'axe optique.

Pour s'assurer de se placer dans ces conditions sur un dispositif expérimental,
on place un diaphragme devant le dispositif afin de laisser passer uniquement
les rayons paraxiaux.

On peut dans ces conditions appliquer l'approximation de Gauss : on peut
supposer que le dispositif est :
- stigmatique : l'image d'un point est un point
- aplanétique : l'image d'un objet plan perpendiculaire à l'axe est un objet
  plan perpendiculaire à l'axe

La plupart des dispositifs sont stigmatiques approchés, avec le seul dispositif
vraiment stigmatique étant le miroir, ou encore le cas spécial du miroir
parabolique qui a un unique point stigmatique à l'infini.

### Lois de conjugaison
Pour une lentille de centre $O$, et un objet de point sur l'axe $A$ et de point
image $A'$, on a la relation de conjugaison de Descartes $\frac{1}{\overline{OA'}} - \frac{1}{\overline{OA}} = \frac{1}{\overline{f'}}$
avec $\overline{f'}$ la distance focale de la lentille.

Soit $F$ son foyer objet et $F'$ son foyer image, on a la relation de
conjugaison de Newton $\overline{FA} \cdot \overline{F'A'} = - \overline{f'}^2$.

Pour un miroir plan de centre $S$, on a $\overline{SA'} = - \overline{SA}$.

Pour d'autres systèmes, la loi de Descartes et les conditions de Gauss
permettent d'applique la relation de conjugaison (on pourra alors l'appliquer
par exemple sur un dioptre à la surface de l'eau, ou encore à une lentille boule).

## Le chemin optique
> On appelle chemin optique le long d'un rayon lumineux entre les points $A$ et
> $A'$ la quantité $L_{A A'} = (A A') = \int\limits_{\hat{A A'}} n ds$.

Comme on sait que $n = \frac{c}{v}$, on a $n ds = c \frac{ds}{v} = c dt_{ds}$
(c'est à dire le temps parcouru par la lumière sur $ds$), donnant
$(A A') = c \Delta t_{A A'}$, qui est une longueur proportionnelle au temps réel
de parcours. Le coefficient étant $c$, on interprète cette longueur comme la
distance qu'aurait parcouru la lumière sur le même temps de parcours. Elle nous
permettra d'étudier le décalage entre des rayons.

### Applications
#### Calcul du déphasage
Pour une onde, la phase spatiale peut s'écrire
$\varphi(\overrightarrow{\rm r}) = \overrightarrow{\rm k} \cdot \overrightarrow{\rm r} + \varphi_0$.
Ainsi, entre deux points $M$ et $M'$ espacés de $d \overrightarrow{\rm r}$,
donnant leur déphasage comme $d \varphi = \overrightarrow{\rm k} \cdot d \overrightarrow{\rm r}$.
Le long d'un rayon, $\overrightarrow{\rm k}$ est parallèle à $\overrightarrow{\rm r}$
($\overrightarrow{\rm k}$ est tangent au rayon lumineux).

Ainsi, on évalue le déphasage entre les deux points par $\varphi(M) - \varphi(S)$
$= \int\limits_{\hat{SM}} d \varphi = \int\limits_{\hat{SM}} \overrightarrow{\rm k} \cdot d \overrightarrow{\rm r}$
$= \int\limits_{\hat{SM}} \frac{2 \pi}{\lambda} ds$. Comme $\lambda = \frac{\lambda_0}{n}$,
on a $\varphi(M) - \varphi(S) = \frac{2 \pi}{\lambda_0} (SM)$. On peut ainsi
calculer facilement de déphasage entre deux points qui ont une source commune.
Attention à toujours appliquer cette formule sur des rayons !

Finalement, pour calculer les interférences en $M$
issues de rayons venant d'un même point $S$,
on a $\Delta \varphi(M) = \varphi_2(M) - \varphi_1(M) = \frac{2 \pi}{\lambda_0} ((SM)_2 - (SM)_1)$.

#### Retour sur le théorème de Malus
> Une surface d'onde est une surface de chemin optique d'égale longueur.

#### Retour sur le stigmatisme
Le stigmatisme nous assure en fait que le chemin optique de tout rayon d'un
point $A$ à son image $A'$ par une lentille est de longueur égale.

## Généralités sur la lumière
### Ondes électromagnétiques
(Voir un diagramme du spectre des ondes ELM)
