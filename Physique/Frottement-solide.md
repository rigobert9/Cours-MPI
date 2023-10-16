# Frottements solides
## Contact entre 2 solides
### Modélisation : contact ponctuel
#### Modélisation
On définit le point de contact $I$ comme le point commun aux deux solides en
contact à leurs points $I_1$ et $I_2$ à un instant $t$. On note $\pi$ le plan
tangent au contact.

Ainsi, la vitesse des points $I$, $I_1$ et $I_2$ peuvent être différentes.

### Cas de la liaison plan-plan
Pour une liaison entre deux plans, on admet qu'on peut modéliser le contact par
un contact ponctuel. Reste à savoir ou placer ce point de contact.

Dans un contact réel, à cause de la déformation des matériaux, le contact se
fait toujours sur une surface $S'$ (toute la surface où les objets
s'aplatissent l'un contre l'autre).

#### Vitesse de glissement
Soit $\mathcal{S}_1$ et $\mathcal{S}_2$ en contact en $I$, la vitesse de
glissement s'écrit comme
$\overrightarrow{\rm V_{g_{\mathcal{S}_1} / \mathcal{S}_2}}(I) = \overrightarrow{\rm V}(I_2) - \overrightarrow{\rm V}(I_1)$.

Le glissement est une grandeur liée au mouvement relatif de $\mathcal{S}_2$ par
rapport à $\mathcal{S}_1$ et ne dépend pas du référentiel $\mathcal{R}$ d'étude.

Ce vecteur vitesse appartient toujours au plan tangent.

## Actions de contact entre deux solides
### Modélisation
#### Modélisation microscopique
On explique ces interactions par les forces de Van der Waals, qui correspondent
aux attractions et répulsions des dipôles électriques induits par les atomes au
bord des objets (attraction quand assez proche mais pas trop, répulsion quand
trop proche). La somme de ces forces microscopiques nous donnera la seule
résultante $\overrightarrow{\rm R}$ au point de contact qu'on étudiera.

#### Propriétés de $\overrightarrow{\rm R}$
On écrit $\overrightarrow{\rm R_{1 \to 2}} = \overrightarrow{\rm N_{1 \to 2}} + \overrightarrow{\rm T_{1 \to 2}}$,
avec $\overrightarrow{\rm N_{1 \to 2}}$ la réaction normales s'opposant à la
pénétration de $\mathcal{S}_2$ sur $\mathcal{S}_1$ et $\overrightarrow{\rm T_{1 \to 2}}$
la réaction tangentielle qui est une force dans $\pi$.

La réaction normale est une force passive qui s'adapte pour empêcher
l'interpénétration des solides. Lorsque sa norme devient nulle, c'est qu'il n'y
a plus de contact.

Le frottement tangentiel, lui, s'oppose au glissement entre les deux solides,
donnant $\overrightarrow{\rm T_{1 \to 2}} \cdot \overrightarrow{\rm V_{g_{\mathcal{S}_1 / \mathcal{S}_2}}}(I) \leq 0$.
Comme $\overrightarrow{\rm T}$ est la partie tangentielle, les deux vecteurs
sont colinéaires et on obtient une force négativement linéairement bornée en
la vitesse de glissement.

Dans le cas du modèle du contact ponctuel, le moment
des actions de contact est nul (cas particulier de la liaison pivot).

#### Loi d'action-réaction
$\overrightarrow{\rm R_{1 \to 2}} = - \overrightarrow{\rm R_{2 \to 1}}$
(et on peut décomposer la relation sur les composantes normales et tangentielles).

### Puissance des actions de contact
#### Expression générale
$P_\text{contact sur le système des deux solides} = P_{\overrightarrow{\rm R_{1 \to 2}}} + P_{\overrightarrow{\rm R_{2 \to 1}}}$\
$= \overrightarrow{\rm N_{1 \to 2}} (\overrightarrow{\rm V}(I_2) - \overrightarrow{\rm V}(I_1)) + \overrightarrow{\rm T_{1 \to 2}} (\overrightarrow{\rm V}(I_2) - \overrightarrow{\rm V}(I_1))$\
$= \overrightarrow{\rm N_{1 \to 2}} \cdot \overrightarrow{\rm v_{g_{\mathcal{S_1}/\mathcal{S_2}}}}(I) + \overrightarrow{\rm T_{1 \to 2}} \cdot \overrightarrow{\rm v_{g_{\mathcal{S_1}/\mathcal{S_2}}}}(I)$\
(puisque la réaction normale est perpendiculaire au plan tangent dans lequel est la vitesse de glissement) $= \overrightarrow{\rm T_{1 \to 2}} \cdot \overrightarrow{\rm v_{g_{\mathcal{S_1}/\mathcal{S_2}}}}(I)$

