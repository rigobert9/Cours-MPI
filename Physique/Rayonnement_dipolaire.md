# Rayonnement dipolaire
## Champ électromagnétique d'un dipôle oscillant
### Position du problème
Soit $V$ un volume contenant toutes les sources des champs électriques et
magnétiques étudiés. On modélise les charges par une densité de charge
volumique, et on pose $\overrightarrow{\rm p} = \iiint \rho(P) \overrightarrow{\rm OP} d \tau$,
en fonction duquel on exprimera les champs.

On considère deux modèles classiques, celui de deux charges mobiles l'une par
rapport à l'autre et celui de deux charges reliées par un courant.

> __Principe du potentiel retardé :__ On admet que le champ électromagnétique
> créé par les charges et les courants volumiques es calculent comme en statique à
> condition de tenir compte du temps de propagation de $P$ à $M$. Ainsi,
> $\overrightarrow{\rm E}(M,t)$ et $\overrightarrow{\rm B}(M,t)$ sont calculés en
> statique à partir des valeurs de $\rho(P,t - \frac{PM}{c})$ et de $\overrightarrow{\rm j}(P, t - \frac{PM}{c})$.

### Approximation dipolaire
Dans le cas des potentiels retardés, il faut calculer
$V(M,t) = \iiint_{P \in V} \frac{\rho(P - \frac{PM}{c})}{4 \pi \varepsilon PM} d \tau$.

> __Approximation dipolaire :__ On suppose, pour $a$ le diamètre de $V$, $OM \gg a$,
> et donc que $\frac{1}{PM} \sim \frac{1}{OM}$.

On cherche alors à avoir $t - \frac{PM}{c} \sim t - \frac{OM}{c}$, qui s'obtient
en montrant qu'il est petit devant un temps caractéristique du problème $T$.
Comme la grandeur à négliger est majorée par $\frac{a}{c}$, on prouve simplement
que comme les charges ne sont pas relativistes, $\frac{a}{T} \ll c$
out encore que $a \ll c T = \lambda$, donc que les charges sont dans l'ARQS.

On fait donc en résumé les approximations $a \ll r \Rightarrow \frac{1}{PM} \sim \frac{1}{OM}$
et $a \ll c T \Rightarrow \frac{PM}{c} \sim \frac{r}{c}$. Dans ce cadre, on
obtient $V(M,t) = \iiint_{P \in V} \frac{\rho(P - \frac{r}{c})}{4 \pi \varepsilon OM} d \tau$.

