# Séries numériques
## Généralités
### Définition
On travaillera sur des suites indexées par les entiers naturels (qu'on
commencera par convention à $0$ dans tous les cas) à valeurs dans $\mathbb{R}$,
$\mathbb{C}$, ou dans des espaces vectoriels de dimension finie.

> On définit pour toute suite $(u_{n})_\mathbb{N}$ la suite des sommes partielles
> $S_n(u) = \sum\limits_{k = 0}^{n} u_k$. On dit que $\sum\limits_{k = 0}^{+\infty}$ converge vers $\ell$
> si $S_n(u) \xrightarrow[n \to +\infty]{} \ell$.

Lorsque $\sum\limits_{k = 0}^{+\infty} u_{k}$ converge, pour $n_0 \geq 0$
$\sum\limits_{k = n_0 + 1}^{+\infty} u_k$ converge et
$\sum\limits_{k = 0}^{+\infty} u_k = \sum\limits_{k = 0}^{n_0} u_k + \sum\limits_{k = n_0 + 1}^{+\infty} u_k$.
On pose alors $R_n(u) = \sum\limits_{k = n + 1}^{+\infty} u_k$ (on ne peut en
parler uniquement si elle est convergente).

> Une série divergente est une série qui ne converge pas.

### Positivité
Si $(u_{n})$ est à valeurs dans $\mathbb{R}^+$, $S_n$ est croissante, permettant
de dissocier deux cas faciles : soit $S_n$ converge, soit elle diverge vers
$+\infty$. On ne peut en revanche pas utiliser ceci directement pour une suite
qui n'est pas dans $\mathbb{R}^+$ : on va introduire des outils permettant
d'utiliser ceci en première approche.

### Convergence absolue
Pour toute suite $(u_{n})$, on dit que la série $\sum u_{k}$ converge absolument
si $\sum \| u_k \|$ converge. On prouve que cette convergence absolue implique
la convergence.

En effet, on nous dit alors que $S_n(u)$ est bornée. Comme les valeurs prises
par $S_n(u)$ sont alors dans un compact, il existe au moins une valeur
d'adhérence, dont on doit prouver seulement l'unicité. En prenant la différence
entre deux sommes partielles en des extractrices vers ces deux valeurs, on peut
majorer cette différence par le reste de la série absolue, qui converge vers
$0$.

Plus simplement, puisque l'espace est complet, on montre que les sommes
partielles sont une suite de Cauchy en majorant pour des $p,q$ assez grands
par la différence de leurs sommes partielles absolues.

### Lien suite-série
On peut souvent définir pour une suite $(v_{n})$ la suite des différences
$(u_{n})$ par $u_{n} = v_{n+1} - v_{n}$. Celle-ci converge si et seulement si
$v_{n}$ converge, et si c'est bien le cas, $\sum\limits_{n = 0}^{+\infty} u_{n}$
$= \lim\limits_{n \to + \infty} v_{n} - v_0$.

Avec ce théorème, on peut déduire la convergence ou divergence pour
$v_{n} = \frac{1}{n}$ et $u_{n} = - v_{n+1} + v_n = \frac{1}{n (n+1)} \geq \frac{1}{(n + 1)^2}$
ou pour $v_{n} = \ln(n)$ et $u_{n} = \ln(1 + \frac{1}{n}) \leq \frac{1}{n}$.

## Séries à termes positifs
### Règle d'Alembert (comparaison à une suite géométrique)
> Soit $u_{n} \in \mathbb{R}_{+}^{\ast}$ à partir d'un certain rang, si $\frac{u_{n+1}}{u_{n}} \to \ell$ :
> - Si $\ell < 1$, la suite converge
> - Si $\ell > 1$, la suite diverge grossièrement (c'est à dire que $u_{n} \to a > 0$,
>   ce qui diverge toujours pour une suite à valeurs dans
>   $\mathbb{R}_{+}^{\ast}$)
> - Si $\ell = 1$, on ne peut rien conclure de plus par ce critère

> De façon générale, si $0 \leq u_{n} \leq v_{n}$ à partir d'un certain rang,
> la convergence de $\sum v_{n}$ implique celle de $\sum u_{n}$, et la divergence
> de $\sum u_{n}$ entraîne la divergence de $\sum v_{n}$.

En corollaire, on pour $\frac{u_{n+1}}{u_{n}} \leq \frac{v_{n+1}}{v_{n}}$ avec
$u_{n}$ et $v_{n}$ non nuls à partir d'un certain rang, la convergence de $\sum v_{n}$
entraîne celle de $\sum u_{n}$, et la divergence de $\sum u_{n}$ donne la
divergence $\sum v_{n}$. (On le prouve avec $u_{n+1} \leq \frac{u_{n_0}}{v_{n_0}} v_{n+1}$).

