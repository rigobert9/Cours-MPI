# Équations de Maxwell, bilans d'énergie électromagnétique et ondes électromagnétiques
# Équations de Maxwell
## Rappel sur les équations locales
En électrostatique, on avait obtenu les équations locales suivantes :
- $\text{div} \overrightarrow{\rm E} = \frac{\rho}{\varepsilon_0}$ (Maxwell-Gauss) $\Rightarrow$ $\circ\!\!\!\!\!\!\iint_{S_G} \overrightarrow{\rm E} \cdot d \overrightarrow{\rm S} = \frac{Q_\text{int}}{\varepsilon_0}$
- $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm E} = 0$ $\Rightarrow$ $\circ\!\!\!\!\int_{\mathcal{C}} \overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} = 0$

De plus, on avait vu en magnétostatique :
- $\text{div} \overrightarrow{\rm B} = 0$ $\Rightarrow$ $\circ\!\!\!\!\!\!\iint_{S_G} \overrightarrow{\rm B} \cdot d \overrightarrow{\rm S} = 0$
- $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm B} = \mu_0 \overrightarrow{\rm j}$ $\Rightarrow$ $\circ\!\!\!\!\int_{\mathcal{C}} \overrightarrow{\rm B} \cdot d \overrightarrow{\rm \ell} = \mu_0 I_e$

On a vu pendant les démonstrations que des simplifications étaient possibles car
on se plaçait en statique, où les dérivées selon le temps sont nulles. Certains
résultats deviennent donc faux hors de la statique, d'autant plus qu'on pourrait
vouloir retrouver les résultats d'induction à deux variables évoqués l'année
dernière.

### Équation de conservation de charge

On avait de plus l'équation de continuité, aussi appelée équation de
conservation de la charge : $\frac{d Q_\text{int}(V)}{dt} = - \frac{\delta \overline{Q_T}(S_G)}{dt}$.
On peut la réécrire $\frac{d}{dt} (\iiint_V \rho d \tau) = - \circ\!\!\!\!\!\!\iint_{V} \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$,
donnant avec le théorème d'Ostrogradski
$\frac{d}{dt} (\iiint_V \rho d \tau) = - \iiint_V \text{div} \overrightarrow{\rm j} d \tau$,
donnant la forme finale 
$\frac{d}{dt} (\iiint_V \frac{\partial \rho}{\partial t} + \text{div} \overrightarrow{\rm j} d \tau) = 0$,
qu'on ramène à l'équation locale toujours vraie $\frac{\partial \rho}{\partial t} + \text{div} \overrightarrow{\rm j} = 0$.

### Équation de Faraday

Les deux équations sur les rotationnels ne sont donc valables qu'en statique, et
il faut prendre en compte dans le cas général le flux, comme avec la loi de
Faraday $e = - \frac{d \varphi_C}{dt}$.
La notion de potentiel ne peut alors plus définir la tension, et ne peut pas non
plus être le potentiel du champ électrique. On peut redéfinir la tension
comme la circulation du champ électrique, qui n'est désormais pas toujours nulle
sur un contour.

On cherche une forme locale pour la loi de Faraday, qu'on réécrit
$\circ\!\!\!\!\int_{\mathcal{C}} \overrightarrow{\rm E_\text{induit}} \cdot d \overrightarrow{\rm \ell} = - \frac{d}{dt} (\iint_{S_C} \overrightarrow{\rm B} \cdot d\overrightarrow{\rm S})$,
qu'on transforme avec Stokes en
$\iint_{S_C} \overrightarrow{\rm \text{rot}} \overrightarrow{\rm E_\text{induit}} \cdot d \overrightarrow{\rm S} = - \frac{d}{dt} (\iint_{S_C} \overrightarrow{\rm B} \cdot d\overrightarrow{\rm S})$,
donnant enfin $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm E} + \frac{\partial \overrightarrow{\rm B}}{\partial t} = \overrightarrow{\rm 0}$,
généralisant l'équation statique.

### Équation d'Ampère
L'équation du rotationnel de $\overrightarrow{\rm B}$ statique n'est aussi
valable qu'en statique, et on cherche donc une alternative qui respecte la
conservation de la charge en régime variable, qu'on prendra
comme $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm B} = \mu_0 (\overrightarrow{\rm j} + \varepsilon_0 \frac{\partial \overrightarrow{\rm E}}{\partial t})$.
On pose par homogénéité $\overrightarrow{\rm j_s} = \varepsilon_0 \frac{\partial \overrightarrow{\rm E}}{\partial t}$
le courant de déplacement.

