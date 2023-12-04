# Interférences à deux ondes
## Principe et présentation générale
> Soit une une zone de l'espace où deux faisceau lumineux se recouvrent (se
> superposent). Si $\exists M \mid I_{1 + 2}(M) \neq I_1(M) + I_2(M)$, on parle
> d'interférence.

Dans une zone d'interférence, il peut y avoir des points où
$I_{1 + 2}(M) = I_1(M) + I_2(M)$. Si pour tout point,
$I_{1 + 2}(M) = I_1(M) + I_2(M)$, il n'y a pas d'interférences.

On représente des coupes planaires de ces zones d'interférence, correspondant à
ce qui est projeté sur un écran. Pour faire une figure d'interférence, on repère
les points de valeur $I_\text{max}$ et $I_\text{min}$ (formant souvent des
courbes plus faciles à comprendre).

Les franges "sombres" ne sont pas toujours obscures. On utilise alors la notion
de contraste de la figure (aussi appelé visibilité) : $V = C = \frac{I_\text{max} - I_\text{min}}{I_\text{max} + I_\text{min}}$.
Cette grandeur est donc de $1$ seulement si $I_\text{min} = 0$, et on ne voit
rien ($0$) si $I_\text{min} = I_\text{max}$.

De façon générale dans les exercices : On montre d'abord qu'il y a interférence
en montrant que les rayons se superposent et qu'en l'un des points où c'est le
cas, il y a interférence (les rayons ont une "histoire différente"). On vérifie
que les deux rayons soient cohérents (ondes monochromatiques de même pulsation,
pas ponctuelles...).\
On calcule $\Delta \varphi(s)$ (le but de l'exercice), et on définit la figure
obtenue sur l'écran en donnant la forme des franges (rectiligne, circulaire),
on calcule leurs positions, et dans le cas de franges rectilignes, on définit
l'interfrange (la distance entre deux franges de même nature consécutifs) (les
anneaux sont rarement régulièrement espacés). Si demandé, on peut aussi calculer
le contraste $C$.

### Calcul de base
#### Conditions de cohérence de rayons qui se superposent
Soit deux rayons qui se superposent en un point $M$, avec
$s_1(M,t) = s_{01} \cos(\omega_1 t - \varphi_1(M))$ et
$s_2(M,t) = s_{02} \cos(\omega_2 t - \varphi_2(M))$.
On a $I_1 = \frac{1}{2} k s_{01}^2$ et $I_2 = \frac{1}{2} k s_{02}^2$.
On étudie $s_\text{tot}(M,t) = s_1(M,t) + s_2(M,t)$, et
$I_\text{tot}(M) = k < s_\text{tot}^2 > = k < (s_1 + s_2)^2 >$
$= k < s_1^2 > + k < s_2^2 > + 2 k < s_1 s_2 >$.

Ainsi, $I_\text{tot}(M) = I_1 + I_2 + 2 k s_{01} s_{02} < \cos(\omega_1 t - \varphi_1) \cos(\omega_2 t - \varphi_2) >$
$= I_1 + I_2 + 2 \sqrt{I_1 I_2} < \cos((\omega_1 + \omega_2) t + \varphi_1 + \varphi_2) + \cos((\omega_1 - \omega_2) t + \varphi_1 - \varphi_2) >$.
C'est ce dernier terme interférentiel qui nous intéresse. Il n'y a interférence
que s'il est non nul.

Si les deux rayons n'ont pas la même pulsation, en notant $T = \frac{2 \pi}{\omega_1 + \omega_2}$
et $T' = \frac{2 \pi}{|\omega_1 - \omega_2|}$, on a $T,T' \ll \tau_D$ et donc la
valeur moyenne sur $\tau_D$ est nulle. Ainsi, la première condition pour voir
des interférences est que les rayons interférents soient isochrones (de même
pulsation). Si $\omega_1 = \omega_2$, le terme interférentiel est $0 + < \cos(\varphi_1(M) + \varphi_2(M)) >$.

Ainsi, on trouve une deuxième condition pour que celui-ci soit non nul, en écrivant
$\varphi_1(M) = \frac{2 \pi}{\lambda_0}(S,M)  + \varphi_{01}$ et
$\varphi_2(M) = \frac{2 \pi}{\lambda_0}(S,M)  + \varphi_{02}$. Les phases à
l'origine $\varphi_{01}$ et $\varphi_{02}$ sont des fonctions constantes par
morceaux de longueurs $\tau_c$ (les valeurs sont des constantes aléatoires),
donnant comme $\tau_D \gg \tau_c$ que $< \cos(\frac{2 \pi}{\lambda_0} \delta + (\varphi_{01} - \varphi_{02})) >_{\tau_D}$
est nul pour ces valeurs moyennes de cosinus aléatoires.
Pour voir des interférence, il faut donc que $\varphi(01)(t) = \varphi_{02}(t)$
et donc que $S_1 = S_2$. Les deux rayons doivent donc provenir de la même source
ponctuelle.

