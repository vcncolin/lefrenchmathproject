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

On s'intéresse au circuit représenté ci-dessus. On considère qu'à $t<0$, le condensateur est chargé, et $u_C(t<0) = U_0$. 

À $t=0$, on ferme l'interrupteur. On s'intéresse à la tension $u_C(t)$ pour $t>0$.

### A. Étude qualitative

On peut se demander comment va évoluer la tension du condensateur. En effet, dans un premier temps, lorsqu'on ferme l'interrupteur, le condensateur va avoir tendance à se décharger. Cependant, la bobine va s'opposer à l'établissement du courant, qui va donc augmenter de manière progressive et non brutale. 

Lorsque la tension du condensateur devient nulle, le mouvement de charges devrait alors s'interrompre. Nous savons cependant que l'intensité électrique est continue dans une bobine : la bobine continue à alimenter le mouvement des charges, et va donc forcer la charge du condensateur dans le sens opposé. 

Intuitivement, on devrait donc voir apparaître une oscillation de la tension du condensateur entre une valeur positive et une valeur négative. 

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
- On remarque que les fonctions qui vérifient cette équation sont les fonctions trigonométriques !
- On appelle ce genre de système **un oscillateur harmonique**.

## 2. L'oscillateur harmonique

> Un oscillateur harmonique est un oscillateur idéal dont l'évolution au cours du temps est décrite par une fonction sinusoïdale, dont la fréquence ne dépend que des caractéristiques du système et dont l'amplitude est constante. (*Wikipédia*)

Il faut comprendre dans le mot idéal, un oscillateur sans frottements. 