À l'aide de ces lemmes, avec $\rho$ un majorant du quotient $\frac{u_{n+1}}{u_{n}}$,
on compare à la suite $(\rho^n)$ dont on trouve la convergence et divergence en
étudiant la suite géométrique.

### Règle des équivalents
Soit $u_{n} \sim v_{n}$, si celles-ci sont positives à partir d'un certain rang,
leurs séries sont de même nature (convergente ou divergente). De plus, si elles
sont divergentes, leur sommes partielles sont équivalentes, et si elles
convergent, leurs restes sont équivalents (ATTENTION : ces deux propriétés ne
passent pas au cas opposé).

__Preuve :__ On peut borner $u_{n}$ par $(1 - \varepsilon) v_{n} \leq u_{n} \leq (1 + \varepsilon) v_{n}$
à partir d'un certain rang car $u_{n} = q_n v_{n}$ à partir d'un certain rang
avec $q_n \to 1$.

### Règle des $O$ et $o$ (négligeabilité et limitation)
Si $u_{n} = o(v_{n})$ (respectivement $O(v_{n})$), avec $v_{n}$
positive à partir d'un certain rang (pas d'hypothèses sur $u_{n}$), alors :
- Si $\sum v_{n}$ converge alors $\sum u_{n}$ converge et
  $R_n(u) = o(R_n(v))$ (respectivement $O(R_n(v))$)
- Si $\sum v_{n}$ diverge alors : si $\sum u_{n}$ converge,
  $S_n(u) = o(S_n(v))$ (respectivement $O(S_n(v))$); et si $\sum u_{n}$ diverge,
  $S_n(u) = o(S_n(v))$ (respectivement $O(S_n(v))$)

