# Électrostatique
## Généralité sur la charge électrique
### Charge électrique dans la matière
Microscopiquement : électrons ou protons. Les électrons sont « faiblement »
arrachables des atomes ce sont eux qui peuvent se déplacer microscopiquement,
soit dans le vide (éclair, effet photoélectrique), soit d'atome en atome
(conduction électrique des métaux). On observe aussi le cas particulier des
solutions dans lesquelles existent des ions mobiles portant des charges.

On compte différents milieux électriques : les isolants (milieux dans lesquels
il n'y a pas de déplacement macroscopique de charges), les conducteurs (métaux,
solutions ioniques) (possibilité de déplacement macroscopique des charges), et
les semi-conducteurs (des isolants qui peuvent être rendus "légèrement"
conducteurs par chauffage, éclairement ou dopage).

### Modélisation de la charge
Parmi ces modélisations, seule celle de la distribution volumique est toujours
valide, puisqu'elle offre une étude macroscopique des lois.

#### Modèle de la charge ponctuelle $q$
Soit $L$ la longueur caractéristique du problème, et $d$ la dimension
caractéristique de la charge. Si $L \gg d$, on peut utiliser le modèle.

#### Distribution volumique de la charge
On définit la densité volumique de charge $\rho(P) = \frac{d q (\delta \tau)}{d \tau}$
où $d q(\delta \tau)$ est la charge contenue dans un volume élémentaire $d \tau$
autour de $P$. La charge $Q$ contenue dans un volume $V$ est alors $Q = \iiint_V \rho(P) d \tau$.

#### Modèle de la charge surfacique
On suppose que la charge se confine à une surface (comme par exemple sur un
plan, ou en passant par des couches pour un volume comme quand on considère que
la charge est inhomogène dans un métal), et alors on mesure la densité
surfacique de charge $\sigma(P) = \frac{d q(dS)}{dS}$, donnant $Q_\pi = \iint_\pi \sigma(P) dS$.

#### Modèle de la charge linéïque
Exactement la même chose que les deux autres modèles, en linéïque, ce qui donne
pour la densité linéïque $\lambda(P) = \frac{d q(d \ell)}{d \ell}$ et donc
$Q_\ell = \int\limits_{0}^{\ell} \lambda(P) d \ell$.

## Champ électrique et potentiel électrique
Quand on étudie le champ électrique du régime stationnaire, on parle
d'électrostatique. On se place alors dans l'approximation d'un régime
stationnaire, où les variable intensives ne dépendent pas du temps $t$, donc que
les dérivées partielles des champs par rapport au temps sont nulles.
Ainsi, par exemple, $\rho(\ell,t)$ se réécrit $\rho(\ell)$.

On doit alors découple les champs $\overrightarrow{\rm E}$ et $\overrightarrow{\rm B}$,
car dans le cas où le régime est variable ces champs électromagnétiques sont
couplés. En régime stationnaire, on étudie l'électrostatique et la
magnétostatique séparément.

