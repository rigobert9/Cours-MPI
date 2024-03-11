# Transfert thermique
On distingue trois modes de transferts thermiques :
- Par diffusion (conduction) thermique, lié à l'agitation microscopique de
  proche en proche
- Par convection lié à déplacement macroscopique de matière (comme un fluide
  réfrigérant; beaucoup plus rapide !)
- Par rayonnement thermique, à cause de l'émission d'ondes électromagnétiques

## Rayonnement thermique
### Définitions et modèle du corps noir
#### Définition
On note le flux thermique (puissance thermique à travers une surface)
$\Phi_\text{Th} = P_\text{th} = \frac{\delta \overline{Q_\text{Th}}(\overrightarrow{\rm S})}{dt}$.
On utilise aussi la densité surfacique de flux $\varphi_\text{Th}$, la grandeur
telle que $d \Phi_\text{Th}(d \overrightarrow{\rm S}) = \varphi_\text{Th} \cdot d S$.

Pour un matériau opaque, on note $\varphi_i$, $\varphi_r$, $\varphi_s$ le
densités de flux incident, réfléchie, et absorbée par le matériau. Par
conservation de l'énergie $\Phi_i = \Phi_r + \Phi_a$ et donc
$\varphi_i = \varphi_r + \varphi_a$. D'autre part, tout corps à la température
$T$ émet de l'énergie électromagnétique $\varphi_e$. On peut remarquer qu'à
l'équilibre thermodynamique, la première loi de la thermodynamique nous donne
$\varphi_e = \varphi_a$.

#### Modèle de corps noir
> Un corps noir est tel que $\varphi_r = 0 \Rightarrow \varphi_i = \varphi_a$. Le
> corps noir absorbe donc tous les rayonnement incidents.

#### Cas général
On ramène le modèle des corps réels à celui du corps noir à à condition de
définir un coefficient de réflexion appellé Albedo (noté $A$) tel que
$\varphi_r = A \varphi_i$ et $\varphi_a = (1 - A) \varphi_i$. Si on veut être
plus précis et étudier un corps plus complexe (qui a une couleur plutôt qu'un
niveau de réflexion), on définit $A(\lambda)$, et donc une densité spectrale de
flux telle que $d \varphi = g(\lambda) d \lambda$, $d \varphi_e = g_i(\lambda) d \lambda$,
$d \varphi_r = g_r(\lambda) d \lambda$, $d \varphi_a = g_a(\lambda) d \lambda$
et avec par conservation de l'énergie $g_e(\lambda) = g_r(\lambda) + g_a(\lambda)$.

### Propriétés du rayonnement du corps noir
#### Spectre du rayonnement du corps noir
Soit un corps noir qu'on "chauffe à blanc", le spectre classique obtenu est une
courbe de $g_e(\lambda)$ montante de façon complexe jusqu'à $\lambda_\text{max}$
avant d'être décroissance linéairement en $\frac{1}{\lambda^4}$ (de la même
façon que la diffusion de Rayleigh).

#### Propriétés
> __Loi de déplacement de Wien :__ $\lambda_{\text{max}} T \approx 3000 \mu m \cdot K$.

> __Loi de Stefan :__ $\varphi_e = \int\limits_{0}^{+\infty} g_e(\lambda) d \lambda = \sigma T^4$

> __98 % de l'énergie émise est entre $\frac{\lambda_\text{max}}{2}$ et $8 \lambda_\text{max}$ :__
> $\int\limits_{\frac{\lambda_\text{max}}{2}}^{8 \lambda_\text{max}} g_e(\lambda) d \lambda = 0,98 \times \sigma T^4$

