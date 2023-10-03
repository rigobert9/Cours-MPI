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

## Dynamique non galiléenne
### Référentiel galiléen
> Un référentiel galiléen est un référentiel dans lequel s'applique les lois de la
> dynamique. En particulier, le mouvement d'un système isolé est forcément
> rectiligne uniforme.

Le référentiel de Copernic (avec pour centre le centre de masse du soleil) ou le
référentiel héliocentrique (avec pour centre le soleil) sont des bonnes
approximations de référentiels galiléens.

On considère de même le référentiel géocentrique comme galiléen pour des
phénomènes courts devant $1$ an et sur des distances petites devant le diamètre
de la Terre.

Le référentiel terrestre sera considéré comme galiléen pour des durées faibles
devant $24$ heures et des distances faibles devant le rayon de la Terre.

### Loi de la dynamique du point matériel dans un référentiel non galiléen
On peut par exemple étudier le mouvement d'un pendule à l'intérieur d'une
voiture au démarrage. La voiture, lorsqu'elle est en mouvement uniformément
accéléré, place le pendule dans un équilibre relatif dans la référentiel de la
voiture.

Dans n'importe quel référentiel non galiléen, on peut appliquer les lois de la
dynamique à condition d'ajouter les forces d'inertie et de Coriolis,
d'expression respectivement $- m \overrightarrow{\rm a_i}$ et $- m \overrightarrow{\rm a_c}$. On peut
ainsi facilement prouver que le RFD et la TMC avec ces forces sont vrais,
permettant de se replacer dans ce qu'on connaît déjà.

### Rédaction
Un exercice de dynamique non galiléenne se résout par :
1. Bien définir $R$ et $R'$, ainsi que le mouvement de $R'$ par rapport à $R$ :
   il doit être en translation ou en rotation autour d'un axe, sinon HP - soit
   on s'est trompé, soit on est aidé, soit le concours nous demande vraiment du
   HP.
2. On calcule l'accélération d'entraînement et de Coriolis, puis les forces
   associées.
3. On déroule l'exercice de mécanique en restant prudent.

### Effet du caractère non euclidien du référentiel terrestre
La rotation instantanée du repère terrestre par rapport au repère géocentrique
est de norme $\frac{2 \pi}{24 \times 360} = 7.31 \text{rad} \cdot s^{-1}$. La
Terre n'étant pas un solide indéformable, elle est déformée (surtout à
l'équateur) en une forme qu'on peut supposer éllipsoïdale.

De plus, on peut redéfinir lorsque c'est nécessaire la pesanteur terrestre,
donnant $\overrightarrow{\rm g} = \overrightarrow{\rm G} + \frac{\overrightarrow{\rm F_{ie}}}{m}$,
soit dans un repère sphérique géocentrique $\overrightarrow{\rm G} = - G \frac{M}{(R_T + z)^2} \overrightarrow{\rm u_r}$
et $\overrightarrow{\rm F_{ie}} = m \Omega_T^2 r_\bot \overrightarrow{\rm e_{r_\bot}}$, soit
finalement $\overrightarrow{\rm g} = - G \frac{M_T}{r^2} \overrightarrow{\rm u_r} + \Omega_T^2 r_{\bot} \overrightarrow{\rm e_{r_\bot}}$.

Dans les exercices, la force d'entraînement est toujours incluse dans $\overrightarrow{\rm g}$, donc si on
prend le référentiel terrestre comme non galiléen il ne faut PAS ajouter $\overrightarrow{\rm F_{ei}}$.
En effet, le poids ne pointe jamais vraiment vers le centre de la Terre (sauf
aux pôles et à l'équateur), donc on prend simplement que la verticale d'un lieu
est définie par le poids plus la force d'entraînement.

Pour ce qui est de la force de Coriolis, la force ajoutée est $\overrightarrow{\rm F_{ic}} = - 2 m \overrightarrow{\rm \Omega_{R_T / R_\text{Géo}}} \wedge \overrightarrow{\rm V_{R_T}}(M)$.

Pour les mouvement horizontaux, en évaluant la force en sa partie horizontale,
on obtient $\overrightarrow{\rm F_{ic_H}} = - 2 m \Omega_T \sin(\lambda) \overrightarrow{\rm e_z} \wedge \overrightarrow{\rm v_{r_H}}$,
avec $\lambda$ la latitude sur Terre. C'est ce qui crée le phénomène de
tourbillons vers le centre d'une dépression, qui tournent dans le sens horaire
dans l'hémisphère nord et dans le sens antihoraire dans l'hémisphère sud.
Les alizés autour de l'équateur sont causés de la même façon. On peut aussi
remarquer plus d'érosion selon cette force (à l'est dans l'hémisphère nord) sur
le bord des fleuves ou sur les rails. Les boucles d'échappée des fleuves (comme
Horseshoe Canyon) sont souvent dans ce sens aussi.

Pour les mouvements verticaux, on obtient que les mouvement vers le bas (chute
libre) sont déviés vers l'est et ceux vers le haut (fusées) vers l'ouest. Cette
déviation est d'ailleurs plus faible plus on est proches de l'équateur (encore
une autre difficulté diminuée en étant plus proche de l'équateur).