Attention, on obtient ainsi $P_\text{contact} = \overrightarrow{\rm T_{1 \to 2}} \cdot \overrightarrow{\rm V}(I_2) + \overrightarrow{\rm T_{2 \to 1}} \cdot \overrightarrow{\rm V}(I_1)$.

Les actions de contact diminuent l'énergie totale du système comprenant les deux
solides (ON NE PEUT PAS L'APPLIQUER À UN SEUL SOLIDE) : les frottement font
perdre de l'énergie au système globale.

Ainsi, si la puissance de contact est nulle, soit il n'y a pas de glissement,
soit il n'y a pas de frottement. Le premier cas se retrouve par exemple pour une
caisse posée sur un tapis roulant ou un vélo qui roule sans glisser. Le second
peut se retrouver dans le cas d'une caisse sur de la glace.

Le frottement s'oppose avant tout au glissement, tendant à lier les deux solides
ensemble.

#### Cas simplifié de $\mathcal{S_1}$ un support fixe
Dans ce cas, la puissance de contact est égale à la puissance de contact sur le
solide $\mathcal{S_2}$, qui perd nécessairement de l'énergie (car l'autre
puissance est nulle).

#### Liaison parfaite
On parle de liaison parfaite quand la puissance de contact est nulle pour tout
vecteur mouvement relatif entre les solides. Le frottement est alors nul.

#### Liaison pivot
> Une liaison pivot est une liaison qui ne laisse qu'un seul degré de liberté en
> rotation autour d'un axe $(o,\Delta)$.

On modélise alors les actions du milieu interstitiel entre ce qui est accroché
et le pivot (par exemple un roulement à billes) avec une réaction $\overrightarrow{\rm R}$
dont le point d'application est sur l'axe et par un couple de moment projeté
sur l'axe $C_\Delta = - \lambda \omega$.

Si une liaison pivot est parfaite, la puissance de contact du pivot est nulle,
donc la puissance de contact égale à la réaction $\cdot$ la vitesse en $O$ plus
$\overrightarrow{\rm C} \cdot \overrightarrow{\rm \omega}$, donnant $0 - \lambda \omega^2$.
Si la liaison est parfaite, alors on a $\lambda = 0$.

Par défaut, il faut dire qu'on la suppose parfaite, permettant de se débarrasser
d'un frottement liquide sur la rotation autour de l'axe.

## Loi phénoménologique sur le frottement de glissements : loi de Coulomb
(Loi phénoménologique, donc une loi observée expérimentalement)

### Expérience préliminaire
Soit une caisse glissant par terre.
Le vecteur $\overrightarrow{\rm R}$ peut être représenté, afin de satisfaire
l'hypothèse que la caisse ne bascule pas en étant poussée, comme venant d'un
point légèrement en avant du centre de gravité et au niveau du sol, avec la
valeur $T = F - mg$.

Si on augment peu à peu la force, la caisse commence par ne pas se déplacer du
tout avant un certain $F_\text{lim}$ car on a $F = T$, et ce jusqu'à ce que $F = F_\text{lim} = f_s N$.