### Champ électromagnétique
#### Loi de Coulomb et champ créé par une charge ponctuelle
La force de coulomb d'une charge ponctuelle $q$ sur une charge ponctuelle $q'$
est $\overrightarrow{\rm F_{q \to q'}} = \frac{q q'}{4 \pi \varepsilon_0 PP'^3} \overrightarrow{\rm P P'}$.
Si $q$ est en un point $O$, le centre d'un repère sphérique dans cette formule,
elle engendre un champ de force $\overrightarrow{\rm F_q}(q') = \frac{q q'}{4 \pi \varepsilon_0 r^3} \overrightarrow{\rm OP'}$.

#### Champ électrique créé par une distribution de charge
Nous n'avons besoin que de ces formules de base pour s'occuper de toute la
partie électrostatique : en effet, le théorème de superposition nous donne que
le champ engendré par plusieurs charges est la somme de leurs champs.

Dans le cas des distributions volumiques, surfaciques ou linéïques, on peut
passer à des intégrales de ces champs, menant rapidement à des monstres type
intégrale triple vectorielle.

### Potentiel électrostatique
#### Expression du potentiel électrostatique
##### Expression pour une charge ponctuelle
Soit $P = O$ et $q$ situé en $O$. En travaillant l'expression de $\overrightarrow{\rm E}(M)$
et en réexprimant la variable $r$ selon chaque coordonnée cartésienne, on peut
bien vérifier $\overrightarrow{\rm E} = - \overrightarrow{\rm \text{grad}}(\frac{q}{4 \pi \varepsilon_0 r})$.
On définit le potentiel $V$ comme étant le potentiel qui engendre $\overrightarrow{\rm E}$ dans
la formule, soit $V_q(M) = \frac{q}{4 \pi \varepsilon_0 r} + u_0$. Par
convention, on prendra $V$ tendant vers $0$ en $r \to \infty$.

##### Expression pour une distribution de charge
Par superposition (et car on utilise les deux mêmes constantes dans tous les
cas), on peut superposer les potentiels. Attention, il faut parfois choisir un
potentiel à l'infini non nul dans le cas de distributions dans tout l'espace.

#### Circulation du champ
On a, par propriété du gradian, $\overrightarrow{\rm \text{grad}} \varphi \cdot d \overrightarrow{\rm \ell} = d \mathcal{C}$
et $\int\limits_{(AB)} \overrightarrow{\rm \text{grad}} \varphi d \overrightarrow{\rm \ell} = \varphi(B) - \varphi(A) = \Delta \varphi$.

En électrostatique, $\overrightarrow{\rm E} = - \overrightarrow{\rm \text{grad}} V$
donc $\overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} = - d V$
et $\int\limits_{(AB)} \overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} = U_{AB}$.

Ainsi, si $\overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} > 0$, la
tension est négative : $\overrightarrow{\rm E}$ est orienté vers les potentiels
décroissants. On le retrouve avec $q > 0$ : une charge positive e est attiré par
les potentiels négatifs.

#### Énergie potentielle d'une charge $q'$ dans un potentiel extérieur
Soit un potentiel créé par des charges $q_i$, qui donne une champ $\overrightarrow{\rm E}(M)$
soumettant la charge à la force $q' \overrightarrow{\rm E}(M)$. Cette force
dérive d'une énergie potentielle $E_{\pi_\text{élec}}(M) = q' V(M) + \text{constante}$.
On choisira le plus souvent une constante telle que $E_{\rho_\text{élec}}$ soit
nulle infiniment loin des charges.

Le travail de cette force sur un chemin de $A$ à $B$ est alors de
$- \Delta E_{\rho_\text{élec}} = - q' U_{AB}$.

### Propriétés de continuité de symétrie et d'invariance
#### Continuité
Les champs ne sont pas continus au niveau des charges (ils divergent à l'endroit
où est la charge).

$d \overrightarrow{\rm E} \propto \frac{\rho d \tau}{r^2} ~ \frac{\rho r^2 dr}{r^2} ~ \rho dr$
mais en présence d'une distribution surfacique
$d \overrightarrow{\rm E} \propto \frac{\sigma d S}{r^2} ~ \frac{\sigma r dr}{r^2} ~ \frac{\sigma dr}{r}$.

> Ainsi, le champ électrique est continu sur les charges volumiques mais
> discontinu (ou indéfini) sur les charges surfaciques, linéïques ou ponctuelles.
> De meme, le potentiel électrique $V$ est continu sur une distribution volumique
> ou surfacique mais discontinu ou non défini sur une distributivité linéïque ou
> une charge ponctuelle.

#### Propriétés de symétrie
> Principe de Curie : La symétrie des causes se retrouve dans les conséquences;
> ici, le champ électrique qui est un champ symétrique possède les même symétries
> que celles des charges qui le créent.

