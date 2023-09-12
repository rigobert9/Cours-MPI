# Analyse harmonique, filtres et numérisation
(voir polycopiés pour partie 1 et 3)

## Effets des filtres
### Généralités sur les filtres
> Un filtre est un système physique qui agit sur une grandeur physique d'entrée
> $e(t)$ et fournit une grandeur physique de sortie $s(t)$. On appellera filtre
> uniquement les opérateurs linéaires, c'est à dire tels $e(t)$ et $s(t)$ soient
> liées par une équation différentielle linéaire.

Par exemple, on peut caractériser les frottements fluides comme un filtre liant
la force à la position d'un système.

On ne s'intéresse en général qu'à l'action du filter ne régime permanent.
Ainsi, pour $e(t)$ périodique, $s(t)$ est égale à la somme des réponses du
filtre en chaque harmonique. On veut donc connaître la réponse harmonique du
filtre. On étudie $e(t) = E_m \cos(\omega t)$. Pour caractériser l'action du
filtre, on définit $H(j\omega) = \frac{\underline{S}}{\underline{E}}$
avec $\underline{S}$ et $\underline{E}$ les fonctions complexes associées à $s(t)$
et $e(t)$.

### Diagramme de Bode
Les diagrammes de Bode sont les deux courbes $G_{dB} = 20 \log(|H(j \omega)|) = 20 \log G = 20 \log(\frac{|\underline{S}|}{|\underline{E}|})$
et $\varphi = \text{Arg}(H(j \omega))$. On peut faire des DL pour chercher le
comportement asymptotique du filtre (ou bien on peut imaginer le circuit
équivalent).

### Action d'un filtre sur un signal périodique
Pour $e(t) = E_m \cos(\omega t)$, on a $s(t) = |H(j \omega)| E_m \cos(\omega t + \text{Arg}(\underline{H}))$,
en si $e(t)$ est périodique de période $T = \frac{2 \pi}{\omega}$,
on a donc $e(t) = e_0 + \sum c_n \cos(n \omega t + \varphi_n)$
$\Rightarrow s(t) = |H(0)| e_0 + \sum c_n |H(jn \omega)| \cos(n \omega t + \varphi_n + \text{Arg}(H(jn \omega)))$.

### Filtre passe-bas
L'effet idéal d'un passe-bas serait de laisser passer tout signal de pulsation
inférieure à sa pulsation de coupure et enlever tout signal de pulsation
supérieure.

Qualitativement, on veut que pour $e(t) = e_0 + \sum e_n(t)$,
si $\omega \gg \omega_c$, $s(t) = H_0 e_0$ (ce qui fait que si $H_0$ = 1
un passe-bas mesure à peut près la valeur moyenne).
En fait, si $\exists k \mid k \omega < \omega_c < (k + 1) \omega \Rightarrow s(t) = H_0 e_0 + \sum\limits_{i = 0}^{k} e_n(t)$.
Plus $k$ est grand, plus $s(t)$ ressemble à $e(t)$, et les discontinuités seront
"arrondies".

#### Filtre passe-bas du premier ordre
Un filtre passe-bas du premier ordre est de la forme
$H(j \omega) = \frac{H_0}{1 + j \frac{\omega}{\omega_0}}$,
soit la modélisation d'une équation différentielle
$\frac{1}{\omega} \frac{d s}{dt} + s = H_0 e$.

On obtient les deux asymptotes, celle de $20 \log(H_0)$ pour $\omega \to 0$
et de $20 \log(H_0) - 20 \log(\frac{\omega}{\omega_0})$ pour
$\omega \to \infty$ (une baisse de 20 décibels par décade). On obtient ainsi le
diagramme de Bode en gain.

La phase $\varphi = - \arctan(\frac{\omega}{\omega_c})$,
qui tend vers $0$ en $0$ et $\frac{-\pi}{2}$ en $+\infty$,
et $\frac{-\pi}{4}$ en $\omega = \omega_c$.
