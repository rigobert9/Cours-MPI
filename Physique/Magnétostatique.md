# Magnétostatique
## Généralités sur la magnétostatique
### Introduction
On introduit $\overrightarrow{\rm B}$ grâce à la partie magnétique de la force
de Lorentz. L'unité SI de son intensité est le Tesla, mais les valeurs sont
souvent de l'ordre de $10^{-2}$ : le champ électromagnétique terrestre est de
$0,2 \times 10^{-4} T$, un magnet a une intensité $10^{-3} - 10^{-1}$, un
électroaimant a une intensité entre $10^{-2} - 1 T$, et les électroaimant avec
des supraconducteurs dans les réacteurs nucléaires et dispositifs à haute
énergie ont une intensité de $50 T$. On utilise donc souvent le Gauss, qui est
tel que $1 \text{Gauss} = 10^{-4} T$.

### Historique
La magnétite ($Fe_2 O_3$) est un matériau magnétique trouvé dans la nature,
connu depuis l'antiquité. La conception des boussoles a mis en évidence le champ
magnétique terrestre. En 1870, on met en évidence un lien entre le courant
électrique et les aimants, puis on obtient des mises en évidence dans les
circuits électriques de l'induction.

De façon générale, le champ magnétique est créé par les charges en mouvement, et
le champ magnétique agit sur les charges en mouvement. Ainsi, il est
techniquement impossible d'étudier l'électrostatique sans magnétisme, et
inversement, mais il est un réalité possible de faire l'approximation car le
courant se fait dans un conducteur.

### Modélisation du courant électrique
On appelle courant électrique tout mouvement macroscopique de charge. Il est
alors important de ne pas confondre la notion individuelle de vitesse d'une
charge, et la notion statistique de vitesse moyenne quadratique. La vitesse
instantanée d'une charge est de l'ordre de $10^3 m \cdot s^{-1}$, tandis que la
vitesse quadratique moyenne de toutes les charges est de l'ordre du millimètre
par seconde.

On définit l'intensité du courant électrique qui traverse une surface $\overrightarrow{\rm S}$
par $I(\overrightarrow{\rm S}) = \frac{\delta q_T(\overrightarrow{\rm S})}{dt}$.

On montre cette expression de $I(\overrightarrow{\rm S})$. Soit des porteurs de
charge d'un seul type, et tous homocinétiques (de même mouvement tout le temps)
de vitesse $\overrightarrow{\rm V}$. Soit le cylindre d'axe $(O,\overrightarrow{\rm V})$
et de longueur $V dt$ qui s'appuie sur $d \overrightarrow{\rm S}$ (un cylindre
en biais). Une charge traverse $d \overrightarrow{\rm S}$ pendant $dt$ si elle
est dans ce cylindre.\
Pour $S'$ le section du cylindre, $\delta q_T(\overrightarrow{\rm S'}) = n V \times q$
avec $n$ la densité volumique des charges et $V$ le volume du cylindre. Or
$d S' = dS \cos(\theta)$, donnant $V = v dt dS \cos(\theta) = \overrightarrow{\rm v} \cdot d \overrightarrow{\rm S} dt$,
soit $\delta q_T(d \overrightarrow{\rm S}) = n \overrightarrow{\rm v} \cdot d \overrightarrow{\rm S} dt q$,
donc $d I(d \overrightarrow{\rm S}) = n q \overrightarrow{\rm v} \cdot d \overrightarrow{\rm S}$.
On définit le vecteur densité de courant volumique de charge comme $\overrightarrow{\rm j} = n q \overrightarrow{\rm v}$.\
Finalement, $d I (d \overrightarrow{\rm S}) = \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$,
soit $I(\overrightarrow{\rm S}) = \iint_S \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$.
On obtient quelque chose de similaire même s'il y a plusieurs types de charges.

### Raisonnement élémentaire à utiliser
Pour un petit bout de fil électrique parcouru par un courant $I$, on travaillera
souvent avec un modèle simplifié filiforme. Puisqu'on a $I = \overrightarrow{\rm j} \cdot \overrightarrow{\rm s}$,
on a $I d \overrightarrow{\rm \ell} = (\overrightarrow{\rm j} \cdot \overrightarrow{\rm s}) d \overrightarrow{\rm \ell}$
donnant $I d \overrightarrow{\rm \ell} = \overrightarrow{\rm j} d \tau$.

Cette dernière équation permet d'utiliser les connaissances en induction de
première année, comme la force de Laplace notée
$d \overrightarrow{\rm F_L} = \overrightarrow{\rm j} \cdot d \overrightarrow{\rm \ell} \wedge \overrightarrow{\rm B}$.

### Modèles de courant
On peut en tout cas travailler avec le courant volumique dans tous les modèles
de charge.

