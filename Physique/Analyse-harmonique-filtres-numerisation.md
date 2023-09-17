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
$\frac{1}{\omega_0} \frac{d s}{dt} + s = H_0 e$.

On obtient les deux asymptotes, celle de $20 \log(H_0)$ pour $\omega \to 0$
et de $20 \log(H_0) - 20 \log(\frac{\omega}{\omega_0})$ pour
$\omega \to \infty$ (une baisse de 20 décibels par décade). On obtient ainsi le
diagramme de Bode en gain.

La phase $\varphi = - \arctan(\frac{\omega}{\omega_c})$,
qui tend vers $0$ en $0$ et $\frac{-\pi}{2}$ en $+\infty$,
et $\frac{-\pi}{4}$ en $\omega = \omega_c$.

#### Comportement intégrateur d'un filtre passe-bas du premier ordre
> Un intégrateur est un filtre tel que $s(t) = \omega_0 H_0 \int e(t) \Leftrightarrow H(j \omega) = \frac{H_0}{j \frac{\omega}{\omega_0}}$.

C'est le cas du circuit formé par une entrée suivie d'une résistance suivie d'un
ampli-op dont l'une des bornes est branchée à sa sortie avec un condensateur. La
sortie correspond à une branche avant le condensateur.
On a alors $\underline{e} = U_r - \varepsilon + 0$ (avec $\varepsilon$ la
différence de tension entre les bornes d'entrée de l'ALI (l'autre nom,
amplificateur linéaire intégré)), et $\underline{e} =
Ri$, donc $\underline{s} = \frac{-1}{j \omega} i - \varepsilon - 0$, donnant
$H = \frac{s}{e} = \frac{-1}{j R C \omega} = \frac{-1}{j \frac{\omega}{\omega_0}}$,
avec $\omega_0 = \frac{1}{RC}$.
Attention, lorsque $\omega \to 0$, $|H|$ tend vers $+\infty$, et les tensions
continues risquent de diverger et les fréquence basses risquent d'être
amplifiées.

