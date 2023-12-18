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

Dans le cas de deux sources incohérentes, les figures d'interférence s'ajoutent
l'une à l'autre.

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

On calcule enfin la position de la figure d'interférence : $\delta = \frac{a z}{D}$
y est constant, donc $z$ y est constant, donc les franges sont rectilignes
et sont de position $z_n = n \frac{\lambda D}{a}$ ($\delta = n \lambda$).

Une autre méthode (au programme) est qu'on observe plus en $M$ d'interférences si
les rayons issus du centre de la source et du bord sont en opposition de phase.
Ainsi, il faut $|P_{z = \frac{b}{2}}(M) - P_{z = 0}(M)| = \frac{1}{2}$, nous
amenant à $\frac{ab}{2 d_S} = \frac{\lambda}{2} \Rightarrow b = \frac{d_S \lambda}{a}$.

#### Un autre dispositif équivalent : le miroir de Lloyd
On observe une source face à un écran, avec un miroir à l'horizontale sous la
source. Les rayons allant vers l'écran sont alors ceux qui sont directs et ceux
réfléchis par le miroir.

Cette construction se ramène en fait aux trous d'Young en considérant une source
symétrique de la source de l'autre côté du miroir; les calculs sont alors les
mêmes.

Le dispositif du miroir de Fresnel fait la même chose en encore plus compliqué,
mais on se ramène encore aux trous d'Young une fois la source virtuelle
trouvée.

### Interféromètre de Michelson
#### Présentation et remarque préliminaire
La lame centrale (la séparatrice) est une lame de verre avec une fine couche de
métal qui permet de réfléchir un peu d'un rayon et de laisser passer le reste.
La lame de verre induisant une différence de marche, les calculs deviennent
complexes : le premier rayon ne passe qu'une seule fois par la lame de verre
après avoir été réfléchie, tandis que le deuxième passe trois fois par la lame.
On a ajoute donc une lame de verre (la compensatrice) qui supprime cette
différence de marche induite par la séparatrice.

La différence de marche induite par la séparatrice est de $3ne - 1ne = 2ne$,
avec $e$ l'épaisseur traversée dans la séparatrice, de valeur (pour
l'orientation originale) $e = \frac{e_{Sp}}{\cos(\frac{\pi}{2})} = \sqrt{2} e_{Sp}$.

#### Effet géométrique de la face métallisée
La séparatrice permet, au final, de considérer que les deux rayons qui arrivent
viennent comme de deux miroirs l'un derrière l'autre (le second miroir est vu
comme son symétrique par la séparatrice); et ces rayons sont comme s'ils
provenaient du symétrique de la source par la séparatrice.

#### Interféromètre de Michelson en lame d'aire par division d'amplitude
Si l'angle $\alpha$ entre le deuxième miroir et la perpendiculaire à l'axe optique
est nul, on parle de lame d'air de distance $d$ (la distance entre l'image du
deuxième miroir par la séparatrice et le premier miroir). Ainsi, le montage se
comporte comme si le premier rayon allait sur le miroir tandis que le deuxième
allait sur le deuxième miroir derrière lui, avec une distance $d$.

Les deux rayons sortent alors parallèles du montage. On observe donc les
interférences dans le plan focal d'une lentille convergente.

Pour calculer la différence de marche, avec $I$ le point auquel les deux rayons
frappent le premier miroir, $J$ le point auquel le deuxième rayon frappe le
deuxième miroir et $K$ le point auquel il "repasse par" le deuxième miroir.
$\delta(M) = (SM)_2 - (SM)_1 = (SI) + IJ + JK + (KM) - ((SI) + (IM))$.

En réutilisant une source virtuelle, malus et le PRIL, on obtient avec $L$ le
point sur la même surface d'onde que $K$, donnant $\delta(M) = IJ + JK + (KM) - (IM)$
$= IJ + JK - IL = 2d \cos(\frac{\hat{IJK}}{2})$.

Les franges correspondent ainsi à des angles identiques, formant des franges qui
sont des anneaux sur l'écran.

