# Calcul différentiel
## Dérivées partielles et différentiabilité
### Situation
On considère dans ce cours les fonctions $f: U \subset E \to F$,
avec $U$ un ouvert de $E$ et $E$ et $F$ des espaces vectoriels de dimension
finie. On rappelle qu'on peut toujours découper l'ensemble d'arrivée sur ses
coordonnées. On se réduira donc sans perte de généralité aux fonctions à valeurs
dans $\mathbb{R}$. En revanche, ces fonctions opèreront toujours sur plusieurs
variables. Tous les théorèmes traiteront donc de telles fonctions avec des
conditions de lisseur supplémentaires.

### Définition de la dérivée partielle
Soit $f: U \subset E$, avec $a \in U$ et $e \in E$,
on définit $\frac{\partial f}{\partial e}(a) = \partial_e f(a)$
comme la dérivée en $0$ de $\varphi(t) = f(a + te)$.

### Différentiabilité
On dit que $f$ est différentiable en $a \in U$
et on pose sa différentielle $d f(a) = \ell$, avec
$\ell \in \mathcal{L}_\mathcal{C}(E,F)$ si pour tout
$h \in U$, $f(a+h) = f(a) + \ell(h) + o(\| h \|)$.

On peut remarquer pour les fonctions de $\mathbb{R}^n$, sous condition
d'existence, la différentielle d'une fonction correspond à son divergent.

> __Théorème (admis) : Caractérisation de $\mathcal{C}^1$ sur $U \subset \mathbb{R}^n$__ : Les deux
> définitions suivantes sont équivalentes :
> - $f$ est différentiable en tout point de $U$, et la fonction associant un point
>   à la différentielle en ce point est continue.
> - Les dérivées partielles sur chaque coordonnée existent et sont continues sur
>   $U$

### Matrice jacobienne
> Soit $f: U \subset \mathbb{R}^n \to \mathbb{R}^m$, avec
> $f(x) = (f_i(x))_{i \in [\![1;m]\!]}$, et $(x_j)_{j \in [\![1;n]\!]}$ une base
> de $\mathbb{R}^n$, on note $Jac(f(a)) = (\frac{\partial f_i}{\partial x_j}(a))_{i,j}$.

Il s'agit de la matrice de $d f(a)$ dans ces bases. On peut s'intéresser ainsi à
des coordonnées plus spéciales, comme les coordonnées polaires. Soit $f = (\rho,\theta) \mapsto (x,y)$,
$Jac(f) = \begin{pmatrix} \frac{\partial x}{\partial \rho} & \frac{\partial x}{\partial \theta} \\ \frac{\partial y}{\partial Gr} & \frac{\partial y}{\partial \theta} \end{pmatrix}^{-1}$
$= \begin{pmatrix} \frac{\partial \rho}{\partial x} & \frac{\partial \rho}{\partial y} \\ \frac{\partial \theta}{\partial x} & \frac{\partial \theta}{\partial y} \end{pmatrix}$.

### Composition
Si $f$ et $g$ sont différentiables respectivement en $a$ et $b = f(a)$,
$g \circ f$ est différentiable en $a$, et on a $d (g \circ f)(a) = d g(b) \times d f(a)$, nous donnant la règle de la chaîne
$(g \circ f)' = (g' \circ f) \times f'$. Plus clairement, $Jac f \circ h = Jac f \times Jac h$.

## Dérivées successives
On définit identiquement les dérivées successives. Par exemple, on dit que
$f: U \subset E \to F$ est $\mathcal{C}^2$ s'il existe $d^2 f = d d f : U \to \mathcal{L}_\mathcal{C}(E, \mathcal{L}_\mathcal{C}(E,F))$.
On définit le gradian $\text{grad} f$ pour $f : U \subset \mathbb{R}^n \to \mathbb{R}$
comme pour $d f(a) \in (\mathbb{R}^n)^{\ast}$, l'application telle que
$d f(a) = ( \text{grad} f | \cdot )$.

###  Définition des continuités supérieurs
> __Théorème (Lemme de Schwartz) :__ Si toutes les dérivées de $f$ à l'ordre plus
> petit ou égal à $n$ et sont continues sur $U$, alors l'ordre de calcul n'intervient pas.

> __Définition :__ $f$ est $\mathcal{C}^k$ si toutes les dérivées d'ordre
> inférieur ou égal à $k$ existent et sont continues sur $U$.

### Extrema
Soit $f: A \subset \mathbb{R}^n \to \mathbb{R}$ avec $A$ ouvert ou non.
Un maximum relatif ou local en $a \in A$ si $f \leq f(a)$ sur un voisinage de $a$, intersecté avec $A$.
On définit identiquement les minima, et on définit les extrema globaux comme
d'habitude.

Si $f$ est $\mathcal{C}^1$ et si $a$ __intérieur__ est un extremum, c'est un
point critique : $df(a) = 0$, $Jac f(a) = 0$ et toutes les dérivées partielles
en $a$ sont nulles (c'est par ces dernières qu'on peut faire la preuve).

## Calculs d'équations à dérivations partielles
### Difféomorphismes
> Un difféomorphisme $\mathcal{C}^k$ est une fonction $\varphi : U \subset E \to V \subset F$
> ($U$ et $V$ ouverts) si elle est bijective et sa fonction inverse sur ces ensembles est
> $\mathcal{C}^k$.

> Théorème d'inversion locale : Si $\varphi: U \to F$ est $\mathcal{C}^1$, et
> si $a \in U$ est tel que le déterminant de la jacobienne de $\varphi$ en $a$
> est non nulle, et que $d \varphi(a) \in GL(E,F)$, $\varphi$ est un
> difféomorphisme $\mathcal{C}^1$ entre un voisinage de $a$
> et un voisinage de $\varphi(a)$.

> Si $\varphi \in \mathcal{C}^1(U,F)$ et que pour tout $a \in U$,
> $\text{det} Jac(\varphi)(a) \neq 0$, alors $\varphi(U)$
> est ouvert et l'image d'un ouvert par $\varphi$ est ouverte.

> Théorème d'inversion globale : Si $\varphi: U \subset E \to F$
> est injective et $\mathcal{C}^1$ et $\text{det} Jac(\varphi)$
> ne s'annule pas sur $U$, $\varphi$ est un difféomorphisme $\mathcal{C}^1$
> de $U$ sur son image, qui est un ouvert.

## Calculs de différentielles
