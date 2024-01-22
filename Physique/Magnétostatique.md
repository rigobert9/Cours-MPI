# Magnétostatique
## Généralités sur la magnétostatique
### Introduction
On introduit $\overrightarrow{\rm B}$ grâce à la partie magnétique de la force
de Lorentz. L'unité SI de son intensité est le Tesla, mais les valeurs sont
souvent de l'ordre de $10^{-2}$ : le champ électromagnétique terrestre est de
$0,2 \times 10^{-4} T$, un magnet a une intensité $10^{-3} - 10^{-1}$, un
électroaimant a une intensité entre $10^{-2} - 1 T$, et les électroaimant avec
des supraconducteurs dans les réacteurs nucléaires et dispositifs à haute
énergie ont une intensité de $50 T$. On utilise donc souvent le Gauss, qui est
tel que $1 \text{Gauss} = 10^{-4} T$.

### Historique
La magnétite ($Fe_2 O_3$) est un matériau magnétique trouvé dans la nature,
connu depuis l'antiquité. La conception des boussoles a mis en évidence le champ
magnétique terrestre. En 1870, on met en évidence un lien entre le courant
électrique et les aimants, puis on obtient des mises en évidence dans les
circuits électriques de l'induction.

De façon générale, le champ magnétique est créé par les charges en mouvement, et
le champ magnétique agit sur les charges en mouvement. Ainsi, il est
techniquement impossible d'étudier l'électrostatique sans magnétisme, et
inversement, mais il est un réalité possible de faire l'approximation car le
courant se fait dans un conducteur.

### Modélisation du courant électrique
On appelle courant électrique tout mouvement macroscopique de charge. Il est
alors important de ne pas confondre la notion individuelle de vitesse d'une
charge, et la notion statistique de vitesse moyenne quadratique. La vitesse
instantanée d'une charge est de l'ordre de $10^3 m \cdot s^{-1}$, tandis que la
vitesse quadratique moyenne de toutes les charges est de l'ordre du millimètre
par seconde.

On définit l'intensité du courant électrique qui traverse une surface $\overrightarrow{\rm S}$
par $I(\overrightarrow{\rm S}) = \frac{\delta q_T(\overrightarrow{\rm S})}{dt}$.

On montre cette expression de $I(\overrightarrow{\rm S})$. Soit des porteurs de
charge d'un seul type, et tous homocinétiques (de même mouvement tout le temps)
de vitesse $\overrightarrow{\rm V}$. Soit le cylindre d'axe $(O,\overrightarrow{\rm V})$
et de longueur $V dt$ qui s'appuie sur $d \overrightarrow{\rm S}$ (un cylindre
en biais). Une charge traverse $d \overrightarrow{\rm S}$ pendant $dt$ si elle
est dans ce cylindre.\
Pour $S'$ le section du cylindre, $\delta q_T(\overrightarrow{\rm S'}) = n V \times q$
avec $n$ la densité volumique des charges et $V$ le volume du cylindre. Or
$d S' = dS \cos(\theta)$, donnant $V = v dt dS \cos(\theta) = \overrightarrow{\rm v} \cdot d \overrightarrow{\rm S} dt$,
soit $\delta q_T(d \overrightarrow{\rm S}) = n \overrightarrow{\rm v} \cdot d \overrightarrow{\rm S} dt q$,
donc $d I(d \overrightarrow{\rm S}) = n q \overrightarrow{\rm v} \cdot d \overrightarrow{\rm S}$.
On définit le vecteur densité de courant volumique de charge comme $\overrightarrow{\rm j} = n q \overrightarrow{\rm v}$.\
Finalement, $d I (d \overrightarrow{\rm S}) = \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$,
soit $I(\overrightarrow{\rm S}) = \iint_S \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$.
On obtient quelque chose de similaire même s'il y a plusieurs types de charges.

### Raisonnement élémentaire à utiliser
Pour un petit bout de fil électrique parcouru par un courant $I$, on travaillera
souvent avec un modèle simplifié filiforme. Puisqu'on a $I = \overrightarrow{\rm j} \cdot \overrightarrow{\rm s}$,
on a $I d \overrightarrow{\rm \ell} = (\overrightarrow{\rm j} \cdot \overrightarrow{\rm s}) d \overrightarrow{\rm \ell}$
donnant $I d \overrightarrow{\rm \ell} = \overrightarrow{\rm j} d \tau$.

Cette dernière équation permet d'utiliser les connaissances en induction de
première année, comme la force de Laplace notée
$d \overrightarrow{\rm F_L} = \overrightarrow{\rm j} \cdot d \overrightarrow{\rm \ell} \wedge \overrightarrow{\rm B}$.

### Modèles de courant
On peut en tout cas travailler avec le courant volumique dans tous les modèles
de charge.

Pour le modèle volumique, $I = \iint \overrightarrow{\rm j} \cdot d \overrightarrow{\rm S}$.
Le modèle surfacique est hors programme mais peut se retrouver aisément. Le
modèle filiforme est le précédent. Enfin, une charge potentielle en mouvement
produit un courant de $I = \frac{q}{T} = \frac{q V}{2 \pi r}$ (en faisant bien attention à l'orientation).

### Propriété de continuité, de symétrie et d'invariance
#### Continuité
Seule la modélisation volumique est réaliste, dans le sens où $\overrightarrow{\rm B}$ est continu.
Les modèles surfacique et linéïque sont approximés dans le sens où $\overrightarrow{\rm B}$ n'est pas continu au niveau
des sources de champ magnétique.

#### Symétrie
Le champ magnétique est antisymétrique. Les axes de symétrie du courant donnent
donc l'opposé du symétrique du vecteur de l'autre côté des symétries. Ainsi, le
champ magnétique est perpendiculaire aux plans de symétrie, et le champ magnétique
dans les plans d'antisymétrie appartient au plan d'antisymétrie.

#### Invariances
$\overrightarrow{\rm B}$ possède les mêmes invariances que le courant.
