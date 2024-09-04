---
layout: default
title:  "Physique FISA"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy3_01_C
---

# Chapitre 0 : Outils mathématiques

## Coordonnées cartésiennes, polaires, et sphériques

Il est d'usage en physique d'utiliser un système de coordonnées approprié au problème que l'on va traiter. 

### Coordonnées cartésiennes
De manière générale, on utilise le système des coordonnées cartésiennes, où un point est repéré par ses côtes le long des axes $Ox,Oy,Oz$

### Coordonnées polaires

![image info](./img/Coordonnees_polaires.png)

Dans un plan, on peut également considérer les coordonnées polaires : au lieu de considérer l'abcisse $x$ et l'ordonnée $y$ d'un point, on va plutôt le repérer via sa distance à l'origine $r$ et l'angle formé avec l'axe des abcisses $\theta$.

On a :
$r = \sqrt{x^2+y^2}$ et $\theta = \arctan (\frac{y}{x}) \pm \pi$

Et à l'inverse : 
$x = r \cos (\theta)$ et $y = r \sin (\theta)$

### Coordonnées cylindriques

![image info](./img/Coordonnees_cylindriques.png)

On peut généraliser le concept des coordonnées cylindriques dans un espace à 3 dimensions, en ajoutant la hauteur $z$ du point considéré. Les calculs restent les mêmes. 

### Coordonnées sphériques

![image info](./img/Coordonnees_spheriques.png)

Il s'agit maintenant de repérer un point dans un espace à 3 dimensions, armé de deux angles et une distance (penser latitude/longitude).

On a maintenant : 
$\rho = \sqrt{x^2+y^2+z^2}$, $\varphi = \arctan(\frac{y}{x})$, et $\theta = \arccos(\frac{z}{\rho})$

Et à l'inverse : 
$x = \rho \sin(\theta)\cos(\varphi)$, $y = \rho \sin(\theta)\sin(\varphi)$, et $z = \rho \cos(\theta)$  


# Chapitre 1 : Champ électrique et magnétique 

## Qu'est-ce que la charge électrique ? 

![image info](./img/wiki_charge.png)

Quand on parle de gravité / d'interaction gravitationnelle, on sait que tout corps massique est à la fois une source de champ gravitationnel (i.e. il peut attirer tout autre corps massique) mais peut également interagir avec tout champ gravitationnel (i.e. il peut être attiré par tout autre corps massique). 

Les particules chargées électriquement agissent de la même manière, à la différence près qu'elles peuvent être chargées négativement. 

On appelle charge élémentaire la valeur $e = 1.6\times 10^{-19} C$, qui correspond à la valeur absolue de la charge d'un électron. 

## Champ électrique : sources et interactions

![image info](./img/Div_conv_E.png)

Le champ électrique est créé par les charges électriques. Il diverge à partir des charges positives et converge vers les charges négatives. Il n'a pas de caractère tourbillonant autour de celles-ci.

Le champ électrostatique créé par une particule de charge $q$ et à la distance $r$ de celle-ci s'exprime : 

$$\vec{E} = \dfrac{q}{4\pi\varepsilon_0 r^2}\vec{u}$$ 

$\varepsilon_0$ est une constante nommée **permittivité du vide**, $\varepsilon_0 = 8.85\times 10^{-12}F.m^{-1}$ 

**Remarque :** il sera de bon ton de se demander comment le vecteur $\vec{u}$ est orienté en se référant à la remarque précédente. 

**Remarque :** le champ électrique prend donc une valeur différente en tout point de l'espace. On peut observer que la dépendance en $1/r^2$ signifie que plus on s'éloigne d'une particule, moins l'intensité du champ généré par celle-ci est élevé.

De plus, l'interaction de toute charge avec un champ électrique s'exprime par le biais de la force :

$$\vec{F}_e = q\vec{E}$$

Lorsque l'intensité de ce champ électrique est constante dans le temps, on parlera de champ **électrostatique**.

## Champ magnétique : sources et interactions

Le champ magnétique, quant à lui, est créé par les *mouvements* de charges électriques (en d'autres termes : du 'courant électrique'). Il est donc plus difficile d'obtenir des équations simples permettant de le caractériser, puisqu'il faut caractériser le mouvement des charges !

Afin de simplifier l'étude ici, nous allons considérer quelques cas particuliers (et qui se retrouvent assez souvent dans notre quotidien) de génération de champ magnétique par des géométries particulières.

À la différence du champ électrique, nous allons voir que le champ magnétique présente un caractère tourbillonnant autour des mouvements de charges électriques (on parle d'un *champ rotationnel*)

**Remarque :** quelques visualisations intéressantes peuvent être trouvées ici : <https://www.youtube.com/watch?v=rB83DpBJQsE>

### Théorème d'Ampère

Le théorème d'Ampère va nous permettre de calculer le champ magnétique le long d'un contour fermé (cf ci-après) : 

$$\oint \vec{B}\vec{d\ell} = \mu_0 I_{enl}$$

Quelques explications sur les différents termes : 
- $\oint$ représente une intégrale sur un contour fermé (par exemple, un cercle est un contour fermé, un segment ne l'est pas)
- En fonction de l'orientation de ce contour (donc du sens dans lequel on intègre), la surface attenante sera elle aussi orientée dans une direction. 
- $\vec{B}$ est le champ magnétique
- $\mu_0$ est une constante, nommée perméabilité du vide, $\mu_0 = 4\pi\times 10^{-7}H.m^{-1}$
- $I_enl$ correspond à l'intensité électrique 'enlacée par le contour' (cf figure ci-dessous).  

L’orientation de la surface peut se faire à l’aide de la règle du tire-bouchon : en tournant le tire-bouchon dans le sens de parcours du contour, le sens de déplacement du manche du tire-bouchon indique l’orientation de $\vec{S}$

![image info](./img/orientation.png)

L'intensité électrique enlacée se calcule ensuite en additionnant **algébriquement** les intensités traversant la surface orientée : dans la figure suivante, $I_enl = i_1 -i_3 +i_3 -i_2$

![image info](./img/Max_Amp.png)



### Champ magnétique généré par un fil rectiligne



### Champ magnétique généré par une spire


### Champ magnétique dans un solénoïde