La frange centrale, correspondant à $\delta = 0$ et donc à $\cos(i) = 0$, est
celle des rayons $i = \frac{\pi}{2}$, qui sont à l'infini sur l'écran.

On cherche ensuite à calculer le rayon des anneaux des franges. On pose $r = f' \tan i$.
La frange d'ordre d'interférence $n$ vérifie $p(r_n) = n \Rightarrow \delta(r_n) = n \lambda$.
Ainsi, $n \lambda = 2 d \cos(i_n)$ avec $f' \tan(i_n) = r_n$. Comme $i_n \ll 1$,
on a $\left\{\begin{matrix} \tan(i_n) \approx i_n + o(i_n^2) \\ \cos(i_n) \approx 1 - \frac{i_n^2}{2} \end{matrix}\right.$
$\Rightarrow \left\{\begin{matrix} 2d (1 - \frac{i_n^2}{2}) = n \lambda \\ i_n = \frac{r_n}{f'} \end{matrix}\right.$,
donnant $n \lambda = 2d (1 - \frac{r_n^2}{2f'^2})$, soit finalement $r_n = f' \sqrt{2 (1 - \frac{n \lambda}{2d})}$.

On constate que $\delta(i = 0) = \delta_\text{max} = 2d$, et $\delta(i)$ est
décroissante sur l'intervalle qui nous intéresse. De même, $p(i = 0) = \frac{2d}{\lambda}$
et $p$ est décroissante sur l'intervalle. On cherche à relier $q$ le numéro de
l'anneau compté à partir du centre avec $n_q$ son ordre d'interférence entier :
pour $q = 1$, $p(r_{n_1} = r_{q = 1}) = \left\lfloor \frac{2d}{\lambda} \right\rfloor$,
et on arrive à $p(r_{n_q} = r_q) = \left\lfloor \frac{2d}{\lambda} \right\rfloor - q + 1$.
En reprenant la formule pour $r_n$, on obtient $r_q = f' \sqrt{2 (1 - \frac{\lambda}{2d} (\left\lfloor \frac{2d}{\lambda} \right\rfloor - q + 1))}$
$= f' \sqrt{\frac{\lambda}{d} (q - 1) + 2 - \frac{\lambda}{d} \left\lfloor \frac{2d}{\lambda} \right\rfloor}$,
qui augmente bien avec $q$. En revanche, $r_{q+1} - r_q$ est décroissante et
tend vers $0$, donc les franges se resserrent en s'éloignant du centre.

L'interféromètre de Michelson utilisé en division d'amplitude fait interférer
rayons rayons issus d'un même rayon initial. Les deux rayons sont nécessairement
cohérents car issus du même point source.

Si on prend deux points source, la figure formée est en fait la même qu'avant,
en plus lumineuse car recevant au même endroit plusieurs sources.

Ainsi, cet interféromètre de Michelson en lame d'air et division d'amplitude
(écran à l'infini), on peut utiliser une source large et observer une figure
d'interférence très lumineuse et bien contrastée.

#### Interféromètre de Michelson en lame d'air et division du front d'onde
On place la source devant l'un des miroirs.

On peut voir en assimilant les rayons revenant des miroirs à des rayons venant
du symétrique de la source par le miroir que le montage est équivalent à deux
sources sur le même axe projetant leurs rayons sur l'écran perpendiculaire à
l'axe. Par symétrie de révolution, $\delta = f(r)$, donc la figure
d'interférence forme des anneaux.

$\delta = S_2 M - S_{1} M = \sqrt{L^2 + r^2} + \sqrt{(L - 2d)^2 + r^2}$\
Comme $L \gg r,d$, on obtient $\delta = L (1 + \frac{r^2}{2 L^2}) - (L - 2d) (1 + \frac{r^2}{2 (L - 2d)^2})$\
$= L + \frac{r^2}{2L} - (L - 2d) - \frac{r^2}{2 (L - 2d)}$\
$= 2d + \frac{r^2}{2} (\frac{L - 2d - L}{L (L - 2d)})$\
$= 2d (1 - \frac{r^2}{2 L (L - 2d)})$\
$= 2d (1 - \frac{r^2}{2 L^2})$

#### Autre dispositif équivalent
Le modèle de la lame de verre dans laquelle "rebondit" un rayon incident,
émettant avec une intensité de plus en plus faible des rayons parallèles des
deux côtés de la lame.

En prenant le rayon réfléchi et le premier rayon parallèle sortant du même côté,
la différence de marche obtenue est, avec $r$ l'angle de réflexion à l'intérieur
de la lame et $i$ l'angle d'incidence, de $\delta = 2n \frac{e}{\cos(r)} - 2 e \tan(r) \sin(i)$
$= 2 e (\frac{n}{\cos(r)} - \tan(r) \sin(i)) = \frac{2 e}{\cos(r)} (n - \sin(i) \sin(r))$
$= \frac{2 e n}{\cos(r)} (1 - \sin^2(r)) = 2 e n \cos(r)$.

En reprenant la formule du contraste avec la formule de Fresnel, on a $C = \frac{2 \sqrt{I_1 I_2}}{I_1 + I_2}$,
et comme en transmission $I_1 \gg I_2$ (donc $C \ll 1$) et en réflexion $C \approx 1$,
on observe en transmission des anneaux peu contrastés mais lumineux et des anneaux
très contrastés mais peu lumineux en réflexion.

#### L'interféromètre de Michelson en coin d'air
On règle les miroirs de façon à ce que la distance $d$
entre le centre des miroirs soit très petite (qu'on considèrera comme
approximation comme nulle), et orientés de façon à former un angle $\alpha$
non nul.

On traitera toujours le cas particulier du rayon incident en incidence normale
sur le miroir qui n'a pas tourné du côté où le miroir qui a tourné est devant.
Les rayons sont alors en division d'amplitude et se coupent sur le miroir qui a
tourné.

Si l'incidence du rayon n'est pas normale mais d'incidence $i$, les rayons se
"coupent" sur un plan passant par le point $O$ où se croisent les miroirs et
formant un angle $i + \alpha$ avec le miroir. Comme les angles sont d'amplitude
très petite, on éclaire le dispositif avec un rayon quasi-parallèle d'incidence
quasi-normale.

> On éclaire l'interféromètre de Michelson en coin d'air avec un faisceau de
> lumière quasi-parallèle en incidence quasi-normale sur "les miroirs". Les
> interférences sont donc localisées "sur les miroirs".

Pour observer les franges localisées sur les miroirs, on fait l'image des
miroirs sur un écran à l'aide d'une lentille convergente. La relation de
conjugaison de Descartes permet de trouver où placer cet écran (le placer dans
le plan conjugué des miroirs par une lentille convergente).

En notant $e(x)$ l'épaisseur du coin d'aire au point $M$ d'abscisse $x$,
$\delta(M) = 2 e(x)$ et donc $\delta$ est constant pour $e(x)$ constant :
les franges se font aux points d'égale épaisseur. Comme $e(x) = x \sin(\alpha)$,
$\delta = 2 x \sin(\alpha)$, et comme $\alpha \ll \pi$,
on approxime par $\delta = 2 \alpha x$.

Les franges sont rectilignes, la frange centrale se situe au point
d'intersection des deux miroirs et les franges sont positionnées aux points
$x_n = n \frac{\lambda}{2 \alpha}$. L'interfrange est donc de $\frac{\lambda}{2 \alpha}$

Idéalement, on éclaire le coin d'air avec un faisceau de lumière parallèle en
incidence normale sur le miroir qui n'a pas tourné. En pratique, la source
ponctuelle placée au foyer d'une lentille convergente a un rayon $R$. Le
faisceau sortant de la lentille est donc un cône de demi-angle au sommet
$\theta = \arctan(\frac{R}{f'}) \approx \frac{R}{f'}$.

Comme on l'a vu, chaque inclinaison crée une figure d'interférence dans un plan
passant par $O$. Quand on obtient l'image "des miroirs" par la lentille, tous
ces plans se superposent, on obtient des franges d'interférences lumineuses, ais
ceci est hors-programme.

#### Source ponctuelle, division du front d'onde
La différence de marche est alors $\delta(M) = \frac{2 \alpha ds x}{L}$, car le
dispositif est équivalent aux trous d'Young.

#### Autres franges d'égale épaisseur
On peut trouver avec les dispositifs classique de la goutte et de la tâche
d'huile, ou encore une bulle de savon (dont l'épaisseur est plus basse en bas à
case de la pesanteur). De façon générale, Michelson en coin d'air permet de
gérer tous les exercices qui traitent de variation d'épaisseur.

## Condition d'obtention des interfaces : problèmes de cohérence
### Effet de la polarisation des ondes électromagnétiques
En tenant compte de la polarisation du champ électrique du rayon, on écrit
les rayons comme $\overrightarrow{\rm E_1} = E_{10} e^{j(\omega t - \varphi_1(M))} \overrightarrow{\rm e_z}$
et $\overrightarrow{\rm E_2} = E_{20} (\cos \alpha \overrightarrow{\rm e_y} + \sin \alpha \overrightarrow{\rm e_z}) \times e^{j (\omega t - \varphi_2(M))}$.
On pose à nouveau $I_1 = k < E_1^2 > = \frac{k}{2} |\underline{E_1}|^2 = \frac{k}{2} E_\text{10}^2 = I_0$ et
$I_2 = k < E_2^2 > = \frac{k}{2} |E_2^2| = \frac{k}{2} E_{10}^2 (\cos^2(\alpha) + \sin^2(\alpha))$
$= \frac{k}{2} E_{20}^2 = I_0$.

$I(M) = k < (\overrightarrow{\rm E_1} + \overrightarrow{\rm E_2})^2 >$\
$= \frac{k}{2} |(\overrightarrow{\rm E_1} + \overrightarrow{\rm E_2})|^2$\
$= \frac{k}{2} (E_{10} + E_{20}^2 \cos^2(\alpha) + E_{10} E_{20} \cos(\alpha) (e^{- i (\varphi_1 - \varphi_2)} + e^{i (\varphi_1 - \varphi_2)}) + E_{20}^2 \sin^2(\alpha))$\
$= I_0 + I_0 \cos^2(\alpha) + 2 I_0 \cos(\alpha) \cos(\varphi_1 - \varphi_2) + I_0 \sin^2(\alpha)$.

> Finalement, on obtient que $I(M) = 2 I_0 (1 + \cos(\alpha) \cos(\Delta \varphi))$.

On obtient d'ailleurs avec les valeurs maximales et minimales que $C = |\cos \alpha|$
(donc que le contraste est nul si $\alpha = \frac{\pi}{2}$). Ainsi, deux ondes
polarisées perpendiculaires n'interfèrent pas.

### Cohérence spatiale : taille de la source
#### Définition
> La cohérence spatiale d'un dispositif interférentiel est caractérisée par la
> longueur $\ell_S$ de cohérence spatiale qui correspond à la taille maximale de
> la source au-delà de laquelle on ne voit plus de figure d'interférence.

Par exemple, pour les trous d'Young, $\ell_{S_y} = +\infty$ et
$\ell_{S_x} = \frac{D_S \lambda}{a}$. Pour Michelson en lame d'air et division
d'amplitude, $\ell_S = +\infty$.

#### Calcul exact de  $\ell_{S_x}$ pour les trous d'Young
C'est un exercice hors-programme mais qui peut être donné guidé.

En plaçant les points de la source des trous d'Young sur un axe, soit une source
de hauteur $X$, $\delta(M) = \frac{a X}{D_S} + \frac{ax}{D}$. Si la source
totale émet une intensité $I_0$ de manière uniforme alors $S(X)$ de longueur $dX$
émet $d I_0$, ce qui pour une source de largeur $b$ donne $d I_0 = \frac{I_0}{b} dX$.

Chaque source $S(X)$ de largeur $dX$ crée une figure d'interférence incohérentes
entre elles, donnant $I(M) = \int\limits_{\text{Tous les } S(X)} d I_{S(X)}(M)$
$= \int\limits_{-\frac{b}{2}}^{\frac{b}{2}} 2 d I_0 (1 + \cos(\frac{2 \pi}{\lambda} \delta_{S(X)}(M)))$\
$= \int\limits_{-\frac{b}{2}}^{\frac{b}{2}} 2 \frac{I_0}{b} (1 + \cos(\frac{2 \pi}{\lambda} \delta_{S(X)}(M))) dX$\
$= \frac{2 I_0}{b} (b + \frac{\lambda D_S}{2 \pi a} (\sin(\frac{\pi}{\lambda} (\frac{ab}{2 D_S} + \frac{ax}{D})) - \sin(\frac{\pi}{\lambda} (- \frac{ab}{2 D_S} + \frac{ax}{D}))))$\
$= 2 I_0 (1 + \frac{\lambda D_S}{\pi a b} \sin(\frac{2 \pi}{\lambda} \frac{ab}{2 D_S}) \cos(\frac{2 \pi}{\lambda} \frac{ax}{D}))$\
$= 2 I_0 (1 + \text{sinc}(\frac{\pi ab}{\lambda D_S}) \cos(\frac{2 \pi a x}{\lambda D}))$

On obtient alors avec les valeurs minimales et maximales de $I$ un contraste
$C = |\text{sinc}(\frac{\pi a b}{\lambda D_S})|$.

L'interfrange est $i = \frac{\lambda D}{a}$. Le contraste est nul quand le sinus
cardinal s'annule, donnant $\ell_{S_X} = \frac{\lambda D_S}{a}$. Si $b$ augmente
au-delà de cette limite, le contraste augmente à nouveau, mais le sinus cardinal
est négatif, donc les franges brillantes deviennent sombre et inversement.

#### Calcul qualitatif : méthode sur la différence d'ordre d'interférence
Les franges disparaissent sur l'écran quand la source large est telle que en un
point $M$ l'intensité créée par le centre de la source soit en opposition de
phase avec l'intensité créée par un bord. Ainsi, il faut
$|P_\text{centre}(M) - P_\text{bord}(M)| = \frac{1}{2}$, donc
$|\Delta \delta(M)| = \frac{\lambda}{2}$, soit
$|\frac{ax}{D} - (\frac{a \frac{b}{2}}{D_S} + \frac{ax}{D})| = \frac{\lambda}{2}$,
donnant $\frac{ab}{2 D_S} = \frac{\lambda}{2} \Rightarrow b_i = \frac{\lambda D_S}{a}$.

#### Cas de la division d'amplitude
Dans le cas d'un dispositif de division d'amplitude, $I(M)$ ne dépend pas de la
position de $S$, donc on peut utiliser une source large. Chaque point source crée
ainsi la même figure, et donc elles se superposent et forment une figure plus
lumineuse.

### Influence du spectre de la source : cohérence temporelle
#### Définition
Il y a interférence seulement si $\delta < \ell_c$ la taille du train d'onde
créé par la source de longueur spectrale $\Delta \omega$, soit $\ell_c = c \tau_c \nu \frac{c}{\Delta \tau}$.

$\ell_c$ est la longueur de cohérence temporelle de la source, inversement
proportionnelle à la longueur du spectre de la source (avec le coefficient de
proportionnalité dépendant de la forme du spectre).

#### Méthode qualitative
Soit un spectre considéré comme une raie rectangulaire de largeur $\Delta \nu$
centrée en $\nu_0$, on cherche à trouver quand la fréquence $\nu_0$
est en opposition avec celle créée par le bord du spectre, soit
$|p_{\nu_0}(M) - p_{\nu_0 + \frac{\Delta \nu}{2}}(M)| = \frac{1}{2}$.
Comme $p(M) = \frac{\delta(M)}{c} \nu$, on a $|\frac{\delta(M)}{c} (\nu_0 - \nu_0 - \frac{\Delta \nu}{2})| = \frac{1}{2}$,
soit $\frac{\delta(M)}{c} \frac{\delta \nu}{2} = \frac{1}{2}$,
donnant $\delta(M) = \frac{c}{\Delta \nu} = \ell_c$.

Si $\delta < \ell_c$, le contraste sera bon, et sera très bas si $\delta$ est
plus grand que $\ell_c$.

#### Cas des trous d'Young en lumière blanche
Ayant $p(M) = \frac{ax}{D \lambda}$ et $i = \frac{\lambda D}{a}$, chaque $\lambda$ du spectre visible créé
a une figure d'interférence incohérente avec les alors qu'elles se superposent.
On obtient alors une frange blanche au milieu et des figures irisées sur le
reste, en atteignant parfois des raies "blanches d'ordre supérieur" quand elles
se superposent à nouveau.

#### Étude d'une raie spectrale
On considère une raie constituée d sources quasi monochromatiques de largeur
$d \nu$, incohérentes entre elles. On a donc $d I(M) = \int d I_\nu(M)$,
donnant $d I_\nu(M) = 2 d I_{0_\nu} (1 + \cos(\frac{2 \pi}{c} \nu \delta(M)))$
et $d I_{0_\nu} = g(\nu) d \nu$ (l'intensité de la source
quasi-monochromatique, une expression qui est valable de toute façon pour toute
forme de spectre $g$).

Comme la raie est rectangulaire, $g(\nu)$ est constante sur la raie, donc
l'intensité est uniforme sur $\Delta \gamma$, donnant une correspondance entre
$d \nu$ et $d I_{0_\nu}$, plus exactement $d I_{0_\nu} = \frac{I_0}{\Delta \nu} d \nu$.
On calcule alors $I(M) = \int\limits_{\nu_0 - \frac{\Delta \nu}{2}}^{\nu_0 + \frac{\Delta \nu}{2}} \frac{2 I_0}{\Delta \nu} (1 + \cos(\frac{2 \pi}{2}) \nu \delta) d \gamma$\
$= 2 I_0 (1 + \text{sinc}(\frac{\pi \Delta \nu \delta}{c}) \cos(\frac{2 \pi}{c} \nu_0 \delta))$.
Si $\Delta \nu$ tend vers $0$, on retrouve bien la formule de Fresnel originale.

On constate que le contraste diminue en s'éloignant de la frange centrale.

#### Étude d'un doublet
Soit deux sources monochromatiques incohérentes entre elles et disjointes,
on a $I(M) = I_{\lambda_0}(M) + I_{\lambda_0 + \Delta \lambda}(M)$
$= 2 I_0 (1 + \cos(\frac{2 \pi}{\lambda} \delta)) + 2 I_0 (1 + \cos(\frac{2 \pi}{\lambda_0 + \Delta \lambda} \delta))$
$= 4 I_0 (1 + \cos(\pi \delta (\frac{1}{\lambda_0} - \frac{1}{\lambda_0 + \Delta \lambda})) \cos(\pi \delta (\frac{1}{\lambda_0} - \frac{1}{\lambda_0 + \Delta \lambda})))$.

Quand $\Delta \lambda \ll \lambda_0$, on peut obtenir des identités plus simples
et
$I(M) \approx 4 I_0 (1 + \cos(\frac{\pi \Delta \lambda \delta}{\lambda_0^2}) \cos(\frac{2 \pi \delta}{\lambda_0}))$.
On observe alors un phénomène de battement où des zones de contraste $1$
alternent avec des zones de contraste nul, appelée anticoïncidence. Il faut
savoir retrouver leur période, ce qui peut se faire par l'utilisation de la
courbe ou simplement avec la différence d'ordre d'interférence. En effet, les
zones d'anticoïncidence correspondent à une différence d'ordre d'interférence de
$\frac{1}{2}$, et on cherche alors l'écart.
