---
layout: default
title:  "Physique A1 - Chapitre 4 - Régime transitoire - Bases"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy1_04_C
---

# Chapitre 4 : Régimes transitoires dans les circuits linéaires du premier ordre

## 1. Notions de base

### A. Régime permanent

"En physique, un régime permanent est le régime d'un système stable qui peut être observé après un certain temps, lorsque le régime transitoire est terminé."

(Wikipédia)

### B. Régime stationnaire

Le régime stationnaire est un cas particulier du régime permanent, où les tensions et les intensités sont indépendants du temps. 

(On verra un autre cas particulier de régime permanent, le régime permanent sinusoïdal)


### C. Régime transitoire

"En physique, un régime transitoire est le régime d'évolution d'un système qui n'a pas encore atteint un état stable (**un régime permanent**)."

(Wikipédia)

En électronique, on peut rencontrer ce genre de régime transitoire typiquement à l'ouverture / fermeture d'un interrupteur. 

Dans ce chapitre, on va étudier les régimes transitoires dits du **premier ordre**.

Nous allons étudier ce phénomène à travers un exemple simple et courant : la charge et la décharge d'un condensateur.

## 2. Charge et décharge d'un condensateur

### A. Condensateur

Un condensateur est un **dipôle** électrique, composé de deux armatures conductrices, séparées par un isolant (appelé diélectrique)

Il présente la propriété de pouvoir stocker des charges électriques contraires sur ses armatures. Cette propriété est caractérisée par sa **capacité électrique $C$**, exprimée en farads ($F$).

![](./img/04_C/capacitor.webp)

Le courant électrique, généralement noté $i$, correspond lui à un mouvement de charges électriques. On peut le décrire comme étant le *débit de charge électrique*, c'est à dire : $i(t) = \frac{dq}{dt}$.

Le courant dans un condensateur est donc créé lorsque les charges sont en cours d'accumulation (ou de déplétion) sur les armatures. La relation caractéristique du condensateur s'écrit : 
$$ i_C(t) = C \dfrac{du_C}{dt} $$ 

En d'autres termes, il existe un courant électrique dans le condensateur lorsqu'il existe une modification de la tension du condensateur. 

En pratique, on peut relier la charge du condensateur à sa tension en remarquant : 

$$ i_C(t) = \dfrac{dq_C}{dt} = C \dfrac{du_C}{dt}  $$

$$ \Leftrightarrow q_C(t) = C u_C(t) $$

### B. Circuit RC série et charge d'un condensateur

![](./img/04_C/RC_series.png)

- À $t < 0$, on considère que le condensateur est déchargé, et que l'interrupteur est ouvert $\Rightarrow u_C = 0$ et $i=0$.
- À $t=0$, on ferme l'interrupteur (le condensateur va donc commencer à se charger)

On cherche maintenant à déterminer le comportement du circuit pour $t\geq0$

Pour ce faire, nous allons chercher à déterminer $u_C(t)$, en trois étapes : 

1. Écrire les équations caractéristiques du circuit (mailles, noeuds, composants)
2. Établir l'équation différentielle vérifiée par $u_C(t)$
3. Résoudre l'équation différentielle 

*Remarque* : Ces étapes s'appliquent à l'étude de tout circuit pour ce chapitre !  

**Équations caractéristiques du circuit**

- Loi des mailles : $(1) : E = u_C(t) + u_R(t)$
- Loi d'Ohm : $(2) : u_R(t) = R.i(t)$
- Loi du condensateur : $(3) : i(t) = C \dfrac{du_C}{dt}$

On va maintenant combiner ces trois équations afin d'obtenir une équation unique qui ne contient que $u_C(t)$.

*Remarque* : Cette démarche sera toujours possible lorsqu'on a autant d'équations que d'inconnues (et que les équations sont indépendantes, cf. cours de maths). Ici on a trois équations pour trois inconnues : $u_R(t), u_C(t), i(t)$.

**Équation différentielle en $u_C(t)$**

$(3) : i(t) = C \dfrac{du_C}{dt}$

On élimine $i(t)$ en utilisant $(2) : i(t) = \dfrac{u_R(t)}{R}$

$\Leftrightarrow \dfrac{u_R(t)}{R} = C \dfrac{du_C}{dt}$

