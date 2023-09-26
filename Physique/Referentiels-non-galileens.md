# Changement de référentiel et mécanique non galiléenne
## Référentiel
### Référentiel et repère
#### Définition
Un référentiel est la donnée d'un solide indéformable et d'une horloge. Un
repère $R$ est constitué d'un point et de 3 vecteurs de direction différente.
Matériellement, un repère $R$ est constitué à l'aide de 4 points du solide $\mathcal{S}$ associé au repère
$R$ de points $O,A,B,C$. Il existe donc une infinité de repères possibles.

Dans la pratique, on utilise un repère orthonormé du $\mathbb{R}$-espace
euclidien classique. En mécanique Newtonienne, toutes les horloges sont
équivalentes (c'est un problème toute autre en mécanique relativiste).

### Mouvement relatif d'un référentiel $\mathcal{R}_2$ par rapport à un référentiel $\mathcal{R}_1$
Soit $R_1$ un repère attaché à $\mathcal{R}_1$ et $R_2$ à $\mathcal{R}_2$.
On souhaite caractériser le mouvement de $R_2$ par rapport à $R_1$.

> $R_2$ est en translation par rapport à $R_1$ si la vitesse de tout point en $R_1$ est la même pour tous les points du référentiel.

Ainsi, le mouvement est entièrement défini par la donnée de la vitesse de
translation de l'origine de $R_2$ dans $R_1$.

#### Exemple du référentiel lié à un train sur terre
Soit un train se déplaçant sur une distance $d \ll R_T$ (auquel cas par
propriété d'une variété on peut considérer qu'on se déplace sur une surface
plane) et rectiligne, il est en translation rectiligne par rapport à la Terre.

La nacelle d'une grande roue est en translation : elle reste dirigée vers le centre
de la terre. Sa translation est en revanche circulaire.

### Rotation
#### Cas particuliers fondamental du mouvement de rotation autour d'un axe fixe
On peut prendre le cas du manège par rapport au repère terrestre.

#### Vecteur rotation instantané de $R_2$ par rapport à $R_1$
On peut prendre le cas du repère cylindrique par rapport au repère cartésien,
quand $\dot{\theta}(t) \neq 0$. On a $\frac{d \overrightarrow{\rm u_r}}{dt} = \dot{\theta} \overrightarrow{\rm u_r}$
et $\frac{d \overrightarrow{\rm u_\theta}}{dt} = - \dot{\theta} \overrightarrow{\rm u_r}$.

On constate que si on pose $\overrightarrow{\rm \Omega_{R_2/R_1}} = \dot{\theta} \overrightarrow{\rm u_{z_1}}$,
on obtient $(\frac{d \overrightarrow{\rm v_r}}{dt})_{R_1} = \overrightarrow{\rm \Omega_{R_2/R_1}} \wedge \overrightarrow{\rm v_r}$,
$(\frac{d v_\theta}{dt})_{R_1} = \overrightarrow{\rm \Omega_{R_2/R_1}} \wedge \overrightarrow{\rm v_\theta}$,
et $(\frac{d \overrightarrow{\rm u_{z_1}}}{dt})_{R_1}$ qui est nul.

De plus, dans le cas d'une rotation plus complexe qu'une seule rotation
circulaire, on a $\overrightarrow{\rm \Omega_{3/1}} = \overrightarrow{\rm \Omega_{3/2}} + \overrightarrow{\rm \Omega_{2/1}}$ :
on décompose la rotation par plusieurs rotations d'axe fixe.

#### HP : Mouvement le plus général
Tout mouvement se ramène à la superposition d'une rotation autour d'un axe et
d'une translation de l'axe. Le mouvement est alors entièrement caractérisé par
$\overrightarrow{\rm v_1}(O_2)$ et $\overrightarrow{\rm \Omega_{2/1}}$ (des
vecteurs tous deux variables de norme et de direction).

### Dérivée covariante
Soit un vecteur $\overrightarrow{\rm X}$, on veut comparer sa dérivée dans $R_1$
et $R_2$. On cherche à relier $(\frac{d \overrightarrow{\rm X}}{dt})_{R_1}$
à $(\frac{d \overrightarrow{\rm X}}{dt})_{R_2}$, et on obtient (facilement
prouvable) $(\frac{d \overrightarrow{\rm X}}{dt})_{R_1} = (\frac{d \overrightarrow{\rm X}}{dt})_{R_2} + \overrightarrow{\rm \Omega_{R_2/R_1}} \wedge \overrightarrow{\rm X}$.

## Loi de composition des mouvements
Soit $R_1$ le référentiel "absolu", et $R_2$ le référentiel "relatif", on
cherche à établir des relations sur la vitesse et l'accélération entre les deux
référentiels.

### Cas d'un référentiel $R_2$ en translation par rapport à $R_1$
Par définition, $\overrightarrow{\rm v_1}(M) = (\frac{d \overrightarrow{\rm O_1 M}}{dt})_1$
et $\overrightarrow{\rm v_2}(M) = (\frac{d \overrightarrow{\rm O_2 M}}{dt})_2$..
On a par Chasles $\overrightarrow{\rm O_1 M} = \overrightarrow{\rm O_1 O_2} + \overrightarrow{\rm O_2 M}$,
donc par linéarité $\overrightarrow{\rm v_1}(M) = (\frac{d \overrightarrow{\rm O_1 O_2}}{dt})_1 + (\frac{d \overrightarrow{\rm O_2 M}}{dt})_1$
$= \overrightarrow{\rm v_1}(O_2) + ((\frac{d \overrightarrow{\rm O_2 M}}{dt})_2 + \overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm O_2 M})$
(formule générale).