## Conduction (diffusion) thermique
### Modélisation
#### Flux thermique
On étudie $\Phi_\text{Th Cond}$, et on introduit le vecteur densité de courant
de chaleur $\overrightarrow{\rm j_\text{Th Cond}}$ qui est tel que
que $\Phi_\text{Th}(\overrightarrow{\rm S}) = \iint_S \overrightarrow{\rm j_\text{Th}} \cdot d \overrightarrow{\rm S}$.
$\Phi_\text{Th}$ étant en Watts, $\overrightarrow{\rm j_\text{Th}}$ est en $W \cdot m^{-2}$.

#### Loi de Fourier
On obtient une loi phénoménologique, dépendant d'une constante $\lambda$ propre
à un matériau, sa conductivité thermique, en $W \cdot m^{-1} \cdot K^{-1}$
de dimension $M L T^{-3} \theta^{-1}$.

> __Loi de Fourier :__ $\overrightarrow{\rm j_\text{Th}} = - \lambda \overrightarrow{\rm \text{grad}} T$

Cette loi ne se vérifie la plupart du temps que pour des variations de $T$ pas
trop grandes (sans quoi $\overrightarrow{\rm j}$ dépend de puissances de ce
gradient, entre autres) et dans des milieu linéaires. On peut éventuellement
s'aventurer à généraliser à un $\lambda(T)$ dans un milieu non linéaire homogène
isotrope.

#### Ordres de grandeur de $\lambda$
Métaux à $0$ degrés Celsius :

Ag | Cu | Fe | Pt | Inox
---|----|----|----|-----
418|390|82|69|14

Liquides à $20$ degrés Celsius :

Eau | Alcool | Huile
---|---|---
0,10 | 0,17 | 0,13

Matériaux :

Bois | Verre | Laine de verre
---|---|---
0.2|1|0.03

#### Analogie entre la loi de Fourier et la loi d'Ohm
On peut très facilement former cette analogie, reliant
$T$ et $V$, $\lambda$ et $\gamma$, et le flux thermique avec le courant.

### Équation de conduction
#### Cas basique : unidirectionnel sans source
Soit un barreau cylindrique d'axe $(Ox)$, de section $S$ isolé transversalement.
On fait d'abord une analyse du problème (symétries et invariances). On suppose
que $T$ est invariant sur une section $S$

> Pour trouver l'équation de conduction thermique (une équation différentielle
> sur $T(x,t)$), on applique le premier principe de la thermodynamique à un
> système élémentaire de la géométrie du problème.

Dans cet exercice, on applique le premier principe à une tranche du barreau.
$d( \delta U ) = \delta W + \delta Q = 0 + \delta Q_A$ (car il s'agit d'une PCII)\
$d( \delta U ) = \delta Q(x) + \delta Q(x + dx)$\
$= \Phi_\text{Th}(S(x) \overrightarrow{\rm e_x}) dt + \Phi_\text{Th}(S(x + dx) (- \overrightarrow{\rm e_x})) dt$\
$= (j_\text{Th}(x) S - j_\text{Th}(x + dx) S) dt$\
On a ainsi $\frac{d \delta U}{dt} = (j_\text{Th}(x) - j_\text{Th}(x + dx)) S$,
donc $\delta m c \frac{\partial T}{\partial t} = - \frac{\partial j_\text{Th}}{\partial x} dx S$.
En supposant que la température est la même dans le volume élémentaire (donc que
$T(x + dx,t) = T(x,t)$), donnant $\rho S dx c \frac{\partial T}{\partial t} = \frac{\partial}{\partial x} (\lambda \frac{\partial T}{\partial x}) dx S$,
soit finalement si $\lambda$ est une constante, on a $\rho c \frac{\partial T}{\partial t} = \lambda \frac{\partial^2 T}{\partial x^2}$.

#### Étude générale
Soit un volume $V$ dans une surface fermée $S_G$, l'application du premier principe
entre $t$ et $t + dt$ nous donne, étant vraie pour tout volume, que
$\rho c \frac{\partial T}{\partial t} = - \text{div} \overrightarrow{\rm j_\text{Th}} + p_V$
et donc $\rho c \frac{\partial T}{\partial t} = \lambda \Delta T + p_V$

