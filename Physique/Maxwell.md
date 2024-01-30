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

## Bilans d'énergie électromagnétique
### Bilan d'énergie électromagnétique, définition de la densité d'énergie électromagnétique
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

### Expression des termes
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

### Bilan d'énergie dans une résistance $R$
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