Tant que la caisse est immobile (la vitesse est nulle), $|\overrightarrow{\rm T}| < f_s N$,
$\overrightarrow{\rm R}$ est dans un cône nommé cône d'adhérence, d'évasement $\alpha$ tel que
$\tan \alpha = \frac{T_\text{max}}{N} = f_s$. Si $F > F_\text{lim}$,
alors l'objet glisse et $\overrightarrow{\rm R}$ est collé à la surface d'un cône
de glissement et $T = f_d N$ (avec $\arctan(f_d)$ l'évasement de ce cône).

On constate que $\overrightarrow{\rm R}$ ne peut jamais sortir du cône
d'adhérence quand on ne glisse par et est sur le cône quand on glisse, donc on
approxime $f_s \approx f_d \approx f$. On les appelle respectivement
coefficients de frottement statique, de frottement dynamique et de frottement
(quand on admet que les deux sont égaux).

Sauf avis contraire, on prendre ces coefficients comme égaux.

### Les lois de Coulomb
Quand il n'y a pas glissement ($\overrightarrow{\rm v_{g_{2/1}}} = \overrightarrow{\rm 0}$),
on a $\| \overrightarrow{\rm T_{1 \to 2}} \| \leq f_s \| \overrightarrow{\rm N_{1 \to 2}} \|$.
S'il y a glissement, on a $\| \overrightarrow{\rm T_{1 \to 2}} \| = f_d \| \overrightarrow{\rm N_{1 \to 2}} \|$.

### Propriétés du coefficient de frottement
Valeurs classiques :
- Métal-métal : 0,1 - 0,2
- Bois-bois :  0,3 - 0,4
- Papier-papier : 0,5 - 0,5
- Bitume-pneu : 0,6 - 0,7

L'inégalité entre les deux coefficients crée les phénomènes de grincement de
gond, de crissement de craie.

## Application
### Roue motrice
Soit une roue de centre $O$, qui tourne à une vitesse angulaire $\omega$, avec
$I$ le point de contact avec le sol.

Si on ne connaît pas la direction de $\overrightarrow{\rm T}$, on pose $\overrightarrow{\rm T} = \overline{T} \overrightarrow{\rm u_x}$,
avec $\overline{T}$ une grandeur algébrique, permettant de l'inclure dans les
calculs. Autrement, on pose $\overrightarrow{\rm N}$, le couple de rotation de
la roue et le poids appliqué en $O$ à la roue.

On fait l'hypothèse qu'on étudie le démarrage de la roue sans glissement,
donc que $\overrightarrow{\rm v_{g_{\text{roue}/\text{sol}}}} = \overrightarrow{\rm 0}$
$= \overrightarrow{\rm v}(I \in \text{roue})$ (puisque le sol ne bouge pas).

Soit $R_\text{roue}$ le repère en translation vers $O$, on a $\overrightarrow{\rm v_{R_\text{sol}}}(I \in \text{roue})$\
$= \overrightarrow{\rm v_{R_\text{roue}}}(I \in \text{roue}) + \overrightarrow{\rm v_e}$\
$= - R \omega \overrightarrow{\rm e_x} + \overrightarrow{\rm v_\text{sol}}(O)$

On obtient donc finalement que la vitesse par rapport au sol de $O$
est de $R \omega \overrightarrow{\rm u_x}$ (ce qui a du sens).

En reprenant le RFD sur la roue, projeté en $\overrightarrow{\rm u_x}$, on a
$m \ddot{x} = T_{1 \to 2}$, et $0 = N_{1 \to 2} - mg$, donnant finalement que
$\overline{T}_{1 \to 2} > 0$ si $\ddot{x} > 0$.

On applique le théorème du moment cinétique en $G$ dans le référentiel de la
roue (on peut puisque dans ce référentiel, $G$ est immobile), en projetant sur
$\overrightarrow{\rm e_y}$. On a ainsi $J \frac{d \omega}{dt} = 0 + 0 + 0 - R \overline{T} + \Gamma_m$
(avec $\Gamma_m$ le couple du moteur).

Ainsi, on obtient le système $\left\{\begin{matrix} J \dot{\omega} = \Gamma_m - R T \\ m \ddot{x} = \overline{T} \\ \dot{x} = R \omega \end{matrix}\right.$,
donnant $J \frac{\ddot{x}}{R} = \Gamma_m - R m \ddot{x} \Rightarrow \ddot{x} = \frac{R \Gamma_m}{m R^2 + J}$.
On vérifie que notre hypothèse de roulement sans glissement tient (donc $\| \overrightarrow{\rm T} \| < f \| \overrightarrow{\rm N} \|$),
or $\overline{T} = \frac{m R \Gamma_m}{m R^2 + J}$ (et est finalement positif car la roue
avance). Comme $N = mg$, cette hypothèse est équivalente à $\Gamma_m < \frac{f g (n R^2 + J)}{R} = \Gamma_{m, \text{max}}$.
Il s'agit du couple moteur qui donne l'accélération maximale avant que les roues
glissent "inutilement" (sans ajouter d'accélération).

Ainsi, l'hypothèse inverse est l'étude dans le cas ou le couple moteur est plus
grande $\Gamma_{m,\text{max}}$, où l'accélération reste constante. On a alors
$m \ddot{x} = f m g \Rightarrow \ddot{x} = f g$, et $J \dot{\omega} = \Gamma_m - R f m g$,
soit $\omega = \frac{\Gamma_m - R f m g}{J} t$