On trouve une troisième condition : si la source est parfaitement
monochromatique, $\varphi_0$ est unique, l'onde dure un temps infini
mais pour une onde réelle $\varphi_0$ change pour chaque photon (train d'onde).
Pour avoir des interférences, il faut qu'un photon interfère avec lui-même. Pour
que ce soit possible, il faut que $\tau_R < \tau_c$, avec $\tau_R$ le retard dû
à la différence de trajet (sinon, il interfèrera avec un autre photon),
et donc $\delta = c \tau_R < \ell_c = c \tau_c$, avec $\ell_c$ la longueur d'un
photon.

##### Conclusion
Tous ces critères nous donne des conditions très fortes pour pouvoir obtenir une
interférence : il y a une interférence si et seulement si les deux rayons sont
issus d'une même source ponctuelle quasi-monochromatique et que $\delta(M) < \ell_c$.
Cela donne les contraintes $\left\{\begin{matrix} \omega_1 = \omega_2 \\ S_1 = S_2 \\ \delta < \ell_c \end{matrix}\right.$.

> Dans ce cas précis, on a $I = I_1 + I_2 + 2 \sqrt{I_1 I_2} \cos(\frac{2 \pi}{\lambda_0} ((S_1 M) - (S_2 M)))$.

#### Calcul à savoir refaire dans le cas d'interférences de deux rayons cohérents
On retrouve la formule précédente à partir des hypothèse qu'on a déterminé. On
dit que deux rayons sont cohérents s'ils sont issus d'une source ponctuelle
monochromatique. La troisième condition n'est pas à spécifier la plupart du
temps quand la source est monochromatique car alors $\Delta \omega = 0 \Rightarrow \tau_c = +\infty$.

Dans le cas d'une source ponctuelle monochromatique, les rayons sont cohérentes
et on peut utiliser les complexes : $S_1 = s_{01} e^{i (\omega t - \varphi_1(M))}$
et $S_2 = s_{02} e^{i (\omega t - \varphi_2(M))}$, donnant $I_\text{tot}$
$= \frac{1}{2} k |\underline{S_1} + \underline{S_2}|^2$\
$= \frac{1}{2} k (\underline{S_1} + \underline{S_2}) \overline{(\underline{S_1} + \underline{S_2})}$\
$= \frac{1}{2} k (|S_1|^2 + |S_2|^2 + \underline{S_1} \overline{\underline{S_2}} + \overline{\underline{S_1}} \underline{S_2})$\
$= I_1 + I_2 + \frac{1}{2} k (s_{01} s_{02} (e^{i \varphi_2 - \varphi_1} + e^{-i (\varphi_2 - \varphi_1)}))$\
$= I_1 + I_2 + k (s_{01} s_{02} \cos(\varphi_2 - \varphi_1))$\
Donnant la formule attendue, appelée parfois formule de Fresnel, la formule des
interférences à deux ondes.

#### Analyse de la formule de Fresnel
Lorsque le déphasage atteint les cas limite de $\Delta \varphi = 2 p \pi$,
pour lequel on atteint l'intensité maximale (interférences constructives),
et $\Delta \varphi = (2p + 1) \pi$, pour lequel on atteint l'intensité minimale
(interférences destructives). On obtient ainsi que $C = \frac{\sqrt{I_1 I_2}}{\frac{I_1 + I_2}{2}} \leq 1$,
avec $C = 1$ si $I_1 = I_2$.

> On peut aussi réécrire la formule lorsque $I_1 = I_2$ comme
> $I(M) = 2 I_0 (1 + \cos(\Delta \varphi(M)))$.

#### Définition de l'ordre d'interférence et de la différence de marche
$\Delta_{2/1} \varphi(M) = \frac{2 \pi}{\lambda_0} ((SM)_2 - (SM)_1)$. On pose
$\delta_{2/1}(M) = (SM)_2 - (SM)_1$, la différence de marche en $M$.
On pose de même $p(M) = \frac{\delta(M)}{\lambda_0}$ l'ordre d'interférence en $M$.

> On peut donc enfin réécrire $\Delta \varphi(M) = \frac{2 \pi}{\lambda_0} \delta(M) = 2 \pi p(M)$.

Une frange brillante est une courbe d'intensité lumineuse maximale, caractérisée
par $\Delta \varphi = 2 \pi n$, $\delta = n \lambda_0$ et $p = n$ avec $n \in \mathbb{Z}$.\
Une frange sombre est une courbe d'intensité lumineuse minimale, caractérisée
par $\Delta \varphi = (2n + 1) \pi$, $\delta = (n + \frac{1}{2}) \lambda_0$ et $p = n + \frac{1}{2}$ avec $n \in \mathbb{Z}$.

## Différents types d'interférences et calcul d'ordre d'interférence, de différence de marche, de déphasage
### Définition
#### Interférence par division du front d'onde ou division d'amplitude
> On parle de division du front quand les deux rayons cohérents qui interfèrent
> sont différente au niveau de la source.

> On parle de division d'amplitude si les deux rayons cohérents qui interfèrent
> sont issus d'un même rayon partant de la source.

#### Interférences non localisées et localisées
> Si le dispositif interférentiel permet d'observer une figure d'interférence sur
> un écran "quelque soit" sa position, on parle d'interférence non localisées.
> S'il en permet de voir la figure que dans une zone très petite de l'espace, on
> parle d'interférence localisées.

### Calcul général
#### Interférences d'onde plane
On repère des interférences d'onde plane quand deux faisceaux de lumière
parallèles se superposent. Comme $\varphi_1(M) = \overrightarrow{\rm k_1} \cdot \overrightarrow{\rm OM} + \varphi_1(O)$
et $\varphi_2(M) = \overrightarrow{\rm k_2} \cdot \overrightarrow{\rm OM} + \varphi_2(O)$, avec
$\overrightarrow{\rm k_1}$ et $\overrightarrow{\rm k_2}$ de même amplitude
mais pas de même directions $\overrightarrow{\rm u_1}$ et $\overrightarrow{\rm u_2}$,
avec $\overrightarrow{\rm u_1} = \cos(\frac{\beta}{2}) \overrightarrow{\rm u_x} - \sin(\frac{\beta}{2}) \overrightarrow{\rm u_z}$
et $\overrightarrow{\rm u_2} = \cos(\frac{\beta}{2}) \overrightarrow{\rm u_x} + \sin(\frac{\beta}{2}) \overrightarrow{\rm u_z}$.

On a donc $\Delta \varphi = (\overrightarrow{\rm k_2} - \overrightarrow{\rm k_1}) \cdot \overrightarrow{\rm OM} + \varphi_2(O) - \varphi_1(O)$
$= \frac{2 \pi}{\lambda_0} (\overrightarrow{\rm u_2} - \overrightarrow{\rm u_1}) \cdot \overrightarrow{\rm OM} + \Delta \varphi(O)$.
Ainsi, $\Delta \varphi(M) = 2 \sin(\frac{\beta}{2}) z + \Delta \varphi(0)$,
avec $z$ la composante en $\overrightarrow{\rm u_z}$ de $\overrightarrow{\rm OM}$. Pour $\Delta \varphi$
une constante, $z$ est une constante, donc les franges sont les droites
rectilignes de $z$ égal.

#### Interférences d'ondes sphériques
...

### Remarques importantes
On montrera que dans les trois cas suivants, il est nécessaire d'ajouter des
déphasages de $\pi$ :
- Réflexion vitreuse
- Réflexion métallique (miroir)
- Le passage par un foyer

Si un rayon passe par l'un de ces appareils, on augmente le déphasage de $\pi$ ou
le chemin optique de $\frac{\lambda}{2}$.

## Applications et exemples
### Trous d'Young
#### Calculs de base
Soit une source $S$ placée face à une barrière avec deux trous $S_1$ et $S_2$,
derrière la quelle il y a un écran à une distance $D$ avec le point $O$ sur
l'axe optique.

$\delta_{2/1}(M) = (SM)_2 - (SM)_1 = ((S S_2) + (S_2 M)) - ((S S_1) + (S_1 M))$\
$= (S_2 M) - (S_1 M) + ((S S_2) - (S S_1))$\
Par symétrie si le point $S$ est sur la médiatrice du segment
$[S_1 S_2]$, on a $(S S_1) = (S S_2)$.

On admet, sauf contre-indication ou sauf si l'objectif est de mesurer l'indice
de l'air, que l'expérience se déroule dans l'aire et que son indice est $1$.
Ainsi, pour $S$ sur la médiatrice de $[S_1 S_2]$, donnant $\delta(M) = S_2 M - S_1 M$
et permettant de faire des coordonnées pour chaque point. On calcule alors
$S_1 M = D \sqrt{1 + \frac{y^2}{D^2} + \frac{(2 - \frac{a}{2})}{D^2}}$; avec
$D \gg a,z,y$, on approxime $S_1 M \approx D (1 + \frac{y^2}{2D^2} + \frac{(z + \frac{a}{2})^2}{2 D^2})$,
et en faisant de même avec $S_2 M$, on obtient $\delta(M) = \frac{2z  \times 2 \frac{1}{2}}{2 D} = \frac{z a}{D}$
(en admettant qu'on mette les distances dans le bon sens, attention).

#### Cas du montage à deux lentilles (dit de Fraunhofer)
Le montage prend les rayons d'une source et les envoie comme des rayons à
l'infini dans les trous : ils sortent comme des rayons à l'infini avant de
croiser une nouvelle lentille qui forme l'image (un télescope avec des trous de
Young).

À l'aide du théorème de Malus, les points $S_1$ et $S_2$, donc
$(S S_1) = (S S_2)$. On place alors une source fictive au point d'image $M$,
et on applique le théorème de Malus à l'onde fictive, permettant de placer
sur la même surface d'onde $S_1$ et un point $H$ perpendiculaire au premier
rayon sur le deuxième rayon, donc $(M S_1) = (M H)$, donnant par principe du
retour inverse de la lumière (PRIL) $(S_1 M) = (HM)$.
