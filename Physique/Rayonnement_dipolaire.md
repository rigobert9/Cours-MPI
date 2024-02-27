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
