---
layout: default
title:  "Physique A1 - Chapitre 5 - Oscillateurs électriques"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy1_05_C
---

# Chapitre 5 : Oscillateurs électriques

## 1. Étude du problème de base : le circuit LC série

![](./img/05_C/LC_series.png)

On s'intéresse au circuit représenté ci-dessus. À $t=0$, on ferme l'interrupteur. On s'intéresse à la tension $u_C(t)$ pour $t>0$.

### A. Étude qualitative

On peut se demander comment va évoluer la tension du condensateur. En effet, dans un premier temps, lorsqu'on ferme l'interrupteur, la bobine va s'opposer à l'établissement du courant dans le circuit. Puis, progressivement, le courant va s'établir, et les charges vont s'accumuler sur le condensateur.

### B. Étude quantitative

On procède de la même manière que dans le chapitre précédent. 

**Équations caractéristiques du circuit :**

- Loi des mailles : $(1) : 0 = u_C(t) + u_L(t)$
- Loi du condensateur : $(2) : i(t) = C \dfrac{du_C}{dt}$
- Loi de la bobine : $(3) : u_L(t) = L \dfrac{di}{dt}$

**Établissement de l'équation différentielle en $u_c(t)$ :**


On part de l'équation $(2) : i(t) = C \dfrac{du_C}{dt}$.

On voudrait éliminer $i(t)$, mais on ne dispose que de l'équation $(3)$ qui contient $\frac{di}{dt}$ et non pas $i(t)$. Il va donc falloir dériver l'équation $(2)$ pour pouvoir utiliser l'équation $(3)$ !

$(2) \Rightarrow \dfrac{di}{dt} = C \dfrac{d^2u_C}{dt^2}$ où $\dfrac{d^2u_C}{dt^2}$ représente la dérivée seconde de $u_C(t)$.

Et donc en remplaçant grâce à $(3) : \dfrac{di}{dt} = \dfrac{u_L(t)}{L}$

$\Leftrightarrow \dfrac{u_L(t)}{L} = C \dfrac{d^2u_C}{dt^2}$

Et enfin en remplaçant $u_L(t)$ grâce à $(1) : u_L(t) = - u_C(t)$,

$\Leftrightarrow \dfrac{- u_C(t)}{L} = C \dfrac{d^2u_C}{dt^2}$

On remet en forme et on obtient: 

$\Leftrightarrow \boxed{\dfrac{d^2u_C}{dt^2} + \dfrac{1}{LC} u_C(t) = 0}$

**Que peut-on dire de cette équation ?**

- Il s'agit d'une équation différentielle linéaire du **second ordre** à coefficients réels constants.
- On ne va pas pouvoir appliquer la même méthode de résolution que pour les équations différentielles du premier ordre, car notre théorème pour la solution homogène ne s'applique plus ! Pas de panique, on va en inventer un autre :)
- On dit que cette équation différentielle est caractéristique d'un oscillateur harmonique