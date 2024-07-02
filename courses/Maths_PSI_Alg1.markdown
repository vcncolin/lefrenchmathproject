---
layout: default
title:  "Cours : Algèbre 1 PSI"
date:   2024-07-01 12:19:36 +0200
categories: courses
exclude: true
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