Au début de tout exercice, on cherchera donc à identifier les plans de symétrie
et d'antisymétrie de la distribution de charge.

#### Conséquence : propriété fondamentale à connaître
> En un point $M$ appartenant à un plan de symétrie $\pi_S$, le champ électrique
> $\overrightarrow{\rm E}(M)$ est contenu dans le plan $\pi_S$.

Si $M \in \pi_{As}$ un plan d'asymétrie, $\overrightarrow{\rm E}(M)$ est
perpendiculaire à $\pi_{As}$.

### Lignes de champ et surfaces équipotentielles
#### Définition
> Une surface équipotentielle est l'ensemble des points contigus ayant le même
> potentiel électrique.

> Une ligne de champ est la courbe tangente en chacun de ces points au champ
> électrique $\overrightarrow{\rm E}$ orienté dans le sens de $\overrightarrow{\rm E}$,
> (en lesquelles $\overrightarrow{\rm E} \wedge d \overrightarrow{\rm \ell}$).

> Un tube de champ est l'ensemble des lignes de champ qui s'appuie sur un contour
> fermé. On ne peut sortir du tube sans traverser ces parois de lignes de champ.

#### Orthogonalité aux équipotentielles
Les lignes de champ sont orthogonales aux surfaces équipotentielles. En effet,
pour $M$ et $M'$ sur une surface équipotentielle, les $d \overrightarrow{\rm \ell}$
entre les deux sont tels que $\int \overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} = \int - d V$
$\Delta V = 0$.

#### Propriétés des lignes de champ
Les lignes de champ possèdent les propriétés de symétrie de $\overrightarrow{\rm E}$.
Elles appartiennent aux plans de symétrie et sont orthogonales aux plans
d'asymétrie. Les axes de symétrie sont donc forcément des lignes de champ.

Les lignes de champ ne peuvent pas se couper, sinon $\overrightarrow{\rm E}$
aurait deux directions différentes (ou bien $\overrightarrow{\rm E}$ serait
nul ou indéfini comme en une charge ponctuelle).

Le long d'une ligne de champ, le potentiel décroit (car $\overrightarrow{\rm E}$ pointe dans les $V$
décroissants). Une ligne de champ ne peut donc pas être fermée, car alors
l'intégrale dessus serait un potentiel nul, qui contredirait la positivité de
$\overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell}$.

Au niveau d'une charge positive, les lignes de champ s'éloignent de la charge;
au niveau d'une négative, les lignes de champ convergent vers la charge.

EN L'ABSENCE DE CHARGES, si les lignes de champ se resserrent, $\| \overrightarrow{\rm E} \|$
croit.

## Lois de l'électrostatique
### Lois sur le flux du champ électrique
#### Flux d'un champ à travers une surface
Dans le chapitre d'induction de l'année de sup, on étudiait avec la loi de
Faraday le flux du champ magnétique à travers des surfaces délimitées par des
contours fermés.

> Le flux d'un champ $\overrightarrow{\rm A}$ à travers une surface $\overrightarrow{\rm S}$
> s'écrit $\varphi_{\overrightarrow{\rm A}} = \iint_S \overrightarrow{\rm A} \cdot d \overrightarrow{\rm S}$.

> On appelle surface fermée $S_F$ une surface frontière d'un volume. Une surface
> fermée définit un intérieur et un extérieur. On ne peut passer de l'un à l'autre
> sans traverser $S_F$.

On pourra orienter les surfaces ouvertes arbitrairement, mais il faut donc préciser
l'orientation du vecteur normal que l'on utilise. Pour les surfaces fermées, la
convention sauf avis contraire est d'orienter le vecteur normal vers l'extérieur
du volume encadré par la surface.

#### Cas du flux à travers une surface fermée
On peut facilement calculer le flux d'une charge ponctuelle $q$ à travers une
sphère l'entourant, ce qui donne de façon élégante $\frac{q}{\varepsilon_0}$. Ce
résultat est vrai de façon générale, ce qu'on peut voir venir en comprenant que
le flux à travers une surface est le flux à travers la surface orthogonale au
champ électrique.