On peut aussi utiliser le théorème d'Ampère généralisé,
$\circ\!\!\!\!\int_{\mathcal{C}} \overrightarrow{\rm B} \cdot d \overrightarrow{\rm \ell} = \mu_0 (I_e + I_{s_e})$,
avec $I_{s_e} = \iint_{S_C} \overrightarrow{\rm j_0} \cdot d \overrightarrow{\rm S}$.
On peut l'interpréter comme le fait qu'un champ électrique variable dans le
temps se comporte comme un courant, et crée un champ magnétique.

Le magnétisme et l'électricité sont donc un même champ. En électrostatique et en
magnétostatique, on applique l'ARQS soit électrique, soit magnétique (et on ne
peut pas faire les deux en même temps).

## Équations de Maxwell
On a rassemblé au cours des dernières parties les équations locales et intégrées
de Maxwell, qui sont toujours valables dans un modèle non quantique de
l'électromagnétisme.

$\rho$ et $\overrightarrow{\rm j}$ créent donc $\overrightarrow{\rm E}$ et $\overrightarrow{\rm B}$,
qui sont couplées par des variations temporelles. Mathématiquement, un champ est
déterminé par son rotationnel et sa divergence, donc les équations forment bien
un système complet (voire surdéterminé).

Les relations de passage sont toujours valables en régime variable à travers une
distribution surfacique. De plus, le champ électrique tangentiel est toujours
continu et le champ magnétique normal est toujours continu.

Enfin, pour une distribution volumique de charge, les deux champs sont toujours
continus.

Il est utile de retenir l'équation de la conservation de la charge, qui est
contenue dans l'équation de Maxwell-Ampère.

# Bilans d'énergie électromagnétique
## Bilan d'énergie électromagnétique, définition de la densité d'énergie électromagnétique
On note le vecteur de densité de courant d'énergie électromagnétique par un
vecteur $\overrightarrow{\rm R}$ ou $\overrightarrow{\rm \pi}$, aussi appelé
vecteur de Poynting, et on note la puissance électromagnétique absorbée $p_0$.

Un bilan d'énergie électromagnétique se fait sur un volume $V$ dans une surface
fermée de Gauss $S_G$. La variation d'énergie correspond donc aux échanges et
aux créations d'énergie, ce qu'on note
$\frac{d E_\text{elm}(V)}{dt} = - \frac{\delta \overline{E_\text{ext}}(S_G)}{dt} + \frac{\delta \overline{E_\text{créée}}(V)}{dt}$.

On peut définir simplement que $E_\text{elm}(V) = \iiint_V u_\text{elm} d \tau$
avec $u_\text{elm}$ une densité volumique d'énergie électromagnétique.
On définirait aussi $\frac{\delta E_\text{champ}(S_G)}{dt} = \circ\!\!\!\!\!\!\iint_{S_G} \overrightarrow{\rm j_{E_\text{elm}}} \cdot d \overrightarrow{\rm S}$
avec $\overrightarrow{\rm j_{E_\text{elm}}}$ un vecteur densité de courant
électromagnétique, qu'on note aussi $\overrightarrow{\rm \pi}$, le vecteur de
Poynting. On définit enfin $\frac{d E_\text{elm créée}(V)}{dt} = \iiint_V p_{v_\text{elm}} d \tau$
avec $p_{v_m}$ la puissance volumique créée.

On réécrit à l'aide du théorème Ostrogradski sur le second terme l'équation,
vraie sur tout volume,
$\iiint_V \frac{d u_\text{elm}}{dt} d \tau = - \iiint_V \text{div} \overrightarrow{\rm \pi} d \tau + \iiint_V p_{v_\text{elm}}$,
et donc l'équation locale associée
$\frac{d u_\text{elm}}{dt} + \text{div} \overrightarrow{\rm \pi} + p_{v_\text{créée}} = 0$,
qu'on appelle équation locale de Poynting ou équation locale de conservation de
l'énergie électromagnétique.

## Expression des termes
Il reste à exprimer concrètement $p_{v_\text{créée}}$, $\overrightarrow{\rm \pi}$
et $u_\text{elm}$.