Pour le modèle volumique, $I = \iint \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$.
Le modèle surfacique est hors programme mais peut se retrouver aisément. Le
modèle filiforme est le précédent. Enfin, une charge potentielle en mouvement
produit un courant de $I = \frac{q}{T} = \frac{q V}{2 \pi r}$ (en faisant bien attention à l'orientation).

### Propriété de continuité, de symétrie et d'invariance
#### Continuité
Seule la modélisation volumique est réaliste, dans le sens où $\overrightarrow{\rm B}$ est continu.
Les modèles surfacique et linéïque sont approximés dans le sens où $\overrightarrow{\rm B}$ n'est pas continu au niveau
des sources de champ magnétique.

#### Symétrie
Le champ magnétique est antisymétrique. Les axes de symétrie du courant donnent
donc l'opposé du symétrique du vecteur de l'autre côté des symétries. Ainsi, le
champ magnétique est perpendiculaire aux plans de symétrie, et le champ magnétique
dans les plans d'antisymétrie appartient au plan d'antisymétrie.

#### Invariances
$\overrightarrow{\rm B}$ possède les mêmes invariances que le courant.

#### Lignes de champ
Les lignes de champ appartiennent aux plans d'antisymétrie, se coupent
uniquement aux points $\overrightarrow{\rm B} = 0$, et forment des courbes
fermées qui s'enroulent autour des courants. Leur orientation dépend de
l'orientation de la règle de la main droite.

## Lois de la magnétostatique
### Lois sur le flux de $\overrightarrow{\rm B}$
#### Le champ magnétique est à flux conservatif
$\circ \!\!\!\!\!\! \iint_{S_G} \overrightarrow{\rm B} \cdot d \overrightarrow{\rm S} = 0$

#### Conséquence
Comme $\overrightarrow{\rm B}$ est à flux conservatif, $\overrightarrow{\rm B}$
est constant le long d'un tube de champ.

On doit savoir démontrer cette propriété : si on prend deux contours successifs
sur lequel s'appuie un tube de champ, on obtient en prenant le volume entre les
deux que le contour du tube a un flux nul, et donc que les deux bouts du tube
reçoivent un même flux (attention aux orientations !).

Ainsi, si les lignes de champ se resserrent (façon tuyau d'arrosage), $\overrightarrow{\rm B}$
croît, et inversement. Dans tous les cas, on retiendra que $B S$ (le champ
magnétique fois la surface) est constante le long d'un tube de champ.

#### Équation locale
En utilisant à nouveau le théorème d'Ostrogradski, on adapte la loi en
$\iiint_{V_G} \text{div} \overrightarrow{\rm B} d \tau = 0$, donnant l'équation
locale $\text{div} \overrightarrow{\rm B} = 0$ (Maxwell-flux/Maxwell-Thompson).

### Loi sur la circulation de $\overrightarrow{\rm B}$
On a vu que $\overrightarrow{\rm B} \propto I$ et que les lignes de champ $\overrightarrow{\rm B}$
s'enroulent autour de $I$, ce qui s'explique par le théorème d'Ampère :
$\circ \!\!\!\! \int_C \overrightarrow{\rm B} \cdot d \overrightarrow{\rm l} = \mu_0 I_\text{enlacé}$
(avec $\mu_0$ la perméabilité magnétique du vide, de dimension $MLT^{-2}I^{-2}$).

Pour l'appliquer, il est nécessaire de définir $I_\text{enlacé}$ et son signe.

#### Définition et unicité de $I_\text{enlacé}$ (conservation de la charge)
On choisit de définir ce $I_\text{enlacé}$ comme le flux de la densité de
courant volumique à travers une surface s'appuyant sur le contour. Mais il
existe un infinité de ces surfaces. Pour obtenir une définition, il est donc
nécessaire que ce flux ne dépende pas de la surface.

##### Preuve d'unicité et équation locale de conservation de charge
Or, si on prend deux surfaces différentes $S_{C_1}$ et $S_{C_2}$, on veut
obtenir $\iint_{S_{C_1}} \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S_{C_1}} = \iint_{S_{C_2}} \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S_{C_2}}$.
Or, ces surfaces forment une surface fermée qui définit un volume.
On obtient donc la condition $\circ \!\!\!\!\!\! \iint_{S_G} \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S_G} = 0$,
donnant avec le fait que ceci doive être vrai pour toutes surfaces et
Ostrogradski que $\text{div} \overrightarrow{\rm j} = 0$. Il reste donc à
interpréter cette condition.