On élimine $u_R(t)$ en utilisant $(1) : u_R(t) = E - u_C(t)$

$\Leftrightarrow \dfrac{E - u_C(t)}{R} = C \dfrac{du_C}{dt}$

Il ne reste qu'à remettre en forme l'équation : 

$\Leftrightarrow \dfrac{E}{R} - \dfrac{u_C(t)}{R} = C \dfrac{du_C}{dt}$

$\Leftrightarrow \boxed{\dfrac{E}{RC} = \dfrac{du_C}{dt} +\dfrac{u_C(t)}{RC}}$

On obtient ainsi une équation différentielle linéaire du premier ordre à coefficients réels constants.

- Équation différentielle : l'inconnue est une fonction, et l'équation est une relation entre la fonction et ses dérivées. 
- Linéaire : pas de $f^2$
- Premier ordre : uniquement des dérivées d'ordre 1 ($f', \cancel{f''}$)
- On a ici écrit l'équation sous **forme canonique**, c'est à dire que le coefficient devant la dérivée de plus haut ordre est $1$.
- On appelle **second membre** le terme constant dans l'équation différentielle (ici $\frac{E}{RC}$)

**Résolution de l'équation différentielle**

*Remarque* : la méthode détaillée ici sera utilisée pour toutes les équations différentielles d'ordre $1$. 

La résolution se déroule en trois étapes : 
- Solution particulière
- Solution homogène
- Détermination des constantes grâce aux conditions intiales

1. Solution particulière $u_{C,p}(t)$:

On cherche la solution en régime permanent. On sait que lorsque la charge du condensateur sera terminée, on aura $\frac{du_C}{dt} = 0$. L'équation devient alors : 
$$\dfrac{1}{RC} u_{C,p}(t) = \dfrac{E}{RC}$$
$$\Leftrightarrow \boxed {u_{C,p}(t) = E}$$

2. Solution homogène $u_{C,h}(t)$:

On écrit l'équation dite "sans second membre", c'est à dire qu'on écrit l'équation sans les termes qui ne dépendent pas de $u_C(t)$ :
$$\dfrac{du_{C,h}}{dt} + \dfrac{1}{RC} u_{C,h}(t) = 0$$

**Théorème :** L'équation $y'(t) + a.y(t) = 0$ a pour solution : $y(t) = \alpha e^{-at}$ où $\alpha$ est une constante à déterminer. 

Donc ici, on peut en déduire que $\boxed{u_{C,h}(t) = \alpha e^{-\frac{t}{RC}}}$

3. Conclusion (et détermination de la constante $\alpha$) :

La solution complète de l'équation différentielle est : 

$$u_C(t) = u_{C,p}(t) + u_{C,h}(t) = E + \alpha e^{-\frac{t}{RC}}$$

Il faut déterminer $\alpha$ afin de terminer la résolution. Pour ce faire, on doit utiliser une condition intiale qui donne la valeur de $u_C(t)$ à un temps donné. Ici, on sait que $u_C(t=0) = 0$.

Alors, 
$$u_C(t=0) = 0$$
$$\Leftrightarrow E + \alpha e^{-\frac{0}{RC}} = 0$$
$$\Leftrightarrow E + \alpha \times 1 = 0$$
$$\Leftrightarrow \alpha = -E$$

Et on peut donc finalement écrire que : 
$$u_C(t) = E - E e^{-\frac{t}{RC}}$$

ou encore : 

$$\boxed{u_{C}(t) = E\left(1 - e^{-\frac{t}{RC}}\right)}$$

**Tracé de la courbe :**

<video autoplay="true" loop="loop" src="https://raw.githubusercontent.com/vcncolin/lefrenchmathproject/main/assets/manim/RC_series_voltage.mp4" width="640" height="480"></video>

On peut faire plusieurs remarques sur cette courbe : 
- On retrouve bien la valeur $u_C(t\to\infty) = E$
- Il existe plusieurs valeurs remarquables : $u_C(RC) \simeq 0.63E$, $u_C(3.RC) \simeq 0.95E$, $u_C(5.RC) \simeq 0.99E$
- On pourra généralement que le condensateur est complètement chargé après $5.RC$

**Intensité dans le condensateur :**