> Théorème de Gauss : Pour $S_F$ une surface fermée et une distribution de charge
> à l'intérieur de charge totale $Q_\text{int}$, on a
> $\circ\!\!\!\!\!\!\iint_{S_F} \overrightarrow{\rm E_\text{distribution}} \cdot d \overrightarrow{\rm S} = \frac{Q_\text{int}}{\varepsilon_0}$.

#### Équation locale de l'électrostatique, équation de Maxwell-Gauss
Par le théorème d'Ostrogradski et le théorème de Gauss, si $S_F$ entoure un
volume $V_F$, on a $\iiint_{V_F} \text{div} \overrightarrow{\rm E} d \tau = \frac{\iiint_{V_F} \pi d \tau}{\varepsilon_0}$,
donnant que $\iiint_{V_G} (\text{div} \overrightarrow{\rm E} - \frac{\rho}{\varepsilon_0}) d \tau = 0$,
donnant enfin l'équation de Maxwell-Gauss :

> $\text{div} \overrightarrow{\rm E} = \frac{\rho}{\varepsilon_0}$

### Loi sur la circulation de $\overrightarrow{\rm E}$
#### $\overrightarrow{\rm E}$ est à circulation conservative
> Pour tout contour fermé $\mathcal{C}$, $\circ\!\!\!\!\int_{\mathcal{C}} \overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} = 0$.

#### Loi locale
Le théorème de Stokes nous permet d'obtenir de la même façon la loi
locale $\overrightarrow{\rm \text{rot}} \overrightarrow{\rm E} = \overrightarrow{\rm 0}$
(en effet, on a déjà vu que c'était le cas car $\overrightarrow{\rm E}$ est le
gradian d'un potentiel, et le rotationnel d'un gradian est nul).

### Équation de Poisson
> On a grâce aux précédents résultats que $- \text{div} \overrightarrow{\rm \text{grad}}(V) = \frac{\rho}{\varepsilon_0}$,
> soit $\Delta V = \frac{- \rho}{\varepsilon_0}$ (avec $\Delta$ le Laplacien).

On appelle équation de Laplace le résultat que $\Delta V = 0$ dans les zones
vides de charge.

### Relation de passage
Soit une surface chargée d'une densité $\sigma$ de charge, et $M, M'$ deux
points de part et d'autre de la surface chargée avec $M_0$ un point sur le
chemin entre les deux sur la surface. On a (hors programme)
$\overrightarrow{\rm E}(M') - \overrightarrow{\rm E}(M) = \frac{\sigma}{\varepsilon_0} \overrightarrow{\rm M_{M \to M'}}$.
La relation suivante est en revanche au programme.

> Au niveau d'une surface chargée, le champ électrique tangentiel à la surface est
> continu et le champ électrique normal à la surface est discontinu.

## Calcul de champ électrique
### Exemples d'application du théorème de Gauss
...

### Autres examples
#### Cas du plan infini
Soit un plan infini $(Oxy)$ portant une densité de charge $\sigma$. La
distribution est invariante par translation par $\overrightarrow{\rm e_x}$
et $\overrightarrow{\rm e_y}$, et est symétrique suivant les plans $(Oxz)$
et $(Oyz)$, montrant que $\overrightarrow{\rm E} = E_z \overrightarrow{\rm e_z}$.

On applique le théorème de Gauss à un cylindre $S_G$ de section $S$ et de
génératrice $(Mz)$ et de hauteur $2 z$ symétrique à $(Oxy)$. Il ne faut pas
oublier de considérer le côté du cylindre mais aussi les deux faces.

