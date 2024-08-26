---
layout: default
title:  "Cours : Physique 1 MPSI"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy1
---

# Chapitre 1 : Outils mathématiques et physiques généraux

Il s'agit dans ce chapitre d'aborder quelques outils de base qui sont considérés comme des blocs élémentaires du calcul en physique. Un étudiant se doit donc à l'issue de ce chapitre de maîtriser les concepts suivants : 

- Dérivation d'ordre quelconque d'une fonction de la variable réelle
- Dérivation d'une fonction de plusieurs variables
- Analyse dimensionnelle d'une équation donnée
- Calcul d'incertitude statistique / propagée

## 1. Dérivation

### A. Fonction d'une seule variable

Soit $f$ une fonction définie sur $\mathbb{R}$ et $x_0 \in \mathbb{R}$ :

- $f$ est dite dérivable à droite en $x_0$ si : 
$ \lim\limits_{h \to 0^{+}} \dfrac{f(x_0+h)-f(x_0)}{h}$ est un nombre fini.

- $f$ est dite dérivable à gauche en $x_0$ si : 
$ \lim\limits_{h \to 0^{+}} \dfrac{f(x_0-h)-f(x_0)}{-h}$ est un nombre fini.

- $f$ est dite dérivable en $x_0$ si et seulement si elle est dérivable à droite et à gauche en $x_0$ et :

$$ \lim\limits_{h \to 0^{+}} \dfrac{f(x_0+h)-f(x_0)}{h} = \lim\limits_{h \to 0^{+}} \dfrac{f(x_0-h)-f(x_0)}{-h} = \lim\limits_{h \to 0^{+}} \dfrac{f(x_0+h)-f(x_0-h)}{2h}$$