$p_{v_\text{créée}}$ est la puissance électromagnétique volumique créée dans le
volume, créée par les charges. On cherche une grandeur qui traduit un échange
énergétique entre $(\rho, \overrightarrow{\rm j})$ et $(\overrightarrow{\rm E}, \overrightarrow{\rm B})$
(une interaction matière-rayonnement), qui se trouve dans la force de Lorentz.
On obtient $d \overrightarrow{\rm F_{\text{Lorentz}} \to d \tau} (\rho \overrightarrow{\rm E} + \overrightarrow{\rm j} \wedge \overrightarrow{\rm B}) d \tau$.
La puissance élémentaire de cette force est $\overrightarrow{\rm j} \cdot \overrightarrow{\rm E} d \tau$.
Cette puissance $\mathcal{P}_{d F_{\text{Lorentz}} \to d\tau}$ est la puissance
que les champs électromagnétiques donne aux charges contenues dans $d \tau$,
donc $\overrightarrow{\rm j} \cdot \overrightarrow{\rm E} = p_{v_\text{elm absorbée}}$,
et $p_{v_\text{elm créée}} = - \overrightarrow{\rm j} \cdot \overrightarrow{\rm E}$.
On a donc notre valeur, permettant de réécrire notre objectif en
$\frac{d u_\text{elm}}{dt} + \text{div} \overrightarrow{\rm \pi} + \overrightarrow{\rm j} \cdot \overrightarrow{\rm E} = 0$.

En développant $\overrightarrow{\rm j} \cdot \overrightarrow{\rm E}$ à l'aide
des équations de Maxwell, et en identifiant les résultats, on obtient
l'équation $\frac{d}{dt} (\frac{1}{2} \varepsilon_0 E^2 + \frac{B^2}{2 \mu_0}) + \text{div} \frac{\overrightarrow{\rm E} \wedge \overrightarrow{\rm B}}{\mu_0} + \overrightarrow{\rm j} \cdot \overrightarrow{\rm E} = 0$.
On exprime donc :
- La densité volumique d'énergie électromagnétique $u_\text{elm}$
  est de $\frac{1}{2} \varepsilon_0 E^2 + \frac{1}{2} \frac{1}{\mu_0} B^2 = u_e + u_m$,
  avec $u_e$ la densité volumique d'énergie électrique et
  $u_m$ la densité volumique d'énergie magnétique
- Le vecteur de Poynting, ou vecteur de densité de courant d'énergie
  électromagnétique, est $\overrightarrow{\rm \pi} = \frac{\overrightarrow{\rm E} \wedge \overrightarrow{\rm B}}{\mu_0}$,
  dont la puissance est $\iint_S \overrightarrow{\rm \pi} \cdot d \overrightarrow{\rm S} = \frac{\delta E_\text{elm}(\overrightarrow{\rm S})}{dt} = P_\text{rayonée}(\overrightarrow{\rm S})$.
- La puissance électromagnétique volumique créée en valeur absolue est $p_{v_\text{elm abs}}$
  $= \overrightarrow{\rm j} \cdot \overrightarrow{\rm E}$

## Bilan d'énergie dans une résistance $R$
On modélise une résistance par un cylindre d'un métal de conductivité $\gamma$.
On pose dans ce modèle une loi d'Ohm locale qui compare la conductivité à un
fluide qui ralentit linéairement le courant, $\overrightarrow{\rm j} = \gamma \overrightarrow{\rm E}$.
On suppose que $\overrightarrow{\rm j}$ est uniforme dans le conducteur,
et que le cylindre est de section $S$ et de hauteur $h$.

On a $I = \iint_S \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S} = + j \pi R^2 \Rightarrow \overrightarrow{\rm j} = \frac{-I}{\pi R^2} \overrightarrow{\rm e_z}$
pour un courant vers $- \overrightarrow{\rm e_z}$ avec une surface vers $- \overrightarrow{\rm e_z}$.
On a donc $R = \frac{U_{AB}}{I_{AB}} = \frac{- \overline{E} h}{I_{AB}}$, donnant
avec la loi d'Ohm $R = \frac{h}{\gamma \pi R^2} = \frac{h}{\gamma S}$.