### Résolution de l'équation de diffusion en régime stationnaire
#### Conservation de $\Phi_A$
En régime stationnaire, $\frac{\partial T}{\partial t} = 0 \Rightarrow \lambda \Delta T + p_V = 0$.
Quand on est en plus en absence de source, $0 = dU = \delta Q_\text{ech} + Q_\text{créé} + \delta W$
$\delta Q_\text{ech} + 0 + 0$.

#### Différentes géométries
##### Géométrie unidirectionnelle
Après une analyse du problème et un étude des symétries, en ayant sur un axe
unique $T = T(x)$ et $\overrightarrow{\rm j_\text{Th}} = j_\text{Th}(x) \overrightarrow{\rm e_x}$.
- On peut en régime stationnaire utiliser la conservation du flux thermique le
  long d'un tube de champ thermique, donnant $j_\text{Th}(x) S$ constante, qui
  nous donne une expression du premier degré du $T(x)$
- On peut trouver l'équation différentielle grâce au premier principe sur un
  système élémentaire, qui est ici un cylindre d'épaisseur $dx$ dans lequel on
  considère la température homogène, permettant de calculer $d U$, qui étant nul
  en régime stationnaire nous donne l'équation
- Avec l'équation de diffusion $\rho c \frac{\partial T}{\partial t} = \lambda \Delta T$

##### Géométrie unidimensionnelle cylindrique
- Dans le cas d'un régime stationnaire en absence de source, $\Phi_\text{Th}$
  se conserve le long des tubes de champ, donnant $T = A h r + B$
- La méthode générale demande d'appliquer le premier principe à la couronne
  cylindrique de hauteur $h$ et comprise entre $r$ et $r + dr$.
- En régime stationnaire, $\lambda \Delta T = 0$, donnant en coordonnées
  cylindriques $\frac{1}{r} \frac{\partial}{\partial r} (r \frac{\partial T}{\partial r}) = 0$.

##### Géométrie sphérique
- On peut aussi utiliser le régime stationnaire en absence de source,
  donnant $\frac{\partial T}{\partial r} = \frac{C}{r^2}$ avec $C$ une
  constante, permettant de dériver $T = \frac{A}{r} + B$
- On peut appliquer le premier principe de la thermodynamique à une coquille
  sphérique
- Autrement, si l'expression est donnée, on utilise l'équation de diffusion avec
  le laplacien sphérique

#### Résistance thermique
En régime stationnaire et en l'absence de source, l'analogie de la conduction
thermique avec la conduction électrique permet de définir une résistance
électrique. On pose donc $R_\text{Th} = \frac{T_1 - T_2}{\Phi_{\text{Th} 1 \to 2}}$.

Cette expression se retrouver directement par continuité de $T$ dans
l'expression de $T(x)$ dans le cas unidirectionnel qui est $\frac{T_2 - T_1}{L} x + T_1$,
donnant avec l'expression du flux thermique $\lambda \frac{T_1 - T_2}{L} S$,
donnant $R_\text{Th} = \frac{L}{\lambda S}$. Attention à bien calculer le flux
thermique dans les autres systèmes de coordonnées. On peut d'ailleurs voir que
pour une sphère, $R_\text{Th} = \frac{e}{\lambda S}$, qui est une approximation
de l'espace entre deux plans pour 2 sphère proches.

### Conditions aux limites
#### Solide-solide
Au niveau d'une interface entre deux solides, on parle de contact parfait quand
$T$ est continue à l'interface (la chaleur qui se propage dans le solide). Par
défaut, on supposera toujours un contact parfait. Il y a aussi continuité du
flux thermique, qu'on peut démontrer en appliquant le premier principe de la
dynamique à la surface de contact, pour laquelle l'énergie est nulle puisque sa
masse est nulle.