Une fois le calcul de la tension dans le condensateur effectué, il est assez simple d'accéder à la valeur de l'intensité en utilisant la formule de base : $i(t) = C \dfrac{du_C}{dt}$

On obtient alors : $i(t) = \dfrac{E}{R} e^{-\frac{t}{RC}}$

<video autoplay="true" loop="loop" src="https://raw.githubusercontent.com/vcncolin/lefrenchmathproject/main/assets/manim/RC_series_current.mp4" width="640" height="480"></video>

**Remarque importante :**

L'intensité dans le condensateur est nulle à $t<0$. Il y a donc une discontinuité de l'intensité dans le condensateur au moment ou la charge débute !

### C. Décharge du condensateur : 

On considère désormais que le condensateur est chargé, et qu'on éteint le générateur à $t=0$.

On peut modéliser cette expérience par le circuit ci-dessous :

![](./img/04_C/RC_series_dis.png)

- À $t < 0$, on considère que le condensateur est chargé, et que l'interrupteur est ouvert $\Rightarrow u_C = E$ et $i=0$.
- À $t=0$, on ferme l'interrupteur (le condensateur va donc commencer à se décharger)

On cherche maintenant à déterminer le comportement du circuit pour $t\geq0$

**Équations caractéristiques du circuit**

- Loi des mailles : $(1) : 0 = u_C(t) + u_R(t)$
- Loi d'Ohm : $(2) : u_R(t) = R.i(t)$
- Loi du condensateur : $(3) : i(t) = C \dfrac{du_C}{dt}$

On va maintenant combiner ces trois équations afin d'obtenir une équation unique qui ne contient que $u_C(t)$.

**Équation différentielle en $u_C(t)$**

$(3) : i(t) = C \dfrac{du_C}{dt}$

On élimine $i(t)$ en utilisant $(2) : i(t) = \dfrac{u_R(t)}{R}$

$\Leftrightarrow \dfrac{u_R(t)}{R} = C \dfrac{du_C}{dt}$

On élimine $u_R(t)$ en utilisant $(1) : u_R(t) = - u_C(t)$

$\Leftrightarrow \dfrac{- u_C(t)}{R} = C \dfrac{du_C}{dt}$

Il ne reste qu'à remettre en forme l'équation : 

$\Leftrightarrow \boxed{\dfrac{du_C}{dt} +\dfrac{u_C(t)}{RC} = 0}$

**Résolution de l'équation différentielle**

1. Solution particulière $u_{C,p}(t)$:

On cherche la solution en régime permanent. On sait que lorsque la charge du condensateur sera terminée, on aura $\frac{du_C}{dt} = 0$. L'équation devient alors : 
$$\dfrac{1}{RC} u_{C,p}(t) = 0$$
$$\Leftrightarrow \boxed {u_{C,p}(t) = 0}$$

2. Solution homogène $u_{C,h}(t)$:

*Remarque : Ici l'équation sans second membre est donc la même que l'équation de base !*

On écrit l'équation dite "sans second membre", c'est à dire qu'on écrit l'équation sans les termes qui ne dépendent pas de $u_C(t)$ :
$$\dfrac{du_{C,h}}{dt} + \dfrac{1}{RC} u_{C,h}(t) = 0$$

**Théorème :** L'équation $y'(t) + a.y(t) = 0$ a pour solution : $y(t) = \alpha e^{-at}$ où $\alpha$ est une constante à déterminer. 

Donc ici, on peut en déduire que $\boxed{u_{C,h}(t) = \alpha e^{-\frac{t}{RC}}}$

3. Conclusion (et détermination de la constante $\alpha$) :

La solution complète de l'équation différentielle est : 

$$u_C(t) = u_{C,p}(t) + u_{C,h}(t) =  0 +  \alpha e^{-\frac{t}{RC}}$$

Il faut déterminer $\alpha$ afin de terminer la résolution. Pour ce faire, on doit utiliser une condition intiale qui donne la valeur de $u_C(t)$ à un temps donné. Ici, on sait que $u_C(t=0) = E$.

Alors, 
$$u_C(t=0) = E$$
$$\Leftrightarrow \alpha e^{-\frac{0}{RC}} = E$$
$$\Leftrightarrow \alpha = E$$

Et on peut donc finalement écrire que : 