### Champ électromagnétique créé
On a, comme déjà vu, les champs suivants, avec $t' = t - \frac{r}{c}$:
- $\overrightarrow{\rm E}(M,t) = \frac{2 \sin \theta}{4 \pi \varepsilon_0} (\frac{p(t')}{r^3} + \frac{\dot{p}(t')}{r^2 c}) \overrightarrow{\rm e_r} + \frac{\sin \theta}{4 \pi \varepsilon_0} (\frac{p(t')}{r^3} + \frac{\dot{p}(t')}{r^2 c} + \frac{\ddot{p}(t')}{r c^2}) \overrightarrow{\rm e_\theta}$
- $\overrightarrow{\rm B}(M,t) = \frac{\mu_0 \sin \theta}{4 \pi} (\frac{\dot{p}(t')}{r^2} + \frac{\ddot{p}(t')}{r c}) \overrightarrow{\rm e_\varphi}$

## Champ de rayonnement et puissance rayonnée
### Différentes zones d'étude : le champ de rayonnement
Puisque $\overrightarrow{\rm B}$ et $\overrightarrow{\rm E}$ dépendent
des termes $\frac{p}{r^3}$, $\frac{\dot{p}}{r^2 c}$, $\frac{\ddot{p}}{r c^2}$.
Soit $\overrightarrow{\rm p}(t) = \overrightarrow{\rm p_0} \cos(\omega t)$
(dipôle sinusoïdal), donnant les équivalents
$p \sim p_0$, $\dot{p} \sim p_0 \omega$, $\ddot{p} \sim p_0 \omega^2$.

Les équivalents aux termes qui nous intéressent donnent alors, dans le cas
$r \ll \lambda$, que le terme $\frac{p}{r^3}$ domine les autres, donnant le cas
de $\overrightarrow{\rm E}$ et $\overrightarrow{\rm B}$ égaux à leurs valeur en
statique (correspond à l'ARQS). Dans le cas où les grandeurs sont comparables, on ne peut pas
simplifier. Dans le dernier cas particulier au programme où $r \gg \lambda$,
le terme prépondérant est $\frac{\ddot{p}}{r c^2}$, donnant
$\overrightarrow{\rm E} = \frac{\sin \theta}{4 \pi \varepsilon_0} \frac{\ddot{p}(t - \frac{r}{c})}{r c} \overrightarrow{\rm e_\theta}$
et $\overrightarrow{\rm B} = \frac{\sin \theta}{4 \pi \varepsilon_0} \frac{\ddot{p}(t - \frac{r}{c})}{r c^2} \overrightarrow{\rm e_\theta}$
(soit $B = \frac{E}{c}$).
On appelle la zone dans laquelle $r \gg \lambda$ la zone de rayonnement.

### Structure du champ de rayonnement
Le champ électromagnétique dans la zone de rayonnement correspond à une onde
ayant localement la structure d'une onde plane, dont la propagation est radiale
(selon $\overrightarrow{\rm e_r}$).Les champs sont
proportionnels à $\sin(\theta)$, donc l'amplitude de l'onde émise dépend 
de l'angle : les champs sont maximaux dans le plan équatorial, et nuls dans la
direction des pôles.

### Puissance rayonnée
#### Vecteur de Poynting
On a finalement $\overrightarrow{\rm \Pi} = \frac{(\ddot{p}(t - \frac{r}{c}))^2 \sin^2(\theta)}{16 \pi^2 \varepsilon_0 c r^2} \overrightarrow{\rm e_r}$.
On peut tracer l'amplitude de ce vecteur selon de nombreux paramètres. Un
diagramme de rayonnement correspond au graphe selon $\theta$.

#### Puissance totale rayonnée
La puissance totale de rayon $r$ étant l'intégrale sur la surface d'une sphère de rayon $r$
du flux du vecteur de Poynting, et est donc de valeur $P_\text{tot}(r) = \frac{\ddot{p}(t - \frac{r}{c})^2}{6 \pi \varepsilon_0 c}$.
Ainsi, la puissance totale est proportionnelle à $\frac{1}{r}$ et à
l'accélération au carré des charges.

C'est cette dernière proportionnalité qui justifie le rayonnement synchrotron
étudié au CERN, les appareils de mesure à rayons X qui créent ces rayons à
partir d'électrons fortement décélérés par une plaque en plomb, et le
rayonnement du corps noir dans lequel l'agitation thermique entraîne une
oscillation des électrons et donc une onde électromagnétique.

#### Cas du dipôle sinusoïdal
Soit $\overrightarrow{\rm p} = p_0 \cos(\omega (t - \frac{r}{c}))$, $\ddot{p} = p_0 \omega^2 cos(\omega (t - \frac{r}{c}))$,
donnant $P_\text{tot}(r) = \frac{p_0^2 \omega^4 \cos^2(\omega (t - \frac{r}{c}))}{6 \pi \varepsilon_0 c}$.
La puissance rayonnée étant la valeur moyenne de cette puissance, on a
$P_\text{rayonnée} = \frac{p_0^2 \omega^2}{12 \pi \varepsilon_0 c}$, qui est
proportionnelle à $\frac{1}{\lambda^4}$.

#### Diffusion de Rayleigh
Soit un atome excité par un champ sinusoïdal à la pulsation $\omega$, l'action
de ce champ sur un électron est proportionnelle à $\frac{1}{\lambda^4}$, et
l'atome absorbe donc cette énergie en émettant une onde électromagnétique :
c'est la diffusion de Rayleigh.

Ce phénomène explique la couleur du ciel pendant la journée et au crépuscule :
pendant la journée, le soleil excite l'atmosphère tangentiellement à la Terre et
nous recevons donc une lumière de couleur bleue (à cause de la puissance du
soleil). Au crépuscule, on a la couleur rouge.