Pour éviter ces risques qui peuvent soit enlever la linéarité du système, soit
l'endommager, on choisit plutôt un filtre passe-bas avec $\omega_c \ll \omega$.
On a ainsi $H_{PB} = \frac{H_0}{1 + j \frac{\omega}{\omega_c}} \approx \frac{H_0}{j \frac{\omega}{\omega_c}}$.
De plus, pour les composantes constantes, on obtient uniquement $H_0 e_0$,
permettant de ne pas intégrer la valeur moyenne. Les fréquences les plus basses
sont donc simplement multipliées, et les hautes (celles sur l'asymptote $-20 \log(x)$) intégrées.

#### Passe-bas du deuxième ordre
$H(j\omega) = \frac{H_0}{1 + 2 j \sigma \frac{\omega}{\omega_0} - (\frac{\omega}{\omega_0})^2}$,
soit $\frac{1}{\omega_0^2} \frac{d^2 s}{dt^2} + 2 \frac{\sigma}{\omega_0} \frac{d s}{dt} + 0 = H_0 e$.
- $\omega_\text{max}$ (la pulsation de résonance) $< \omega_0$
- Trois cas sont possibles : une grande résonance pour $\sigma < \frac{1}{2}$,
  une plus petite et plus tôt qui colle très vite à l'asymptote en $+\infty$
  pour $\frac{1}{\sqrt{2}} < \sigma < \frac{1}{2}$, et un passage légèrement
  plus bas et plat qu'un premier ordre, sans résonance, pour $\sigma > \frac{1}{\sqrt{2}}$
- $\omega_0$ est la fréquence de coupure à $-3 dB$ **UNIQUEMENT** pour $\sigma =
  \frac{1}{\sqrt{2}}$
- On peut utiliser un passe bas d'ordre 2 comme un passe-bande sur la résonance
  (qui est très étroite)

### Filtre passe-haut
L'effet idéal d'un passe-haut serait de laisser passer tout signal de pulsation
supérieure à sa pulsation de coupure et enlever tout signal de pulsation
inférieure.

Qualitativement, on veut que pour $e(t) = e_0 + \sum e_n(t)$,
si $\omega \ll \omega_c$, $s(t) = H_0 \sum e_n(t)$ (ce qui fait qu'un passe-haut
mesure un signal sans valeur moyenne).

#### Filtre passe-haut du premier ordre
Un filtre passe-haut du premier ordre est de la forme
$H(j \omega) = \frac{H_0 j\frac{\omega}{\omega_0}}{1 + j \frac{\omega}{\omega_0}}$,
soit la modélisation d'une équation différentielle
$\frac{1}{\omega} \frac{d s}{dt} + s = \frac{H_0}{\omega_0} \frac{d e}{dt}$.

#### Comportement dérivateur d'un filtre passe-haut du premier ordre
> Un dérivateur est un filtre tel que $s(t) = \frac{H_0}{\omega_0} \frac{d e}{dt} \Leftrightarrow H(j \omega) = H_0 j \frac{\omega}{\omega_0}$.

De la même façon que pour les intégrateurs, un vrai dérivateur risque de trop
augmenter les hautes fréquences et de les faire diverger quand il y en a une
infinité (ce qui est toujours techniquement le cas).

Pour éviter ces risques qui peuvent soit enlever la linéarité du système, soit
l'endommager, on choisit plutôt un filtre passe-haut avec $\omega_c \gg \omega$.
On intègre ainsi les harmoniques les plus basses, les harmoniques qui ne créent
pas les discontinuités.

#### Passe-haut du deuxième ordre
$H(j\omega) = \frac{-H_0 (\frac{\omega}{\omega_0})^2}{1 + 2 j \sigma \frac{\omega}{\omega_0} - (\frac{\omega}{\omega_0})^2}$,
soit $\frac{1}{\omega_0^2} \frac{d^2 s}{dt^2} + 2 \frac{\sigma}{\omega_0} \frac{d s}{dt} + 0 = \frac{H_0}{\omega^2} \frac{d^2 e}{dt^2}$.
- $\omega_\text{max}$ (la pulsation de résonance) $> \omega_0$
- Trois cas sont possibles : une grande résonance pour $\sigma < \frac{1}{2}$,
  une plus petite et plus tôt qui colle très vite à l'asymptote en $+\infty$
  pour $\frac{1}{\sqrt{2}} < \sigma < \frac{1}{2}$, et un passage légèrement
  plus bas et plat qu'un premier ordre, sans résonance, pour $\sigma > \frac{1}{\sqrt{2}}$
- $\omega_\text{max}(\sigma)$ tend vers $\omega_0$ quand $\sigma$ tend vers $0$
- On peut utiliser un passe haut d'ordre 2 comme un passe-bande sur la résonance
  (qui est très étroite)

Tout comme l'autre circuit du second ordre, quand $\sigma > 1$ on peut trouver
deux racine imaginaires pures au dénominateur, permettant de séparer en deux
filtres passe-haut du premier ordre se multipliant, ce qui donne un diagramme de
Bode plus simple à observer.

### Passe-bande
#### Définition et diagramme de Bode
Un filtre passe-bande est défini par une fonction de transfert
$H(j\omega) = \frac{H_0 j \frac{\omega}{\omega_0}}{1 + 2 j \sigma \frac{\omega}{\omega_0} - (\frac{\omega}{\omega_0})^2}$,
ce qui correspond à l'équation différentielle
$\frac{1}{\omega_0^2} \frac{d^2 s}{dt^2} + \frac{2 \sigma}{\omega_0} \frac{d s}{dt} + s = \frac{H_0}{\omega_0} \frac{d e}{dt}$.

On a ainsi $G_{dB} = 20 \log(|H|) = 20 \log(\frac{H_0 \frac{\omega}{\omega_0}}{\sqrt{(1 - (\frac{\omega}{\omega_0})^2)^2 + 4 (\frac{\sigma \omega}{\omega_0})^2}})$.
En $\omega \to 0$, on approche $20 \log(\frac{H_0}{\omega_0}) + 20 \log(\omega)$
(asymptote à $+20 dB$ par décade), et en $\omega \to +\infty$, $H$ tend vers $\frac{H_0}{j \frac{\omega}{\omega_0}}$
(et on obtient en gain une asymptote de $-20 dB$ par décade). En $\omega = \omega_0$, $H$ tend vers
$\frac{H_0}{2 \sigma}$, et donc les asymptotes se coupent à l'ordonnée $20 \log(H_0)$ en abscisse $\omega_0$.
De plus, si $\frac{1}{2 \sigma} < 1$, le maximum reste sous les asymptotes
(pas de résonance au milieu de la bande).

- Si $0 < \sigma < \frac{1}{2}$, on a une résonance au milieu de la bande
- Si $\frac{1}{2} < \sigma < \frac{1}{\sqrt{2}}$, pas de résonance et la courbe
  approche beaucoup les asymptotes
- Si $\frac{1}{\sqrt{2}} < \sigma$ a un maximum plus bas sous les asymptotes et est
  plus bas que les asymptotes dans les branches

Le diagramme en phase va de $\frac{\pi}{2}$ à $\frac{-\pi}{2}$
en passant par $0$ en $\omega_0$.

Encore une fois, quand $\sigma > 1$, $H(j \omega) = \frac{H_0' j \frac{\omega}{\omega_0}}{(1 + j \frac{\omega}{\omega_{0_1}}) (1 + j \frac{\omega}{\omega_{0_2}})}$,
ce qui correspond au produit d'un passe-haut du premier ordre et d'un passe-bas
du premier ordre.

#### Forme canonique et étude de la résonance
On réécrit la fonction $H$ sous la forme
$H(j \omega) = \frac{\frac{H_0}{2 \sigma}}{1 + \frac{1}{2 \sigma} j (\frac{\omega}{\omega_0} - \frac{\omega_0}{\omega})}$.
On peut ainsi étudier plus facilement le gain qui s'écrit, avec $H' = \frac{H_0}{2 \sigma}$,
$G = \frac{H_0'}{\sqrt{1 + \frac{1}{4 \sigma^2} (\frac{\omega}{\omega_0} - \frac{\omega_0}{\omega})^2}}$.

On observe donc la bande passante en $G_{dB \text{ max}}-3 dB$ sur le gain en décibels ou $\frac{G_\text{max}}{\sqrt{2}}$
sur le gain. Lorsque $G(\omega) = \frac{G_\text{max}}{\sqrt{2}}$, on a
$H = \frac{H_0'}{\sqrt{2}}$, soit $\frac{\omega}{\omega_0} - \frac{\omega_0}{\omega} = \pm 2 \sigma$.
On recherche la solution à cette équation du second degré, et on obtient comme
solutions positives (si elles existent) $\pm \sigma + \sqrt{1 + \sigma^2 \omega_0^2} \omega_0$,
et on obtient la bande passante qui est de $\Delta \omega = 2 \sigma \omega_0$.

> Le facteur de qualité d'un passe-bande $Q$ est définie comme $\frac{\omega_0}{\Delta \omega}$,
> donc de $\frac{1}{2 \sigma}$ pour un passe-bande du seconde ordre.

On peut donc finalement réécrire la forme canonique sous la forme
$H = \frac{H_0'}{1 + j Q (\frac{\omega}{\omega_0} - \frac{\omega_0}{\omega})}$.

## Traitement numérique d'un signal
### Position du problème
Numériser un signal analogique $s(t)$ consiste à discrétiser $s(t)$ en des
valeurs $s_n = s(t_n)$ avec $t_n = n T_e$. On code ensuite ces valeurs $s_n$ en
valeurs $c_n$ (ce codage est le plus souvent en binaire).

Pour que la numérisation soit de bonne qualité, il faut que le signal codé
puisse restituer un signal analogique $s^{\ast}(t)$ à partir des valeurs
$s_n(t_n)$ "sans qu'on puisse faire la différence" avec $s(t)$.

On peut ainsi plus facilement transmettre le signal : celui-ci ne risque plus
d'être distordus par le moyen de transport car il est binaire. Du bruit ne peut
plus s'installer. Le traitement informatique est aussi assez pratique (bien
qu'on puisse faire beaucoup de choses avec de l'électronique). De plus, le
stockage d'information binaire est très facile et peut se faire sur beaucoup de
choses; pour enregistrer un signal analogique, il faut reproduire l'onde sur une
surface ou volume solide (vinyles).
