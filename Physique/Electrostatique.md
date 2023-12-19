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
