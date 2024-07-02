---
layout: default
title:  "Cours : Algèbre 1 PSI"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Alg1
---

# 1. Compléments

## A. Espaces vectoriels

**Définition** : $(E, +, .)$ est un $\mathbb{K}$ espace vectoriel  si :

- $(E,+)$ est un groupe abélien
- $\forall (\lambda, \mu) \in \mathbb{K}^2, \forall x \in E, \lambda.(\mu.x) = (\lambda \times \mu).x$ et $(\lambda + \mu). x = \lambda.x + \mu.x$
- $\forall \lambda \in \mathbb{K}, \forall (x,y) \in E^2, \lambda.(x+y) = \lambda.x + \lambda.y$
- $\forall x \in E, 1_\mathbb{K}.x = x$

**Remarque** : Il est généralement plus simple de prouver qu'un ensemble $F$ est un sous-espace vectoriel d'un autre espace $E$ plutôt que de vérifier toutes les conditions de la définition précédente.

**Quelques espaces vectoriels usuels** : 

- $(\mathbb{K}, +, .)$
- $(\mathbb{K}^n, +, .)$
- $M_{m,n}(\mathbb{K})$, l'ensemble des matrices à $m$ lignes et $n$ colonnes à coefficients dans $\mathbb{K}$
- $\mathbb{K}[X]$ l'ensemble des polynômes à coefficients dans $\mathbb{K}$
- $\mathbb{K}^\mathbb{N}$ l'ensemble des suites d'éléments de $\mathbb{K}$
- $\mathcal{L}(E,F)$ l'ensemble des applications linéaires de $E$ dans $F$

## B. Applications linéaires

**Définition** : Soit $f : E \longrightarrow F$. On dit que $f$ est linéaire lorsque : 

- $\forall (u, v) \in E^2, \forall \lambda \in \mathbb{K}, f(\lambda.u, v) = \lambda f(u) + f(v)$

**Terminologie** : 

- On note $\mathcal{L}(E, F)$ l'ensemble des applications linéaires de $E$ dans $F$
- Si $E$ = $F$ on note $\mathcal{L}(E, E) = \mathcal{L}(E)$. Les éléments de $\mathcal{L}(E)$ sont des endomorphismes.
- Un isomorphisme est une application linéaire bijective
- Un automorphisme est un endomorphisme bijectif

**Propriétés** :

1. *Restriction* : Si $f \in \mathcal{L}$, si $G$ est un SEV de $E$, et si $H$ est un SEV de $F$ tel que $f(G) \subset H$, alors $f_{/G} \in \mathcal{L}(G,H)$
2. *Somme et multiplication* : Si $(f,g) \in \mathcal{L}(E,F)$ et $\lambda \in \mathbb{K}$, alors $\lambda.f + g \in \mathcal{L}(E,F)$
3. *Composition* : Si $f \in \mathcal{L}(E,F)$ et $g \in \mathcal{L}(F,G)$, alors $g \circ f \in \mathcal{L}(E,G)$
4. *Bijection réciproque* : Si f est un isomorphisme de $E$ sur $F$, alors $f^{-1}$ est un isomorphisme de $F$ dans $E$

**Définition** : Noyau et image

Soit $f \in \mathcal{L}(E,F)$
1. On appelle noyau de $f$ : 
$$
Ker(f) = f^{-1} (\{0\}) = \{x \in E / f(x) = 0\}
$$
2. On appelle image de $f$ :
$$
Im(f) = f(E) = \{f(x) \in F / x \in E \}
$$

$Ker(f)$ et $Im(f)$ sont des SEV de respectivement $E$ et $F$

**Remarque** : 

Soit $f \in \mathcal{L}(E,F)$
1. $f$ est injective $\iff Ker(f) = \{0\}$
2. $f$ est surjective $\iff Im(f) = F$

**Terminologie** : 

Soit $f \in \mathcal{L}(E)$ un endomorphisme

1. $f$ est un projecteur $\iff f^2 = f$
2. $f$ est une symétrie $\iff f^2 = Id_{/E}$

## C. Familles de vecteurs

**Définitions** :

On considère $(x_1, x_2, ... x_p) = (x_i)_{i\in I}$ une famille de $p$ vecteurs de l'EV $E$
1. La famille de vecteurs est libre si $\sum\limits_{i=1}^p \lambda_i x_i = 0 \implies \forall i \in I, \lambda_i = 0$ 
2. La famille de vecteurs est génératrice si $\forall x \in E, \exists (\lambda_i)_{i\in I} / x = \sum\limits_{i=1}^p \lambda_i x_i$
3. La famille de vecteurs est une base si elle est libre et génératrice, ou encore si $\forall x \in E, \exists !(\lambda_i)_{i\in I} / x = \sum\limits_{i=1}^p \lambda_i x_i$

**Remarque** : 

Si $E$ est un EV de dim $n$, et $(x_i)$ une famille de vecteurs de $E$, alors il y a équivalence entre les trois propositions suivantes : 
1. $(x_i)$ est une base de $E$
2. $(x_i)$ est une famille libre à $n$ éléments
3. $(x_i)$ est une famille génératrice à $n$ éléments

**Définition** : 

Soient $E$ et $F$ deux EV, et $u \in \mathcal{L}(E,F)$. On suppose que $E$ est de dimension finie. On appele rang de $u$ : 
$$
rg(u) = dim(Im(u))
$$

**Théorème** :
Soient $E$ et $F$ deux EV, et $u \in \mathcal{L}(E,F)$. On suppose que $E$ est de dimension finie. On a alors la formule du rang : 

$$
dim(E) = dim(Ker(u)) + rg(u)
$$

**Remarque** :
Que peut-on en déduire si $dim(E) = dim(F)$ ? (donc pour tout endomorphisme en dimension finie)

## D. Produit et somme d'espaces vectoriels


**Définition**:
On considère $n \hspace{2mm} \mathbb{K}$-EV $E_1, ... E_n$
Le produit cartésien $E_1 \times E_2 \times ... \times E_n$ est défini comme l'ensemble des $(x_1, x_2, ..., x_n)$ tels que $x_i \in E_i$

$E_1 \times E_2 \times ... \times E_n$ a une structure de $\mathbb{K}$-EV et $dim(E_1 \times E_2 \times ... \times E_n) = \sum\limits_{i=1}^n dim(E_i)$

**Définition** : 
On considère deux SEV $F$ et $G$ d'un même EV $E$. On note alors : 
$$
F+G = \{x+y / x\in F, y \in G\} = \{z \in E / \exists (x,y) \in F \times G, z = x+y\} 
$$

La somme $F+G$ est un SEV de E.

**Définition** :
On dit que deux SEV $F$ et $G$ sont en somme directe lorsque $F \cap G = \{0\}$, dans ce cas on note $F+G = F\oplus G$

**Définition** :
On dit que deux SEV $F$ et $G$ sont supplémentaires dans $E$ lorsque 
1. $F \cap G = \{0\}$
2. $F+G = E$ (tout vecteur de $E$ peut s'exprimer comme une somme d'un vecteur de $F$ et d'un vecteur de $G$)

**Théorème** : 
Soient $E$ un $\mathbb{K}$-EV et $F$ et $G$ deux SEV de $E$ de $dim$ finie. 
1. $F+G$ est un SEV de $E$ de $dim$ finie et $dim(F+G) \leq dim(F) + dim(G)$
2. De plus si $F$ et $G$ sont en somme directe alors $dim(F\oplus G) = dim(F) + dim(G)$