Cette application du théorème de Gauss nous donne deux termes égaux sur les
faces et un terme nul par le côté du cylindre (car le champ électrique est perpendiculaire
au côté), donnant un résultat de $\frac{\sigma S}{\varepsilon_0}$ qui est égal à
$E(z) S - E(-z) S$. On DOIT alors préciser la symétrie utilisée qui mène à
$E(-z) = - E(z)$, et avec laquelle on conclut $2 E(z) S = \frac{\sigma S}{\varepsilon_0}$
$\Rightarrow E(z) = \frac{\sigma}{2 \varepsilon_0}$ pour $z > 0$. On en dérive
l'expression du champ dans tout l'espace $\overrightarrow{\rm E}(z) = \pm \frac{\sigma}{2 \varepsilon_0}$,
positif pour $z$ positif et négatif pour $z$ négatif.

On peut aussi arriver à la même conclusion via la relation de passage et Maxwell-Gauss
(avec une densité volumique de charge nulle puisque la distribution est
surfacique).

#### Le modèle du condensateur plan
##### Définition et constitution
Un condensateur plan est constitué de deux plans infinis parallèles espacés
d'une distance $e$ et de charge surfacique opposés, $\sigma$ et $- \sigma$.

##### Calcul de $\overrightarrow{\rm E}$ dans tout l'espace
Une première méthode est utile si on a déjà travaillé sur le modèle du plan
infini. On utilise alors simplement le théorème de superposition. On peut aussi
le faire avec la relation de passage.

##### Définition et calcul de la capacité d'un condensateur
La capacité d'un condensateur est définie comme $C = \frac{Q_{1}}{V_{1} - V_2} = \frac{Q_2}{V_2 - V_1}$.
On le calcule avec $\overrightarrow{\rm E}$ entre les plaques, puis on calcule
la circulation de $\overrightarrow{\rm E}$ d'une armature à l'autre, ce qui
donne une relation entre $V_1 - V_2$ et $Q_1$.

En effet, on a alors $\int\limits_{1}^{2} \overrightarrow{\rm E} \cdot d \overrightarrow{\rm \ell} = V_1 - V_2$
$= \int\limits_{1}^{2} - \frac{\sigma}{\varepsilon_0} \overrightarrow{\rm e_z} d \ell \overrightarrow{\rm e_z}$
$= \frac{- \sigma}{\varepsilon_0} e$. Or, $Q_1 = - \sigma S_1 \Rightarrow \sigma = \frac{- Q_1}{S_1}$,
donnant finalement $V_1 - V_2 = \frac{Q_1 e}{S_1 \varepsilon_0}$, donnant
$C = \frac{Q_1}{V_1 - V_2} = \frac{\varepsilon_0 S}{e}$.

##### Validité du modèle
Les plans infinis n'existent toujours pas, mais is $e \ll \sqrt{5}$, on dit
qu'on néglige les effets de bord, et tout se passe comme si les plans étaient
infinis.

##### Aspect énergétique
On rappelle que $P = u i$ est la puissance reçue par un dipôle électrique.
Pour le condensateur, $P = (V_1 - V_2) \frac{d Q_1}{dt}$. Or $C = \frac{Q_1}{V_1 - V_2} \Rightarrow V_1 - V_2 = \frac{Q_1}{C}$,
donc $P = \frac{Q_1}{C} \frac{d Q_1}{dt} = \frac{d}{dt} (\frac{1}{2} \frac{Q_1^2}{C})$,
la dérivée d'une énergie électrostatique stockée par le condensateur
$E_\text{élec} = \frac{Q^2}{2 C} = \frac{1}{2} C (V_1 - V_2)^2$.

