# Extensions de corps
On considère un corps $\mathbb{K} \subset \mathbb{C}$, et l'application
$\begin{aligned} f: K[X] &\to \mathbb{C} \\ P &\mapsto P(\alpha) .\end{aligned}$.
On note $\mathbb{K}[\alpha] = \text{Im}(f)$.

Cette application est un morphisme d'anneaux, et donc son noyau est un idéal.
Pour un polynôme $\pi$ engendrant l'idéal (et qui soit unitaire), on dit qu'il
s'agit du polynôme minimal de $\alpha$. Si $\pi = 0$, $\alpha$ est transcendant,
et si $f$ n'est pas algébrique, $\alpha$ est algébrique, et on appelle $d_\mathbb{K} \alpha$
le degré du polynôme minimal.

Lorsque $\alpha \in \mathbb{K}$, le degré est $1$. $\mathbb{K}[\alpha]$ est de
degré $d_\mathbb{K} \alpha$ (et on peut voir par division euclidienne qu'il est
isomorphe à aux polynômes de moins 1 de ce degré). $\mathbb{K}[\alpha]$
est donc $\mathbb{K}[X] / (\pi)$.

Si $\alpha$ est algébrique sur $\mathbb{K}$, $\pi_\alpha$ est uniquement
caractérisé par le fait que $\alpha$ soit une de ses racines et qu'il soit
irréductible.

Quand $\alpha$ est algébrique, $\mathbb{K}[\alpha]$ est un corps. En effet,
soit $\begin{aligned} \mathbb{K}[\alpha] &\to \mathbb{K}[\alpha] \\ x &\mapsto \beta x, \beta \in \mathbb{K}[\alpha] .\end{aligned}$,
comme c'est une application linéaire, elle est clairement injective (pour les
corps qui nous concernent), et donc est surjective (endomorphisme de dimension
finie), donc il existe un antécédent à $1$ qui est notre inverse.
Sinon, soit $B = P(\alpha)$, si $\pi_{\alpha} \not \mid P$, comme $\pi_d$
est irréductible leur PGCD est $1$, et donc Bézout nous donne un inverse.

### Exemple important
On prend $\alpha = \sqrt{2} + \sqrt{3}$. Comme $\alpha^2 = 5 + 2 \sqrt{6}$,
on a $(\alpha^2 - 5)^2 = 24 \Rightarrow \alpha^4 - 10 \alpha^2 + 1 = 0$
un annulateur. On cherche à voir s'il existe un diviseur de ce polynôme.

S'il existait un diviseur de degré 1 (et donc par dualité un diviseur de degré 3),
on trouverait $x = \frac{p}{q}$ une racine du polynôme dans $\mathbb{Q}$. On
aurait ainsi $p \mid a_0$ et $q \mid a_n$ (voir le polynôme sous forme sommée
fois $q^n$ et la divisibilité de 0). Ici, on a donc $p \mid 1$, $q \mid 1$, donc
$x = \pm 1$, ce qui n'est pas le cas.

Pour vérifier s'il existe un diviseur de degré 2, c'est plus difficile. On va
empiler des extensions finies. Soit $[K : k]$ le degré de $\mathbb{K}$ comme
$k$-EV (ainsi, $[\mathbb{K}[\alpha] : \mathbb{K}] = d_{\mathbb{K}} \pi_d = d_{\mathbb{K}} \alpha$).
Si $L$ est une extension finie de $K$ et $K$ est une extension finie de $k$,
alors $L$ est une extension finie de $k$, $L$ est une extension finie de $k$ et
$[L : k] = [L : K] [K : k]$. On le vérifie en prenant une base de chaque EV et
en faisan une base de $L$ avec $k$.

Soit $K \succeq k$ ($K$ étend $k$), on a $d_k \alpha \leq d_K \alpha$.
Or $\mathbb{Q}[\sqrt{2},\sqrt[3]{2}] \succeq \mathbb{Q}[\sqrt{2}] \preceq \mathbb{Q}$
et $\mathbb{Q}[\sqrt{2},\sqrt[3]{2}] \succeq \mathbb{Q}[\sqrt[3]{2}] \preceq \mathbb{Q}$.
Comme $[\mathbb{Q}[\sqrt{2},\sqrt[3]{2}] : \mathbb{Q}[\sqrt{2}]] \leq 3$
(et $\leq 2$ pour l'autre), $[\mathbb{Q}[\sqrt{2},\sqrt[3]{2}] : \mathbb{Q}] \leq 6$,
mais comme $2$ et $3$ divisent ce degré, on a
$[\mathbb{Q}[\sqrt{2},\sqrt[3]{2}] : \mathbb{Q}] = 6$.(Faire dessin de la
pyramide).

### Valuation $p$-adique
Soit $p$ un nombre premier, pour $x \in \mathbb{N}^{\ast}$, $v_p(x) = n$
quand $p^n \mid x$ et $p^{n+1} \not \mid x$. On étend cette valuation à $\mathbb{Q}^{\ast}$,
en prenant $v_p(\frac{a}{q}) = v_p(a) - v_p(q)$. On peut reconstituer la valeur
absolue d'un nombre à partir de sa valuation $p$-adique en tous ses facteurs
premiers (forcément). On a ainsi $[\mathbb{Q}[\sqrt{p_1},\ldots,\sqrt{p_n}] : \mathbb{Q}] = 2^s$
pour des nombres premiers deux à deux inégaux. On peut le voir par extensions
successives qui ajoutent ces racines, car $d_\varphi \sqrt{p_{n}} = 2$.

### Théorie de Galois
Un plongement est un morphisme de corps $K \to \mathbb{C}$. Il laisse donc $\mathbb{Q}$
invariant ($\mathbb{Q} = \sigma(\mathbb{Q})$).

En prenant l'exemple de $\mathbb{Q}[\sqrt{2}]$, on peut trouver deux plongements
: l'identité et le conjugué. L'idée centrale de la théorie de Galois est la
correspondance entre le nombre de plongements et le degré de l'extension.
Soit l'extension $\mathbb{K} \preceq \mathbb{K}[\alpha]$, et $\beta$ racine dans
$\mathbb{C}$ de $\pi_\alpha$, et $\sigma \in \mathbb{C}^{K}$, on admet que
$\exists! \overline{\sigma} \mathbb{K}[\alpha] \to \mathbb{C}$ qui prolonge $\sigma$ sur $K$
et tel que $\overline{\sigma}(\alpha) = \beta$.

Il existe autant de plongements dans $K_n = \mathbb{Q}[\sqrt{p_1},\ldots,\sqrt{p_n}]$
que de façons de mettre plus ou moins aux racines (car $\sigma(\sqrt{p_n})^2 = \sigma(p_n) = p_n$)
(donc $2^n$) (on peut le prouver par récurrence).

Comme $\pi_\alpha(\alpha) = 0$, $\sigma_i(\pi_\alpha(\alpha)) = 0 \Rightarrow \pi_\alpha(\sigma_i(\alpha)) = 0$.
On peut prouver que $(\sigma_i(\alpha))_i$ sont des éléments un à un distincts,
qui sont les racines de $\pi_a$ dans $\mathbb{C}$, ce qui signifie que son degré
est de $2^n$, vérifiant ainsi que pour $\alpha = \sum\limits_{k = 0}^{n} a_k \sqrt{p_k}$,
$\mathbb{Q}[\alpha] = \mathbb{Q}[\sqrt{p_1},\ldots,\sqrt{p_n}]$.
