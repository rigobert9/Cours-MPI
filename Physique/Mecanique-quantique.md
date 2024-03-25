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
$\Delta x \Delta k \approx 1$, donc $\Delta x \Delta (\frac{p}{\hbar}) \approx 1$,
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

## Équation de Schrödinger (1926), dynamique de la fonction d'onde
> Dans le cas où un quanton évolue dans un milieu dans lequel il a une énergie
> potentielle (qu'on appelle "potentiel" en mécanique quantique) $E_p = V(x,t)$,
> sa fonction d'onde $\Psi$ vérifie l'équation
> $j \hbar \frac{\partial \Psi}{\partial t} = - \frac{\hbar^2}{2 m} \frac{\partial^2 \Psi}{\partial x^2} + V(x,t) \Psi$.

On peut essayer de retrouver l'équation à partir de l'injection d'un quanton de
De Broglie dans l'équation. Le principe correspond alors simplement à la
conservation de l'énergie.

En trois dimension, on a
$j \hbar \frac{\partial \Psi}{\partial t} = - \frac{\hbar^2}{2 m} \Delta \Psi + V(x,t) \Psi$.

On introduit l'opérateur hamiltonien $\hat{H}(f) = - \frac{\hbar^2}{2 m} \Delta f + V \times f$.

Puisque l'équation de Schrödinger est linéaire d'ordre, on peut facilement
construire des solutions supplémentaires par superposition.

### Résolution de l'équation de Schrödinger indépendante du temps
On se place dans le cas ou $E_p$ ne dépend que de la position et pas du temps.

La méthode de la séparation des variables nous fait chercher des solution $\Psi(x,t)$
$= f(x) g(t)$. On obtient alors $j \hbar f(x) g'(t) = - \frac{\hbar}{2 m} f''(x) g(t) + V f(x) g(t)$,
donnant $j \hbar f(x) \frac{g'(t)}{g(t)} = - \frac{\hbar}{2 m} \frac{f''(x)}{f(x)} + V = E$,
avec $E$ l'énergie de la particule comme on peut l'observer dans le cas d'un
quanton de De Broglie. On a finalement
$\left\{\begin{matrix} g'(t) = - j \frac{E}{\hbar} g(t) \\ - \frac{\hbar^2}{2 m} f''(x) + V(x) f(x) = E f(x) \end{matrix}\right.$.

### États stationnaires
> On appelle états stationnaires de l'équation de Schrödinger les fonctions d'onde
> solution de la forme $\Psi_\text{es}(x,t) = \varphi_s(x) e^{- j \omega t}$, avec
> $\hbar \omega = E$, et $\varphi_s$ vérifiant $\hat{H}(\varphi_s) = E \varphi_s$.

Comme $\varphi_s$ est indépendante du temps pour un état stationnaire, il s'agit
d'un vecteur propre de $\hat{H}$ de valeur propre $E$. Les états stationnaires
sont donc une base orthonormée de vecteur propres pour toutes les solutions.

Si plusieurs vecteurs propres ont la même valeur propre alors on parle de
"dégénérescence de l'ordre".

> Les états stationnaires solution de l'équation de Schrödinger indépendante du
> temps forment une base des solutions.

On peut choisir les $\varphi_s$ comme une base orthonormée pour le produit
scalaire $\int\limits_{-\infty}^{+\infty} f^{\ast} g$ en prenant les $\varphi_s$
normalisés (donc de probabilité de présence normalisée).

La fonction d'onde d'un état stationnaire $\varphi_s(x,t)$ est continue et
bornée. Dans le cas où $V(x)$ est continue et bornée, alors $\frac{d \varphi_s}{dx}$ est
continue et bornée (ce qu'on démontre en intégrant l'équation de Schrödinger sur
un intervalle infinitésimal).

Si le problème est symétrique autour de $O$, c'est à dire que $V(x)$ est pair,
alors $\varphi_s(x)$ est soit paire soit impaire.

### Superposition de deux états stationnaires
On "prépare" un quanton dans un état correspondant à la superposition de deux
états stationnaires $\varphi_{s_1}$ et $\varphi_{s_2}$. Ainsi, on a
$\Psi(x,t) = \alpha_1 \varphi_{s_1}(x) e^{- j \frac{E_1}{\hbar} t} + \alpha_2 \varphi_{s_2} e^{- j \frac{E_2}{\hbar} t}$.
Les deux états stationnaires étant orthogonaux, la superposition est normalisée
si et seulement si $|\alpha_1|^2 + |\alpha_2|^2$. On choisit $\alpha_1 = \frac{1}{\nu_1}$
et $\alpha_2 = \frac{1}{\nu_2}$.

Le quanton est donc dans un état de superposition avec
$\Psi(x,t) = \frac{1}{2} (\rho_1 + \rho_2 + \varphi_{s_2} \varphi_{s_1}^{\ast} e^{- j \frac{E_2 - E_1}{\hbar} t} + \varphi_{s_2}^{\ast} \varphi_{s_1} e^{j \frac{E_2 - E_1}{\hbar} t})$
$= \frac{1}{2} (\rho_1 + \rho_2 + 2 |\varphi_{s_1}^{\ast} \varphi_{s_2}| \cos(\frac{E_2 - E_1}{\hbar} t - arg(\varphi_{s_1}^{\ast} \varphi_{s_2})))$.

Un quanton en superposition de deux états stationnaires oscille entre deux états
avec une pulsation $\omega_0 = \frac{E_2 - E_1}{\hbar}$.

## Applications
### Formes des solutions en fonction du signe de $V - E$
#### Remarque préliminaire
On va étudier des dispositifs où le potentiel (l'énergie potentielle) du quanton
est constant par morceaux. Si $\lambda_\text{DB} \gg L$, avec $L$ une distance
caractéristique de variation de $V(x)$, le quanton voit une discontinuité.

#### Résolution de l'équation de Schrödinger
On cherche les états stationnaires, de la forme $\Psi_\text{es}(x,t)$
$= \varphi_s(x) e^{- i \frac{E}{\hbar} t}$. On cherche à résoudre l'équation de
Schrödinger spatiale $- \frac{\hbar^2}{2 m} \frac{d^2 \varphi_s}{dx^2} + V \varphi_s(x) = E \varphi_s(x)$
$\Leftrightarrow \frac{d^2 \varphi_s}{dx^2} + \frac{2m}{\hbar^2} (E - V) \varphi_s = 0$.

Si $V$ est constant, on a deux cas :
- Si $V < E$, $\varphi_s(x) = \underline{A} e^{i k x} + \underline{B} e^{- i k x}$
  $= \underline{A'} \cos(kx) + \underline{B'} \sin(kx)$ avec $k = \sqrt{\frac{2 m (E - V)}{\hbar^2}}$
- Si $E < V, \varphi_s(x) = \underline{A} e^{K x} + \underline{B} e^{- Kx}$ avec
  $K = \sqrt{\frac{2 m (V - E)}{\hbar^2}}$

Dans le second cas est une configuration purement quantique, qui ne peut pas
s'interpréter en mécanique classique : en effet, dans ce cas, un quanton peut
pénétrer dans une zone où son énergie est inférieure à $E_p$. Sa probabilité de
présence est exponentiellement décroissante, et on peut alors réécrire la
solution avec $\underline{A}$ et $\underline{B}$ qui disparaissent
respectivement en $-\infty$ et $+\infty$. Ces quantons ont une probabilité de
présence non nulle seulement dans une épaisseur de quelques $\delta = \frac{1}{K}$.

### Puits infini
On considère un potentiel $V(x)$ nul dans $[0;L]$ et infini en dehors.
Ainsi, l'équation d'onde stationnaire du quanton dans ce puits est nulle hors du
puits. De plus $\varphi_s(x)$ est continue en $0$ et $L$, bien que sa dérivée ne
soit pas continue, car le potentiel est infini.

On résout $\frac{d^2 \varphi_s}{d x^2} + \frac{2 m}{\hbar^2} (E - V) \varphi_s = 0$.
Dans le cas où $E < V$, on ne peut pas réaliser les conditions initiales,
donc on a $E > V \geq 0$ (dans les cas de diffusion, on sélectionne la forme
exponentielle, et on prend la forme trigonométrique dans les cas liés).

Les conditions aux limites donnent alors $\varphi_S(x) = B sin(k x)$,
avec un $k$ tel que $k L = n \pi$ avec $n \in \mathbb{N}$, quantifiant les
fonctions d'onde possibles : on a donc $\sqrt{\frac{2m E}{\hbar^2}} = \frac{n \pi}{2}$,
soit des $E$ de la forme $E = \frac{n^2 \pi^2 \hbar^2}{2 m L^2} = \frac{n^2 h^2}{8 m L^2}$.
La condition de normalisation donne que $|B| = \sqrt{\frac{2}{L}}$, et donc
$B = \sqrt{\frac{2}{L}} e^{i \alpha}$. On choisit $\alpha = 0$.

Au final, les états stationnaires du quanton dans le puits infini sont
les $\left\{\begin{matrix} \Phi_{\text{ES}_n}(x,t) = \sqrt{\frac{2}{L}} sin(n \frac{\pi}{L} x) e^{-i \frac{E_n}{\hbar} t \\ E_n = \frac{n^2 h^2}{8 m L^2}} \end{matrix}\right.$.
Toutes solution réelle s'écrit donc comme la combinaison linéaires infinie
normalisée de ces solutions.

- Pour chaque $E_n$, il n'y a qu'un $\varphi_{S_n}(x)$ (donc il n'y a pas
  dégénérescence de l'ordre)
- En mécanique quantique, les conditions aux limites peuvent avoir pour
  conséquence une quantification de l'énergie, en confinant une onde et en la
  faisant se comporter comme une corde vibrante
- Un changement de repère permet de mettre le centre en $0$
