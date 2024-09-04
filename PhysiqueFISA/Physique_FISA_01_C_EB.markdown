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

![image info](./img/Div_conv_E.png)