On retrouve les champs à l'aide des symétries et invariances dans le cylindre
comme $\overrightarrow{\rm E} = \frac{- I}{\gamma \pi R^2} \overrightarrow{\rm e_z}$
et $\overrightarrow{\rm B}(r) = \left\{\begin{matrix} - \frac{\mu_0 I}{2 \pi r} \text{ si } r > R \\ - \mu_0 I \frac{r}{2 \pi R^2} \text{ si } r < R \end{matrix}\right.$.

On effectue enfin le bilan : $u_\text{elm} = \frac{1}{2} \varepsilon_0 \frac{I^2}{(\gamma \pi R^2)^2} + \frac{1}{2} \mu_0 (\frac{I^2}{4 \pi^2 R^4} r^2)$,
dont la dérivée de l'intégrale triple est nulle puisque $u_\text{elm}$ ne dépend
pas du temps. Le flux à travers la surface fermée du vecteur de Poynting, avec
le vecteur qui est $\overrightarrow{\rm \pi} = - \frac{\overline{E} \overline{B}}{\mu_0} \overrightarrow{\rm e_r}$,
est de $0 + 0 + \iint_{S_\text{contour}} \frac{- \overline{E(R)} \overline{B(R)}}{\mu_0} R d \theta d z$
$= \frac{I^2}{\gamma 2 \pi R^3} \int\limits_{0}^{2 \pi} \int\limits_{0}^{h} R d\theta dz$
$= R I^2$, qui est la puissance habituelle d'une résistance. Enfin
$\overrightarrow{\rm j} \cdot \overrightarrow{\rm E} = \frac{I^2}{\gamma \pi^2 R^4}$,
et on obtient en intégrant que la puissance absorbée est de $R I^2$.
Le bilan s'écrit donc $0 = RI^2 - RI^2$, qu'on interprète comme le fait
qu'il n'y ait pas de variation à l'intérieur de la résistance car la puissance
rayonnée sortante par les côtés est égale à l'opposé la puissance reçue à la matière.

# Ondes électromagnétiques dans le vide
## Équations d'onde
Dans le vide, $\rho = 0$ et $\overrightarrow{\rm j} = \overrightarrow{\rm 0}$,
donc $\text{div} \overrightarrow{\rm E} = 0$, $\text{div} \overrightarrow{\rm B} = 0$,
$\overrightarrow{\rm \text{rot}} \overrightarrow{\rm E} = - \frac{\partial \overrightarrow{\rm B}}{\partial t}$
et $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm B} = \mu_0 \varepsilon_0 \frac{\partial \overrightarrow{\rm E}}{\partial t}$.

On a $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm \text{rot}} \overrightarrow{\rm E} = \overrightarrow{\rm 0} s \Delta \overrightarrow{\rm E}$,
donnant $- \mu_0 \varepsilon_0 \frac{\partial^2 \overrightarrow{\rm E}}{\partial t^2} = - \Delta \overrightarrow{\rm E}$, une équation fondamentale pour notre problème.
De la même façon, on obtient $\Delta \overrightarrow{\rm B} - \mu_0 \varepsilon_0 \frac{\partial^2 \overrightarrow{\rm B}}{\partial t^2} = \overrightarrow{\rm 0}$.

Ces deux équations sont la même équation de d'Alembert, avec des constantes $\mu_0 \varepsilon_0$
qui sont de dimension $L^{-2} T^2$. On pose donc une constante de vitesse $c = \frac{1}{\sqrt{\mu_0 \varepsilon_0}}$,
qui est la vitesse de la lumière, puisque la lumière est une onde
électromagnétique.

## Formes des solutions possibles
### Ondes planes progressives
Une onde plane est une onde dont les surfaces d'onde sont des plans. En prenant
la variable $x$ dans la direction normale à ces plans, on a l'équation planaire
d'Alembert $\frac{\partial^2 s}{\partial x^2} - \frac{1}{c^2} \frac{\partial^2 s}{\partial t^2} = 0$.
En posant $u,v = x \mp ct$, on a $\frac{\partial^2 s}{\partial u \partial v} = 0$,
donnant $s(u,v) = f(u) + g(v)$, permettant de réécrire $s$ comme la somme de
deux ondes progressives à la vitesse $c$, l'une vers les $x$ croissants et
l'autre vers les $x$ décroissants.

### Ondes sphériques
Les surfaces d'onde étant sphériques, on obtient
$\Delta s = \frac{1}{r^2} \frac{\partial^2 (r^2 s)}{\partial r^2}$,
soit $\frac{1}{r} \frac{\partial^2 (r s)}{\partial r^2} - \frac{1}{c^2} \frac{\partial^2 s^2}{\partial t^2} = 0$,
donnant finalement $s(r,t) = \frac{f(r - ct)}{r} + \frac{g(r + ct)}{r}$,
c'est-à-dire la somme d'ondes progressives de vitesse $c$, l'une centrifuge et
l'autre centripète. Le facteur en $\frac{1}{r}$ traduit la conservation de
l'énergie, ce qui montre que le milieu est non absorbant (c'est le vide).

### Onde stationnaire
Une onde stationnaire est une onde qui se réécrit sous la forme
$s(M,t) = f(M) g(t)$.

Pour une onde stationnaire plane, on a alors l'équation de d'Alembert
$g(t) f''(x) = \frac{1}{c^2} f(x) g''(t)$, donnant après un peu de travail
$s(x,t) = S_0 \cos(\alpha x + \varphi) \cos(c \alpha t + \psi)$.