On verra qu'on pourra définir une énergie volumique liée à la présence de charge
(le simple fait qu'elle soit là statique) $e_\text{élec} = \frac{d E_\text{élec}}{d \tau} = \frac{1}{2} \varepsilon_0 E^2$.

#### Quelques notions sur les conducteurs à l'équilibre électrique
Un conducteur est un matériau dans lequel les charges peuvent se déplacer
macroscopiquement. À l'équilibre électrique les charges sont immobiles, donc
$som \overrightarrow{\rm F}_{\to \text{ charge}} = \overrightarrow{\rm 0}$. Dans
le cas le plus simple, le champ électrique est simplement nul.

Dans un conducteur, on suppose les électrons de conduction comme quasi libres
(donc de PFD nul). En fait, en moyenne, la force moyenne du réseau sur les
charge est de $- h \overrightarrow{\rm v_q}$, le ralentissant lorsqu'il essaie
de se déplacer du réseau. Dans tous les cas, le PFD nul permet de déterminer que
le champ électrique est nul dans le conducteur à l'équilibre, ce qui est
équivalent au fait que le potentiel soit constant dans un conducteur.

## Champ gravitationnel
### Analogie gravitation/électrostatique
La force de Coulomb peut être mise directement en comparaison avec la force de
gravitation, en remplaçant les deux charges par les deux masses et $\frac{1}{2 \pi \varepsilon_0}$
par $-G$. On peut donc aussi bien considérer le champ gravitationnel à la place
du champ électrique, donnant un équivalent au théorème de Gauss pour la
gravitation : $\circ\!\!\!\!\!\!\iint_{S_G} \overrightarrow{\rm \mathcal{G}} \cdot d \overrightarrow{\rm S} = - 4 \pi G M_\text{int}$.
On peut en découler une équation locale de la même façon.

## Dipôle électromagnétique
### Définition et expression du dipôle électrostatique
#### Définition
> On appelle distribution électrostatique dipolaire une distribution de charge
> dans un volume $V$ telle que $Q_\text{int} = 0$. On appelle sa longueur
> caractéristique $L$ son diamètre, et on s'intéresse au champ $\overrightarrow{\rm E}$ créé en $M$
> pour la distribution "de loin", c'est à dire que $OM = r \gg L$.

Ce qui est alors intéressant, c'est la polarisation des molécules, qui ont un
barycentre positif à un autre endroit que le barycentre négatif.

On définit $G_+ = P$ le barycentre des charges positives, et $G_- = N$ celui des charges
négatives. On rappelle précisément la définition comme $\overrightarrow{\rm OG_+}$
$= \frac{\sum\limits_{i_+} q_{i+} \overrightarrow{\rm OP_{i+}}}{\sum\limits_{i+} q_{i+}}$,
et on note $q = \sum\limits_{i+} q_{i+}$ et $-q = \sum\limits_{i-} q_{i-}$. On
admet que le champ créé par la distribution est le même que celui créé par
la distribution $\{N;P\}$.

#### Ordre de grandeur et unité
On cherche donc à montrer que $\overrightarrow{\rm E}$ créé par la distribution ne
dépend que du moment dipolaire de la distribution qui vaut $\overrightarrow{\rm p} = q \overrightarrow{\rm NP}$.
Ce moment dipolaire est d'unité SI $C \cdot m$, mais souvent d'ordre de grandeur
$10^{-29}$. Les chimistes lui préfèrent donc le Debye, avec $1 D = \frac{1}{3} 10^{-29} C \cdot m$.

### Expression du potentiel et du champ dipolaire
#### Calcul de $V$ dans $\ell'$ et approximation dipolaire
On reprend l'approximation dipolaire faite plus haut, c'est-à-dire que
$OM = r \gg d$. Alors on a $V(M) = V_q(M) + V_{-q}(M) = \frac{q}{4 \pi \varepsilon_0 PM} + \frac{-q}{4 \pi \varepsilon_0 NM}$.
$PM = \sqrt{(\overrightarrow{\rm PO} + \overrightarrow{\rm OM})^2} = \sqrt{(\frac{d}{2})^2 + r^2 + 2 \overrightarrow{\rm PO} \cdot \overrightarrow{\rm OM}}$\
$= \sqrt{\frac{d^2}{4} + r^2 - d r \cos(\theta)}$\
$= r \sqrt{1 - \frac{d}{r} \cos(\theta) + \frac{d^2}{4 r^2}}$\
Ainsi, $\frac{1}{PM} \underset{r \gg d}{\sim} \frac{1}{r} (1 + \frac{d}{2r} \cos(\theta) + o(\frac{d}{r}))$.
De même, $\frac{1}{NM} \underset{r \gg d}{\sim} \frac{1}{r} (1 - \frac{d}{2r} \cos \theta)$.

On a donc $V(M) \approx \frac{q d \cos(\theta)}{4 \pi \varepsilon_0 r^2}$. Or $\overrightarrow{\rm p} = qd \overrightarrow{\rm e_z}$,
et $\cos(\theta) = \overrightarrow{\rm e_r} \cdot \overrightarrow{\rm e_z}$,
donnant finalement $V_{\text{créé par } \overrightarrow{\rm p}}(M) = \frac{\overrightarrow{\rm p} \cdot \overrightarrow{\rm e_r}}{4 \pi \varepsilon_0 r^2}$.

On peut remarquer que ce potentiel dipolaire décroît plus vite (en $\frac{1}{r^2}$) que le potentiel créé par une charge seule
($\frac{1}{r}$).

#### $\overrightarrow{\rm E}$ créé par $\overrightarrow{\rm p}$
Comme $\overrightarrow{\rm E} = - \overrightarrow{\rm \text{grad}} V$, on
obtient l'expression
$\overrightarrow{\rm E} = \left\{\begin{matrix} E_r = \frac{2 p \cos(\theta)}{4 \pi \epsilon_0 r^3} \\ E_\theta = \frac{p \sin(\theta)}{4 \pi \varepsilon_0 r^3} \\ E_\varphi = 0 \end{matrix}\right.$

#### Lignes de champ du dipôle
Pour que $\overrightarrow{\rm E} \wedge d \overrightarrow{\rm \ell}$ soit nul,
il est nécessaire (en coordonnées sphériques) que $E_r r d \theta - E_\theta d r = 0$,
soit $\frac{2 p \cos(\theta)}{4 \pi \epsilon_0 r^3} r d \theta = E_\theta = \frac{p \sin(\theta)}{4 \pi \varepsilon_0 r^3} dr$\
$\Rightarrow \frac{dr}{r} = \frac{2 \cos(\theta)}{\sin(\theta)} d \theta$\
$\Rightarrow ln(r) = 2 \ln(\sin(\theta)) + C$, soit $r = A \sin^2(\theta)$.

On retrouve la figure en ailes de papillon qu'on retrouve souvent en
magnétisme.

#### Action d'un champ électrique extérieur sur un dipôle de moment dipolaire $\overrightarrow{\rm p}$
Un dipôle de moment dipolaire $\overrightarrow{\rm p}$ dans un champ extérieur
$\overrightarrow{\rm E}$ possède une énergie potentielle $E_p = - \overrightarrow{\rm p} \cdot \overrightarrow{\rm E}$,
et subit un couple $\overrightarrow{\rm \Gamma} = \overrightarrow{\rm p} \wedge \overrightarrow{\rm E}$.
Ce couple ne dépend pas du point $O$ où on le calcule (on peut retrouver cette
expression à partir du moment sur $N$ et $P$).

La résultante des forces donne $\overrightarrow{\rm F} = q \overrightarrow{\rm E} + - q \overrightarrow{\rm E} = \overrightarrow{\rm 0}$
(dans un champ uniforme), donc le dipôle est soumis uniquement à un moment. Si
$\overrightarrow{\rm E}$ n'est pas uniforme, $\overrightarrow{\rm F} = (\overrightarrow{\rm p} \cdot \overrightarrow{\rm \text{grad}}) \overrightarrow{\rm E}$.

Si le champ électrique n'est pas uniforme, et dans tous les cas plus compliqués
en général, on peut voir que la position d'équilibre à laquelle arrive le dipole
est un minimum local d'énergie potentielle (étude lagrangienne).
