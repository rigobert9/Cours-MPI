# Mécanique quantique
## Introduction
### Rappel historique sur les faits expérimentaux non expliqués par la mécanique classique
Planck, en 1900, introduit le quanta d'énergie $h \nu$ entre la matière et le
rayonnement pour expliquer la "catastrophe ultraviolette" qui se trouvait dans
la différence entre le modèle du corps noir à certaines longueurs d'onde et
l'expérience.

En 1905, Einstein étudie l'effet photoélectrique et retrouve des quantas
identiques, rétablissant une théorie corpusculaire de la lumière qui mènera à
une théorie hybride. De nombreux modèles essaient par la suite de représenter
les quantifications de niveaux d'énergie dans l'atome (comme le premier modèle
de Bohr pour l'hydrogène).

La dualité onde-corpuscule, proposée par Louis de Broglie en 1923, s'est
observée seulement 40 ans plus tard par des expériences de diffraction
d'électrons avec un réseau cristallin, puis des trous d'Young sur les électrons,
photons, et même atomes.

### Dualité onde-corpuscule
> $E = h \nu$
> $\overrightarrow{\rm p} = \hbar \overrightarrow{\rm k} = \frac{h}{\lambda} \overrightarrow{\rm u}$

On appelle $\overrightarrow{\rm p}$ et $E$ les grandeurs corpusculaires de la
particule, et $\overrightarrow{\rm k}$ et $\omega$ les grandeurs ondulatoires de
la particule.

Attention, la particule est une onde mais pas nécessairement une onde
électromagnétique.

### Conditions d'utilisation de la mécanique quantique
On admet que l'on peut expliquer la trajectoire des particules en mécanique
classique tant que $\lambda_\text{DB} \ll L_\text{Caractéristique de l'étude}$.
Quand on étudie un phénomène quantifié par un entier $n$, on retrouve pour la
plupart des théories les résultats classiques en $n \to +\infty$.

Quand une grandeur homogène à $h$ (une action) liée à la particule est grande
devant $h$, la particule se comporte comme dans les modèles classiques. C'est le
cas aussi du moment cinétique. On peut donc aussi arriver aux résultats
classiques en faisant tendre $h \to 0$.

## Dualité onde-corpuscule : la fonction d'onde
### Définition, interprétation, propriété
> L'état physique d'un quanton est entièrement par une fonction complexe du
> temps et de l'espace $\Psi(M,t)$. On appelle cette fonction fonction d'onde du
> quanton.

__Interprétations :__
- $\Psi(M,t)$ est l'amplitude de probabilité de présence
- $\rho(M,t) = |\Psi(M,t)|^2$ est la densité volumique de probabilité de présence,
  avec $dP = \rho(M,t) d \tau$ la probabilité de trouver le quanton dans $d \tau$ autour de $M$
  à l'instant $t$

Puisque seule $\rho(M,t)$ est mesurable, on définit $\psi(M,t)$ à $e^{i \alpha}$
près

Le quanton se trouvant quelque part, l'intégrale de $\rho(M,t)$ sur tout
l'espace a une valeur de $1$ : on parle de fonction d'onde normalisée.

$[\Psi] = L^{-\frac{3}{2}}$, car $[|\Psi|^2] = L^{-3}$.

La fonction d'onde est continue spatialement.

Au programme, on étudiera le plus souvent des quantons contraints à sa déplacer
sur un axe $(Ox)$, et on définira donc une fonction d'onde linéïque $\Psi(x,t)$,
qui est alors de dimension $L^{-\frac{1}{2}}$ car sa densité de probabilité de
présence est linéïque.

### Utilisation de $\Psi$ et retour sur son interprétation
#### Évaluation de la grandeur imaginaire d'une propriété fonction de $x$ lié au quanton
On calcule toutes ces fonction associée à $x$ à travers une moyenne (par une
intégrale) pondérée par les densités de probabilité de présence.

#### Interprétation statistique
Une expérience sur un quanton donne un résultat probabiliste, mais en répétant
un grand nombre de fois les expériences avec des quantons "préparés" de manière
identique, l'étude statistique permet d'interpréter l'effet probabiliste.

#### Retour sur les trous d'Young
Dans une expérience ou on envoie un quanton sur les trous d'Young, on admet que
quand un quanton est dans une superposition d'état $A$ et $B$ :
- Si les deux états sont discernables alors on somme les probabilités de
  présence
- Si les deux états sont indiscernables on somme les amplitudes

Si on sait expérimentalement par quel trous est passé le quanton, alors on ne
voit palus les franges d'interférence. Sinon, on peut obtenir la probabilité de
présence à partir d'un analogue de la formule de Fresnel :
$d P_{A + B} = d P_A + d P_B + 2 \sqrt{dP_A dP_B} \cos(\varphi_a - \varphi_B)$.

#### Remarques sur la mesure
La mécanique quantique est une théorie où l'expérimentateur influence l'objet de
sa mesure, car il modifie l'état de l'objet en le mesurant (par example, une
caméra nécessite d'envoyer des photons). On parle de réduction du paquet d'onde.

### Fonction d'onde de De Broglie
Par analogie avec les ondes électromagnétiques, on définit un quanton dit de De
Broglie par une fonction d'onde $\Phi_\text{DB}(x,t) = A e^{j(kx - \omega t)}$
(avec les variables dans ce sens là !).

Le terme exponentiel doit être écrit exactement dans ce sens : il ne s'agit pas
d'un "passage aux complexes" mais bien d'une solution complexe. Ces fonctions
d'onde sont l'analogue d'une OPPM, et n'existent pas non plus : elle ne sont pas
normalisables. En revanche, elles forment aussi une base des quantons réels.

On sait que $k = \frac{p}{\hbar}$, $\omega = \frac{E}{\hbar}$, soit
$\Psi_\text{DB} = A e^{j(\frac{p}{\hbar} x - \frac{E}{\hbar} t)}$. Un quanton de
De Broglie a une énergie $E$ et une quantité de mouvement $p$ parfaitement
définies.

Le quanton associé à cette onde possède une équation de dispersion qui dépend
de son état. Par exemple, pour un quanton isolé dans le vide non relativiste,
$E = E_c + E_p = E_c + 0 = \frac{p^2}{2m}$, soit $\hbar \omega = \frac{\hbar^2 k^2}{2m}$
$\Rightarrow \omega = \frac{\hbar k^2}{2m}$. Un autre exemple, le quanton
relativiste isolé, donne $E = \sqrt{\rho^2 c^2 + m^2 c^{4}}$, soit pour un
quanton de masse nulle $E = \rho c \Rightarrow \omega = k c \Rightarrow \frac{\omega}{k} = c$.
L'équation de dispersion d'un quanton non relativiste isolé donne $v_\varphi = \frac{\omega}{k} = \frac{\hbar k}{2m}$
$= \frac{p}{2m} = \frac{V}{z}$ et $v_g = \frac{d \omega}{dk} = \frac{k}{m} = v$.

Ainsi, les quantons de De Broglie n'existent pas mais leur interprétation est
riche.

### Notion de paquet d'onde
Par analogie avec les ondes électromagnétiques et grâce à la transformée de
Fourier, on peut définir un quanton réel à l'aide d'un "paquet d'onde", superposition
d'une infinité de quantons de De Broglie.

Un quanton réel n'a pas un énergie ou une vitesse, mais a une probabilité
d'avoir un grand nombre d'énergies ou de vitesses différentes. On s'intéresse
donc à $<E>$ et $<p>$.

Par la propriété fondamentale de la transformée de Fourier,
$\Delta x \Delta k \approx 1$, donc $\Deltax x \Delta (\frac{p}{\hbar}) \approx 1$,
soit $\Delta x \Delta p \approx \hbar$, donnant une version approximative du
plus exact théorème d'incertitude d'Heisenberg.

### Relation d'indétermination d'Heisenberg
#### Relation d'indétermination spatiale d'Heisenberg (1927)
La mesure de la position $x$ et de la quantité de mouvement $p_x$ d'un quanton
possèdent des incertitudes fondamentales liées par $\Delta p_x \Delta x \geq \frac{\hbar}{2} = \frac{h}{4 \pi}$.
Dans cette inégalité, $\Delta x$ et $\Delta p_x$ sont les écarts types des des
mesures de $x$ et $p_x$, avec $(\Delta p_x)^2 = <p_x^2> - <p_x>^2$.

On peut généraliser ce théorème à chaque dimension de l'espace.

#### Exemples d'utilisation des inégalités d'Heisenberg
##### Diffraction
Soit une particule passant par un trou de largeur $a$, à une vitesse $\overrightarrow{\rm v_0}$,
celle-ci peut sortir du trou avec une vitesse formant un angle jusqu'à $\alpha$
avec $\overrightarrow{\rm v_0}$. Comme la particule est nécessairement dans la
fente, soit $\Delta y \approx a$, on a $\Delta p_y \approx \frac{\hbar}{a}$.
Or, $p_y = m v_y = m v_0 \sin(\alpha)$, soit $\Delta p_y \approx m v_0 \Delta \sin \alpha \approx m v_0 \Delta \alpha$,
donc $m v_0 \Delta \alpha \approx \frac{\hbar}{a}$, donnant avec $m v_0 = p = \frac{h}{\lambda}$,
soit $\theta = \Delta \alpha \approx \frac{\lambda}{a} \times \frac{1}{2 \pi}$.

##### Énergie cinétique d'une particule libre dans une boîte
En admettant une particule libre quantique dans une boîte de dimensions $\Delta
x, \Delta y, \Delta z$. En utilisant l'inégalité d'Heisenberg, on obtient
en ayant par symétrie $<p_x> = <p_y> = <p_z> = 0$ (sinon la particule sort de la
boîte) et donc que $(\Delta p_x)^2 = <p_x^2>$, que $<E> = \frac{(\Delta p_x)^2}{2m} + \frac{(\Delta p_y)^2}{2m} + \frac{(\Delta p_z)^2}{2m}$
$\geq \frac{\hbar}{8} (\frac{1}{(\Delta x)^2 + \frac{1}{(\Delta y)^2} + \frac{1}{(\Delta z)^2}})$,
et a donc une énergie cinétique minimale.

##### Énergie minimum d'un oscillateur harmonique
Soit un quanton en interaction tel que $V = E_p = \frac{1}{2} m \omega_0^2 x^2$,
son énergie totale est $E = E_c + E_p = \frac{p_x^2}{2 m} + \frac{1}{2} m \omega_0^2 x^2$,
donc comme par symétrie $<x> = 0$ et $<p_x> = 0$,
$<E> = \frac{(\Delta p_x)^2}{2m} + \frac{1}{2} m \omega_0^2 (\Delta x)^2$
$\geq (\text{Heisenberg}) \frac{\hbar^2}{8 m (\Delta x)^2} + \frac{1}{2} m \omega_0^2 (\Delta x)^2$.
En analysant la dérivée de ce minorant, on obtient que son maximum selon $\Delta x$ nous
contraint à avoir $<E> > E_\text{min} = \frac{1}{2} \hbar \omega_0$

### Vecteur densité de courant de probabilité
Soit une grandeur physique $G$, et $g = \frac{d G}{d \tau}$ est sa grandeur
volumique et $\overrightarrow{\rm j_G} = g \overrightarrow{\rm v}$ est le
vecteur densité de courant de $G$, donnant $\overrightarrow{\rm j_G} \cdot d \overrightarrow{\rm S} = \frac{\delta \overline{G_T}}{dt} d \overrightarrow{\rm S}$.

Cette fois-ci, on prend $G$ la probabilité de présence et $g = \rho = |\Psi|^2$.

On a $\frac{\partial g}{\partial t} + div \overrightarrow{\rm j_G} = 0$ (si pas
de création de la grandeur), nous donnant un principe de conservation de charge.

On admet que pour un quanton de De Broglie, on pose un vecteur $\overrightarrow{\rm J}$
de densité de courant de probabilité $\overrightarrow{\rm J} = \rho \overrightarrow{\rm v_g} = |\Psi|^2 \frac{\hbar \overrightarrow{\rm k}}{m}$.