$$\boxed{u_{C}(t) = Ee^{-\frac{t}{RC}}}$$

**Tracé de la courbe :**

<video autoplay="true" loop="loop" src="https://raw.githubusercontent.com/vcncolin/lefrenchmathproject/main/assets/manim/RC_series_voltage_dis.mp4" width="640" height="480"></video>


### D. Exercice d'application : 

On considère le circuit suivant : 

![](./img/04_C/RC_application.png)

- À $t < 0$, on considère que le condensateur est déchargé, et que l'interrupteur est ouvert.
- À $t=0$, on ferme l'interrupteur.

1. Que vaut $u_C(t=0)$?
2. Déterminer $u_C(t)$ pour $t>0$.
3. Une fois le régime permanent atteint dans la situation précédente, on rouvre  l'interrupteur. On choisit comme nouvelle origine des temps cet instant. Donner la nouvelle expression de $u_C(t)$.

### SOLUTION :

Il est de bon usage de commencer par annoter tout le circuit : 

![](./img/04_C/RC_application_annot.png)

1. Le condensateur étant déchargé à $t=0$, on peut dire que $u_C(t=0)=0$. 

2. On fait tout d'abord l'inventaire des équations caractéristiques du circuit : 

- $(1)$ Loi des mailles : $E - u_{R_1}(t) - u_{R_2}(t) = 0$
- $(2)$ Loi des mailles : $u_{R_2}(t) = u_C(t)$
- $(3)$ Loi des noeuds : $i(t) = i_C(t) + i_R(t)$
- $(4)$ Loi d'Ohm : $u_{R_1}(t) = R_1 . i(t)$
- $(5)$ Loi d'Ohm : $u_{R_2}(t) = R_2 . i_R(t)$
- $(6)$ Loi du condensateur : $i_{C}(t) = C \dfrac{du_C}{dt}$

$$(6) : i_{C}(t) = C \dfrac{du_C}{dt}$$

On remplace $i_C(t)$ en utilisant $(3) : i_C(t) = i(t) - i_R(t)$

$$\Leftrightarrow i(t) - i_R(t) = C \dfrac{du_C}{dt}$$

On remplace $i(t)$ et $i_R(t)$ en utilisant $(4, 5) : i(t) = \dfrac{u_{R_1}(t)}{R_1}, i_R(t)= \dfrac{u_{R_2}(t)}{R_2}$

$$\Leftrightarrow  \dfrac{u_{R_1}(t)}{R_1} - \dfrac{u_{R_2}(t)}{R_2} = C \dfrac{du_C}{dt}$$

On remplace $u_{R_1}(t)$ et $u_{R_2}(t)$  en utilisant $(1, 2) : u_{R_2}(t) = u_{C}(t), u_{R_1}(t)= E - u_{R_2}(t) = E - u_{C}(t)$

$$\Leftrightarrow  \dfrac{E - u_{C}(t)}{R_1} - \dfrac{u_{C}(t)}{R_2} = C \dfrac{du_C}{dt}$$

Il ne reste plus qu'à remettre l'équation en forme : 

$$\Leftrightarrow  C \dfrac{du_C}{dt} = \dfrac{E}{R_1} - \dfrac{u_{C}(t)}{R_1} - \dfrac{u_{C}(t)}{R_2} $$

$$\Leftrightarrow  C \dfrac{du_C}{dt} + \dfrac{u_{C}(t)}{R_1} + \dfrac{u_{C}(t)}{R_2}= \dfrac{E}{R_1}$$

$$\Leftrightarrow  C \dfrac{du_C}{dt} + R_2\dfrac{u_{C}(t)}{R_1R_2} + R_1\dfrac{u_{C}(t)}{R_1R_2}= \dfrac{E}{R_1}$$

$$\Leftrightarrow  C \dfrac{du_C}{dt} + \dfrac{R_1+R_2}{R_1R_2}u_C(t)= \dfrac{E}{R_1}$$

$$\Leftrightarrow  \boxed{\dfrac{du_C}{dt} + \dfrac{R_1+R_2}{R_1R_2C}u_C(t)= \dfrac{E}{R_1C}}$$

On peut alors résoudre l'équation différentielle : 

- Solution particulière : $\dfrac{du_C}{dt} = 0$