Attention, cela signifie que la divergence de $v_{n}$ ne présage pas la
convergence ou divergence de $u_{n}$ (quelque chose de fini est négligeable face
à quelque chose d'infini).

### Comparaison à une série de Riemann
Ce critère est "plus fin" que le premier, il est rarement utile d'essayer le
premier après que celui-ci ne donne rien.

> $\sum \frac{1}{n^\alpha}$ diverge grossièrement si $\alpha \leq 1$, et converge
> si $\alpha > 1$.

Un autre bon exemple avec la même preuve est que $\sum \frac{(-1)^n}{n^\alpha}$
diverge grossièrement si $\alpha \leq 0$. On peut aussi chercher à prouver
qu'elle est semi-convergente sinon.

__Preuve :__ Comparaison à une intégrale (se voit bien sur un graphe) :
soit $f(t) = \frac{1}{t^\alpha}$, on a $\int\limits_{n}^{n + 1} f \leq f(n) \leq \int\limits_{n-1}^{n} f$
donnant $\int\limits_{1}^{N} f(t) dt + f(N) \leq \sum\limits_{k = 1}^{N} f(k) \leq \int\limits_{1}^{N} f(t) dt + f(1)$.
$f$ est intégrable sur $[1;+\infty[$ si $\alpha > 1$, et non intégrable sur cet
intervalle si $\alpha \leq 1$, donnant que $S_N$ est bornée donc convergente si
$\alpha > 1$ et qu'elle diverge sinon. De plus, si $\alpha \leq 1$,
$\int\limits_{1}^{N} f = \frac{1}{1 - \alpha} N^{1 - \alpha}$ (pour $\alpha < 1$),
et comme $f(1), f(N) = o(N^{1 - \alpha})$, on a $S_N \sim \frac{N^{1 - \alpha}}{\alpha - 1}$.
Enfin, si $\alpha > 1$, $\int\limits_{1}^{N} f = \frac{1}{(\alpha - 1) N^{\alpha - 1}}$
permettant d'avoir identiquement $R_N \sim \frac{1}{(\alpha - 1) N^{\alpha - 1}}$.\
Cette technique peut marcher sur des suites complexes, il convient donc de la
connaître et de la maîtriser.

__Autre preuve :__ Lien suite-série : On peut parfois essayer de faire des
choses avec une suite sortie de l'intégrale de notre suite, dont la différence
est équivalente à notre suite. Pour $u_{n} \geq 0$, si $n^{\alpha} u_{n} \to 0$
avec $\alpha > 1$ alors $\sum u_{n}$ converge, et si cela converge vers $+\infty$
pour $\alpha \leq 1$, $\sum u_{n}$ diverge. (Dans le premier cas, $u_{n} = o(\frac{1}{n^{\alpha}})$)
et dans le deuxième, $\frac{1}{n^{\alpha}} = o(u_{n})$

### Méthodes pratiques
On peut généraliser la règle d'Alembert en utilisant les valeurs absolues,
donnant la convergence absolue. Pour la règle des équivalents, il s'agit de
faire un développement asymptotique jusqu'à un terme absolument convergent ou
un signe constant.

### Critère spécial des séries alternées (CSSA)
On appelle $\sum u_{n}$ semi-convergente si elle converge sans pour autant être absolument
convergente (le terme permet juste d'expliciter qu'on en sait pas plus).

$\sum \frac{(-1)^n}{n^\alpha}$ est semi-convergente si et seulement si $\alpha > 0$
pour $\alpha \in \mathbb{R}$

> Si $u_{n} = (-1)^n a_n$ pour $(a_n)$ décroissante convergeant en $0$,
> $\sum u_{n}$ converge (par majoration de $|R_n|$ par $a_{n+1}$).

### Transformation d'Abel
C'est l'équivalent de l'intégration par parties pour les séries.

Soit $u_{n} = a_n b_n$ pour tout $n$, on note $A_n = \sum\limits_{k = 0}^{n} a_k$,
alors $\sum\limits_{k = p}^{q} u_k = \sum\limits_{k = p}^{q} (A_k - A_{k-1}) b_k$
$= \sum\limits_{k = p}^{q - 1} A_k (b_k - b_{k+1}) + A_q b_q - A_{p - 1} b_p$.
En pratique, on calcule $A_n$ et on en déduit la convergence ou d'autres
propriétés.

Par exemple $\frac{e^{in x}}{n^{\alpha}}$, avec $a_n = e^{i n x}$,
ou encore $\frac{e^{i \sqrt{n} x}}{n^{\alpha}}$ avec
$a_n = \frac{e^{i x \sqrt{n}}}{\sqrt{n}} !$.

### Comparaison à une intégrale
Un cadre simple d'étude est par exemple celui de $u_{n} = f(n)$ avec $f$
monotone. Plus généralement, on pose $v_n = u_n - \int\limits_{n}^{n + 1} f$ et
on cherche à avoir $\sum v_n$ convergente. Le problème se tourne alors vers la
convergence d'une intégrale à l'infini de $f$

Par exemple, pour $f(t) = \frac{e^{i x \sqrt{t}}}{t}$, on a
$v_n = \int\limits_{n}^{n + 1} f(t) dt - \frac{e^{i x \sqrt{n}}}{n}$
$=\int\limits_{n}^{n + 1} (f(t) - f(n)) dt$.
On a $|f(t) - f(n)| \leq (1 + \frac{|x|}{2}) \frac{1}{n^{\frac{3}{2}}}$,
donc $v_n = O(\frac{1}{n^{\frac{3}{2}}})$ et elle est donc absolument
convergente. Ainsi, $S_n(u) = S_n(v) + \int\limits_{1}^{n+1} f(t) dt$

### Sommabilité : ensemble $\ell^1$
$\ell^1$ est l'espace des suite dont la série est absolument convergente.

#### Produit de Cauchy
Soit $a_n$, $b_n$ deux séries de $\ell^1$, la série de $c_n = \sum\limits_{p + q = n} a_p b_q$
est absolument convergente et $\sum\limits_{n \geq 0} c_n = (\sum\limits_{n \geq 0} a_n) (\sum\limits_{n \geq 0} b_n)$.
On appelle cette série le produit de Cauchy de deux séries absolument
convergentes.

Par exemple, connaissant pour $|x| < 1$, $- ln(1 - x) = \sum\limits_{n \geq 1} \frac{x^n}{n}$
et $\frac{1}{1 - x} = \sum\limits_{n \geq 0} x^n$, donnant
$\frac{- \ln(1 - x)}{1 - x} = \sum\limits_{p + q = n} \frac{1}{p} 1 x^p x^q$
$= \sum H_n x^n$.

#### Théorème de Fubini
Soit la suite $(u_{n,m})_{n,m}$, on note $S_n = \sum\limits_{m = 0}^{+\infty} u_{n,m}$
et $T_m = \sum\limits_{n = 0}^{+\infty} u_{n,m}$. Si la suite est toujours
positive, alors $\sum S_n$ converge si et seulement si $\sum T_m$
et elles sont alors égales ($\sum\limits_{n \geq 0} \sum\limits_{m \geq 0} u_{n,m}$
$= \sum\limits_{m \geq 0} \sum\limits_{n \geq 0} u_{n,m}$). On dit alors que
cette suite à deux indices est $\ell^1$.

De façon générale, on dire qu'une suite est sommable si la suite de la valeur
absolue de chaque terme est sommable.

#### Sommation par paquets
Soit $(u_{n,m})$ sommable, et une décomposition de $\mathbb{N} \times \mathbb{N}$
en union disjointe de $(I_k)$, alors si $R_p = \sum\limits_{(n,m) \in I_p} u_{n,m}$,
$\sum\limits_{n} \sum\limits_{m} u_{n,m} = \sum\limits_{p} R_p$.