La condition $\text{div} \overrightarrow{\rm j} = 0$ est liée à la loi de
conservation de la charge. En effet, la variation de charge dans notre volume
correspond au nombre de charges qui entrent et sortent par la surface fermée
(puisqu'aucune charge ne se créée ou disparaît). On a ainsi
$\frac{d Q(V_G)}{dt} = - \frac{d \delta \overline{Q_\text{sortant}(S_G)}}{dt}$.

Le théorème de Gauss et Ostrogradski permettent enfin de conclure
que la conservation de la charge nous donne $\circ \!\!\!\!\!\! \iiint_{V_G} (\frac{d \rho}{dt} + \text{div} \overrightarrow{\rm j}) d \tau = 0$
sur toute surface fermée, donnant $\frac{d \rho}{dt} + \text{div} \overrightarrow{\rm j} = 0$, qu'on appelle équation de continuité ou équation
locale de la conservation de charge.

Ainsi, pour que $\text{div} \overrightarrow{\rm j}$ soit nul, il est nécessaire
que $\frac{d \rho}{dt}$ soit nul. En magnétostatique, "rien ne bouge", et on
peut donc en déduire que notre $I_\text{enlacé}$ est indépendant du choix de la
surface sur le contour, nous donnant une définition cohérente.

##### Conclusion
Le théorème d'Ampère tel qu'on l'a vu est donc valable uniquement en statique
(ou dans l'ARQS qui simule la statique). On en tire une équation locale avec le
théorème de Stokes, l'équation de Maxwell-Ampère en statique, $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm B} = \mu_0 \overrightarrow{\rm j}$.

### Relation de passage
On obtient une relation de passage entre deux points $M$ et $M'$ avec $\overrightarrow{\rm N_{MM'}}$
le vecteur perpendiculaire à la surface $S$ entre les deux points qui est
$\overrightarrow{\rm B}(M') - \overrightarrow{\rm B}(M) = \mu_0 \overrightarrow{\rm j_S} \wedge \overrightarrow{\rm M_{MM'}}$.

Le champ magnétique normal est toujours continu en traversant un nappe
surfacique de courant, et le champ tangentiel est discontinue en traversant une
nappe surfacique de courant.

## Calcul de champ
### Solénoïde infini
Le solénoïde est caractérisé par son nombre de spires par unité de longueur $n = \frac{d N}{dz}$.
On applique le modèle à un solénoïde réel lorsque son rayon est petit devant sa
longueur.

On repère les plans de symétrie, qui sont toutes les sections du cylindre
enroulé dans le solénoïde. Comme le champ magnétique est perpendiculaire à ces
plans, en utilisant des contours rectangulaires entièrement à l'extérieur et
entièrement à l'intérieur du solénoïde, on trouve que le champ magnétique y est
homogène.

En utilisant finalement un contour à cheval entre l'extérieur et l'intérieur, on
obtient assez facilement $B(r < R \text{(à l'intérieur du solénoïde)}) = \mu_0 n I$.

## Dipôle magnétique
### Dipôle magnétique et moment dipolaire magnétique
Vu de loin, une source de $\overrightarrow{\rm B}$ semble globalement nulle,
donc le champ magnétique est toujours un champ dipolaire. On cherche donc à
étudier l'expression de $\overrightarrow{\rm B}(M)$ créée par $\overrightarrow{\rm j}(P)$
dans le volume $V$, dans le cadre de l'approximation dipolaire $r = OM \gg L_C$.

On peut montrer que $\overrightarrow{\rm B}(M)$ ne dépend que d'une grandeur
appelée moment dipolaire magnétique ed la distribution de courant $\overrightarrow{\rm \mathcal{M}}$.
Pour un spire, $\overrightarrow{\rm \mathcal{M}} = I \overrightarrow{\rm S_C}$.
On peut voir que c'est le cas peu importe la forme de la surface choisie.

Il n'est demandé que de connaître le cas de la spire circulaire de moment $I 2 \pi r^2 \overrightarrow{\rm e_z}$.
Les autres cas se ramènent presque toujours à une somme de spires (ou à une
intégrale d'une infinité de spires).

Le moment magnétique est en $A \cdot m^2$. Une spire macroscopique avec un
courant d'intensité $10^{-2} A$ et d'un mètre carré de surface a un moment
magnétique de l'ordre de $10^{-2}$, et la rotation d'un électron autour du noyau
génère un moment d'ordre $10^{-24}$ (ce qui est non négligeable si tous les
atomes d'un matériau s'alignent).

### Champ magnétique créé par un dipôle magnétique
Les lignes de champ sont identiques à celles de $\overrightarrow{\rm p}$
donc $\overrightarrow{\rm B}$ est de même forme que $\overrightarrow{\rm E}$.
On a $\overrightarrow{\rm B}$ qui en $r$ est de valeur $\frac{\mu_0 2 \mathcal{M} \cos(\theta)}{4 \pi r^3}$
et en $\theta$ de $\frac{\mu_0 \mathcal{M} \sin(\theta)}{4 \pi r^3}$.