#### Solide-fluide
Dans un fluide il y a facilement des mouvement macroscopiques de convection, qui
ont tendance à homogénéiser le fluide. Dans un gaz, on supposera même que $T$
est toujours uniforme. Les liquides sont, selon certains cas, modélisés comme
des solides, des liquides avec différents comportements, ou des gaz.

Il y a discontinuité de la température au niveau de la paroi (le milieu
s'accorde plus avec lui-même que l'extérieur).

> __Loi de Newton :__ Le flux sortant d'une paroi solide en contact avec un gaz
> vaut $\overrightarrow{\rm j}(x_{0}^+) = h (T_p - T_\text{ext}) \overrightarrow{\rm r_\text{ext}}$
> avec si $T_p > T_\text{ext}$, $\overrightarrow{\rm j} \cdot r_\text{ext} > 0$ et
> inversement. $h$ est le coefficient conducto-convectif de Newton en $W \cdot m^{-2} \cdot K^{-1}$.

Ce $h$ dépend de la nature de gaz et de l'épaisseur de la couche limite, car on
peut l'étudier comme les particules de gaz qui viennent régulièrement frapper
une paroi solide. On obtient pour $\lambda_g$ la conductivité thermique du gaz
et $e$ l'épaisseur de la paroi $h = \frac{\lambda_g}{e}$.

#### Cas particulier
Dans certains exercices, l'analyse qualitative du problème impose des flux
thermiques au niveau de certaines surfaces.

#### Irréversibilité
##### Dans l'équation différentielle
La diffusion thermique est caractérisée par $\lambda \Delta T = \rho c \frac{\partial T}{\partial t}$.
Puisque l'une des dérivées est impaire en $t$, l'équation différentielle est
différente sur $-t$ et donc le phénomène est irréversible.

La propagation caractérisée par $\Delta X - \frac{1}{c^2} \frac{\partial^2 X}{\partial t^2} = 0$
est un phénomène réversible.

##### Dans le modèle de Fourier
Dans le modèle de Fourier, l'échange élémentaire de chaleur est toujours orienté
du chaud vers le froid et est donc irréversible.

##### À l'aide du second principe de la thermodynamique
...

#### Résolution de l'équation de diffusion en régime variable
##### Analyse qualitative
On cherche un ordre de grandeur du temps caractéristique $\tau$ de la diffusion
de la chaleur sur une distance $L$. On l'obtient en raisonnant sur l'équation
de diffusion en termes d'ordres de grandeur, en assimilant les dérivées aux taux
d'acroissement. On a donc à partir de $\lambda \Delta T = \rho c \frac{\partial T}{\partial t}$
avec $\Delta T \approx \frac{\delta T}{L^2}$ et $\frac{\partial T}{\partial t} \approx \frac{\delta T}{\tau}$,
que $L = \sqrt{\frac{\lambda}{\rho c} \tau}$ et donc $\tau = \frac{\rho c L^2}{\lambda}$.
On peut ainsi remarquer que la diffusion est un phénomène lent : $L$ est
proportionnel à $\sqrt{\tau}$

##### Étude de solutions particulières
L'énoncé fournit une forme de solution dont il faut vérifier la validité.
Par exemple, pour un barreau, on recherche des solutions de la forme $T(x,t) = T_0 + \delta T(x,t)$,
qu'on formule avec la forme complexe $\underline{\delta T} = f(x) e^{j \omega t}$, donnant
$\frac{- \rho c j \omega}{\lambda} = (\frac{1 - j}{\sqrt{\frac{2 \lambda}{\rho c \omega}}})^2$,
soit une équation de la forme finale avec $D = \frac{\rho c}{\lambda}$
$T(x,t) = T_0 + \frac{\theta}{\sqrt{1 + \frac{D t}{\ell_0^2}}} \exp(- \frac{x^2}{\ell_0^2 + 4 D t})$,
et donc une longueur caractéristique de $\ell \approx \sqrt{4 D t}$.
