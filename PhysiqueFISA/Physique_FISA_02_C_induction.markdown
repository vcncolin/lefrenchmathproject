---
layout: default
title:  "Physique FISA"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy3_02_C
---

# Induction

L'induction électromagnétique est un phénomène physique découvert au cours du XIXè siècle. Ce phénomène se traduit par l'apparition d'un courant électrique dans un circuit en interaction avec un champ magnétique (sous certaines conditions).

**Question :** dans quels dispositifs utilisés de manière quotidienne rencontre-t-on le phénomène d'induction ? 

On étudiera deux cas dans le cadre de ce cours : 

- un circuit en mouvement dans un champ magnétique uniforme et stationnaire : l'induction de **Lorentz**
- un circuit immobile dans un champ magnétique variable : l'induction de **Neumann**

**Remarque :** n'oubliez pas votre tire-bouchon !

## Lois basiques de l'induction

### Loi de Faraday

*Remarque pour les élèves de prépa : il s'agit de la traduction intégrale de l'équation de Maxwell-Faraday*

> Les variation de flux magnétique au travers d'un circuit fermé se modélisent par l'ajout d'un générateur dans le circuit. On dit alors que la **force électromotrice (f.e.m) induite** $e$ est reliée au flux magnétique $\Phi$ par :
>
> $$e = \dfrac{-d \Phi}{dt}\text{  avec  }\Phi = \int\int_{circuit} \vec{B}\vec{dS}$$

**Remarque :** la surface $\vec{dS}$ est orientée par règle de la main droite par rapport au sens conventionnel du courant

**Re-remarque :** la force électromotrice induite $e$ est alors orientée en convention générateur par rapport à $i$ (dans le même sens)

**Exemples :**

![image info](./img/Lorentz.jpeg)

Dans le cas de l'induction de Lorentz, on a un circuit en mouvement dans un champ magnétique $\vec{B}$ uniforme. Dans ce cas, $\vec{B}$ est constant, mais $S$ ne l'est pas.

On a alors : 

$e = \dfrac{-d \Phi}{dt}$

$= - B_0 \dfrac{dS}{dt}$

$= -B_0 \ell \dfrac{dx}{dt}$

où $\ell$ est la largeur du circuit considéré.

![image info](./img/Neumann.jpeg)

Dans le cas de l'induction de Neumann, le circuit est fixe, mais le champ est variable. Dans ce cas, $S$ est constant, mais $\vec{B}$ ne l'est pas.

On a alors : 

$e = \dfrac{-d \Phi}{dt}$

$= - S \dfrac{dB(t)}{dt}$

### Loi de Lenz

![image info](./img/Lenz_meme.jpeg)

Induction $\rightarrow$ modération

En d'autres termes, les phénomènes d'induction tendent à atténuer leur cause.

*C'est ce qu'on appelle une loi de modération*

Pour le phénomène d'induction, la cause est toujours la même : il s'agit d'une variation du flux magnétique $\Phi$.

- Si cette variation de flux est dûe à une variation du champ magnétique $\vec{B}$, alors le champ magnétique induit aura tendance à atténuer ces variations de flux. 
- Si cette variation de flux est dûe à un mouvement du circuit, alors la force de Laplace induite va avoir tendance à s'opposer au mouvement initial.