$$\Leftrightarrow  \dfrac{R_1+R_2}{R_1R_2C}u_{C,p}(t)= \dfrac{E}{R_1C}$$

$$\Leftrightarrow  u_{C,p}(t)= \dfrac{E}{\cancel{R_1C}}.\dfrac{\cancel{R_1}R_2\cancel{C}}{R_1+R_2}$$

$$\Leftrightarrow  \boxed{u_{C,p}(t)= \dfrac{ER_2}{R_1+R_2}}$$

- Solution homogène :

$$\dfrac{du_{C,h}}{dt} + \dfrac{R_1+R_2}{R_1R_2C}u_{C,h}(t)= 0$$

D'après le théorème, on a alors : $\boxed{u_{C,h}(t) = \alpha \exp\left(\dfrac{-(R_1+R_2)t}{R_1R_2C}\right)}$

- Conclusion :

$$u_C(t) = u_{C,p}(t) + u_{C,h}(t) = \dfrac{ER_2}{R_1+R_2} + \alpha \exp\left(\dfrac{-(R_1+R_2)t}{R_1R_2C}\right)$$

On détermine $\alpha$ grâce à la condition initiale $u_C(t=0)=0$ : 

$$u_C(t=0) = 0$$

$$\Leftrightarrow \dfrac{ER_2}{R_1+R_2} + \alpha \exp\left(\dfrac{-(R_1+R_2).0}{R_1R_2C}\right) = 0$$

$$\Leftrightarrow \dfrac{ER_2}{R_1+R_2} + \alpha .1 = 0$$

$$\Leftrightarrow \alpha = - \dfrac{ER_2}{R_1+R_2}$$

Et on en déduit finalement : 

$$\boxed{u_C(t) = \dfrac{ER_2}{R_1+R_2}\left(1 - \exp\left(\dfrac{-(R_1+R_2).t}{R_1R_2C}\right)\right)}$$

Dans ces cas là, il peut être utile de poser $\tau = \dfrac{R_1R_2C}{R_1+R_2}$ afin de simplifier l'écriture de l'équation : 

$$\boxed{u_C(t) = \dfrac{ER_2}{R_1+R_2}\left(1 - \exp\left(\dfrac{-t}{\tau}\right)\right)}$$

3. Lorsqu'on rouvre l'interrupteur : 
- Le circuit redevient un simple circuit RC série
- La condition initiale devient le régime permanent de l'étude précédente, donc $u_C(t=0) = \frac{ER_2}{R_1+R_2}$

L'équation différentielle est alors la même que celle du cours : 

$\boxed{\dfrac{du_C}{dt} +\dfrac{u_C(t)}{R_1C} = \dfrac{E}{R_1C}}$

**Résolution :**

- Solution particulière :

$$\dfrac{1}{R_1C} u_{C,p}(t) = \dfrac{E}{R_1C}$$
$$\Leftrightarrow \boxed {u_{C,p}(t) = E}$$

- Solution homogène :

$$\dfrac{du_{C,h}}{dt} + \dfrac{1}{R_1C} u_{C,h}(t) = 0$$

$$\Leftrightarrow \boxed{u_{C,h}(t) = \alpha e^{-\frac{t}{R_1C}}}$$

- Conclusion (et détermination de la constante $\alpha$) :

La solution complète de l'équation différentielle est : 

$$u_C(t) = u_{C,p}(t) + u_{C,h}(t) =  E  +  \alpha e^{-\frac{t}{R_1C}}$$

Or, 
$$u_C(t=0) = \dfrac{ER_2}{R_1+R_2} $$
$$\Leftrightarrow E + \alpha e^{-\frac{0}{R_1C}} = \dfrac{ER_2}{R_1+R_2}$$
$$\Leftrightarrow \alpha = \dfrac{ER_2}{R_1+R_2} - E$$
$$\Leftrightarrow \alpha = \dfrac{ER_2}{R_1+R_2} - E\dfrac{R_1 + R_2}{R_1+R_2}$$
$$\Leftrightarrow \alpha = -\dfrac{ER_1}{R_1+R_2}$$

Et on peut donc finalement écrire que : 

$$\boxed{u_{C}(t) = E -\dfrac{ER_1}{R_1+R_2}e^{-\frac{t}{R_1C}}}$$