### Onde plane progressive sinusoïdale (OPPS) / harmonique (OPPH) / monochromatique (OPPM)
Une telle onde s'écrit $s = s_0 \cos(\overrightarrow{\rm k} \cdot \overrightarrow{\rm r} - \omega t + \varphi_0)$,
avec $s$ l'amplitude, $\varphi(M) = \overrightarrow{\rm k} \cdot \overrightarrow{\rm r} + \varphi_0$
la phase spatiale, $\varphi_0$ la phase à l'origine (qu'on peut décaler pour
être nulle si on étudie une seule onde, mais il est très important de prendre en
compte la différence de phase quand il y en a plusieurs), et $\varphi(M,t) =
\varphi(M) - \omega t$ la phase de l'onde. $\omega$ est la pulsation de l'onde,
et $\overrightarrow{\rm k}$ le vecteur d'onde (la pulsation spatiale).

Cette onde est alors périodique en $\lambda$ spatialement (dans le vide) et en $T$
temporellement. On note la vitesse de propagation, à la fois de l'onde vers les
$x$ croissants, mais aussi de la phase, comme $v_\varphi = \frac{\omega}{k}$.
On parle de vitesse de groupe pour $V_g = \frac{d \omega}{dk}$.

Dans un milieu linéaire, homogène, et isotrope, tout se passe comme dans le vide
à condition de remplacer $\varepsilon_0$ par $\varepsilon_0 \varepsilon_r$,
faisant le lien avec l'indice optique.

### Structure d'une OPPM dans le vide
On souvent écrire des dérivations spatiales sous la forme complexe. Pour un
champ scalaire $V$, le potentiel d'un champ $\overrightarrow{\rm E} = \overrightarrow{\rm E_0} e^{j (\overrightarrow{\rm k} \cdot \overrightarrow{\rm r} - \omega t)}$,
qui s'écrit donc $V_0 e^{j (\overrightarrow{\rm k} \cdot \overrightarrow{\rm r} - \omega t)}$,
on a $\overrightarrow{\rm \text{grad}} V = j \overrightarrow{\rm k} V$,
donnant avec $\overrightarrow{\rm \nabla} = j \overrightarrow{\rm k}$ ou $- j\overrightarrow{\rm k}$,
les formes habituelles $\text{div} \overrightarrow{\rm E} = \overrightarrow{\rm \nabla} \cdot \overrightarrow{\rm E}$
et $\overrightarrow{\rm \text{rot}} = \overrightarrow{\rm \nabla} \wedge \overrightarrow{\rm E}$.
De même, $\frac{d \overrightarrow{\rm E}}{dt} = j \omega \overrightarrow{\rm E}$
ou $- j \omega \overrightarrow{\rm E}$.

On détermine les propriétés des OPPM grâce aux équations de Maxwell.

####  $\overrightarrow{\rm E}$ et $\overrightarrow{\rm B}$ sont transverses
Puisque dans le vide, $\text{div} \overrightarrow{\rm E} = 0$, on a $\overrightarrow{\rm E} \perp \overrightarrow{\rm n}$,
montrant que le champ électrique est polarisé perpendiculairement à la direction
de propagation. De même, $\overrightarrow{\rm B} \perp \overrightarrow{\rm n}$.
Les deux champs sont donc transverses à la direction de propagation de l'OPPM.
De façon générale, les divergences vont permettre de déterminer la direction de
polarisation.

#### Lien entre $\overrightarrow{\rm E}$ et $\overrightarrow{\rm B}$
Les expressions des rotationnels donne la relation de structure des OPPM
dans tous les milieux $\overrightarrow{\rm B} = \frac{\overrightarrow{\rm k} \wedge \overrightarrow{\rm E}}{\omega}$.
Dans le vide, $\frac{\omega}{k} = c$, donnant $\overrightarrow{\rm B} = \frac{\overrightarrow{\rm n} \wedge \overrightarrow{\rm E}}{c}$.

Ainsi, $\overrightarrow{\rm k}$, $\overrightarrow{\rm E}$ et $\overrightarrow{\rm B}$ forment une famille orthogonale.

Un équation de dispersion est une relation entre $k$ et $\omega$, qu'on obtient
en injectant l'onde dans l'équation de propagation :
$\Delta \overrightarrow{\rm E} = \nabla^2 \overrightarrow{\rm E} = (j \overrightarrow{\rm k})^2 \overrightarrow{\rm E}$
donnant $- k^2 \overrightarrow{\rm E} - \mu_0 \varepsilon_0 (-j \omega)^2 \overrightarrow{\rm E} = 0$
donnant l'équation finale $k^2 = \mu_0 \varepsilon_0 \omega^2 = \frac{\omega^2}{c^2}$.