Or, comme le référentiel est en translation, on simplifie comme $\overrightarrow{\rm v_1}(M) = \overrightarrow{\rm v_2}(M) + \overrightarrow{\rm v_1}(O_2)$.
Le premier terme correspond à la vitesse absolue, et les deux termes de la somme
sont respectivement la vitesse relative (celle de $M$ dans le repère $R_2$),
et la vitesse d'entraînement en $M$ de $R_2$ à $R_1$.

Soit un point de $P$ coïncident avec $M$ à l'instant $t$ mais fixe dans $R_2$,
comme la vitesse relation est alors nulle, on obtient l'égalité de la vitesse
d'entraînement avec $\overrightarrow{\rm v_1}(P)$.

#### Loi de composition des accélérations
En bourrinant exactement les mêmes calculs, on obtient
$\overrightarrow{\rm A_1}(M) = \overrightarrow{\rm A_2}(M) + \overrightarrow{\rm A_1}(O_2)$,
et avec le point d'entraînement l'accélération d'entraînement est de $\overrightarrow{\rm A_1}(O_2)$.

Si $R_2$ est en translation rectiligne uniforme, on obtient les conditions d'un
référentiel galiléen.

### Cas d'un référentiel $R_2$ en rotation uniforme par rapport à $R_1$
On a alors $\overrightarrow{\rm \Omega_{2/1}}$ un vecteur constant, et l'axe est
de direction fixe.

#### Loi de composition des vitesses
Par décomposition de Chasles et dérivée covariante, on obtient
$\overrightarrow{\rm v_1}(M) = \overrightarrow{\rm v_2}(M) + \overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm O_2 M}$,
et on obtient que la vitesse d'entraînement est $\overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm O_2 M}$.

Comme l'axe doit être fixe, $O_2$ est fixe dans $R_1$.

#### Loi de composition des accélérations
On obtient cette fois-ci
$\overrightarrow{\rm A_1}(M) = \overrightarrow{\rm A_2}(M) + \overrightarrow{\rm \Omega_{2/1}} \wedge (\overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm O_2 M}) + 2 \overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm v_2}(M)$.
On obtient de même avec le point coïncident que l'accélération d'entraînement
est $\overrightarrow{\rm A_1}(P) = \overrightarrow{\rm \Omega_{2/1}} \wedge (\overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm O_2 M})$.

On réécrit toute l'expression comme l'accélération relative, l'accélération
d'entraînement et l'accélération de Coriolis $\overrightarrow{\rm A_C}(M) = 2 \overrightarrow{\rm \Omega_{2/1}} \wedge \overrightarrow{\rm v_r}(M)$.

Propriétés de l'accélération de Coriolis : le terme n'apparaît pas dans les
mouvements de translation, ...
