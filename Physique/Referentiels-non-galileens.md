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
