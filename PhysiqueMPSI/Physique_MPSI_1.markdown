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

On appelle ces limites "dérivée de f en $x_0$" et elle se note $f'(x_0)$. 

La fonction dérivée d'une fonction $f$ se note $f'$ et est définie pour tout point $x$ où $f$ est dérivable. 

\textbf{Exemple :} La fonction $$
\begin{array}{rlll}
D: \mathbb{R} & \longrightarrow & \mathbb{R} \\
x & \longrightarrow & 3x^2+2
\end{array}
$$ est-elle dérivable en $x = 1$ ?

Calculons : 

$$ \dfrac{f(1+h)-f(1)}{h} = \dfrac{3(1+h)^2 + 2 - (3*1^2 + 2)}{h} = \dfrac{ 3(1+2h+h^2)+2-(3+2)}{h} = \dfrac{ 3+6h+3h^2+2-3-2}{h} = \dfrac{6h + 3h^2}{h} = 6+3h \to_{h \to 0^{+}} 6 $$

\textbf{En pratique :} Il convient de savoir quelles sont les fonctions usuelles dérivables, et le cas échéant, quel est leur intervalle de dérivabilité, ainsi que la fonction dérivée associée ! (cf. méthodes, tableau de dérivation)

