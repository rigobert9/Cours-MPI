# Cours de chimie
## Étude quantitative et calcul de pH
### Prévision des réaction prépondérantes
#### Règle du gamma
Soit la réaction entre les deux couples $A_1 H / A_1^{-}$
et $A_2 H / A_2^-$, $(R) A_1 H + A_2^- = A_1^- A_2 H$.
Or, ces deux couples, lorsqu'ils réagissent avec l'eau,
ont les constantes d'équilibre $K_{A_{1}}$ et $K_{A_2}$.
Comme $R$ est la différence des réactions de chaque couple avec l'eau, on a
$K_R = \frac{K_{A_1}}{K_{A_2}}$.

Ainsi, $K_{A_1} \gg K_{A_2} \Rightarrow K_R \gg 1$ (réaction dans le sens $1$)
et inversement. En présence de deux couples, on a donc l'acide le plus fort
($pK_A$ le plus petit) qui réagit sur la base la plus forte ($pK_A$ le plus grand).

### Calcul de pH
#### Acide fort dans l'eau
On étudie la réaction, qui est totale comme l'acide est fort,
$AH + H_2 O \to A^-  + H_3 O^+$. Attention, il y a une concentration de $H_3 O^+$
de $10^{-7} mol \cdot L^{-1}$, qu'on néglige le plus souvent s'il y a assez de
concentration d'acide.

#### Acide faible dans l'eau
On a alors $K_A = \frac{[A^-] [H_3 O^+]}{[AH]} = \frac{\frac{\zeta^2}{v^2}}{\frac{C_0 V - \zeta}{V}}$
$= \frac{\zeta^2}{(C_0 V - \zeta) V}$. Soit on résout cette équation du second
degré, soit on approxime en utilisant $K_A \ll 1$, donc $\zeta \ll C_0 V$
$\Rightarrow \zeta = \sqrt{K_A C_0 V^2} \Rightarrow [H_3 O^+] = \frac{\zeta}{V} = \sqrt{K_A C_0}$.
On obtient alors $pH = \frac{1}{2} (p K_A - \log C_0)$.

Attention, cette formule n'est utilisable que si le $pH$ de l'acide est
inférieur à 6, donc que la concentration de $H_3 O^+$ initiale est petite devant
la concentration finale. Cela traduit que $\zeta \ll C_0 V \Rightarrow [A^-] < [AH]$
$\Rightarrow pH f < p K_A - 1$.

#### Base forte
On a en faisant l'équation $pH = p K_e + \log C_0$.

#### Base faible
On obtient $K_A = \frac{K_e (C_0 V - \zeta) V}{\zeta^2}$,
et on faisant l'approximation $C_0 V - \zeta  \approx C_0 V$, on a
$\zeta = \sqrt{\frac{K_e C_0 V^2}{K_A}} \Rightarrow [OH^-] = \sqrt{\frac{K_e C_0}{K_A}}$.
On a $[H_3 O^+] = \frac{K_e}{[OH^-]} = \sqrt{\frac{K_e K_A}{C_0}}$.

Ainsi, $pH = \frac{1}{2} (pK_e + pK_A + \log C_0)$.
