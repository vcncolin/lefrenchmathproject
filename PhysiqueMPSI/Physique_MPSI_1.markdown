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

## 1. Dérivation des fonctions de la variable réelle

### A. Définition

Soit $f$ une fonction définie sur $\mathbb{R}$ et $x_0 \in \mathbb{R}$ :

- $f$ est dite dérivable à droite en $x_0$ si : 
$ \lim\limits_{h \to 0^{+}} \dfrac{f(x_0+h)-f(x_0)}{h}$ est un nombre fini.

- $f$ est dite dérivable à gauche en $x_0$ si : 
$ \lim\limits_{h \to 0^{+}} \dfrac{f(x_0-h)-f(x_0)}{-h}$ est un nombre fini.

- $f$ est dite dérivable en $x_0$ si et seulement si elle est dérivable à droite et à gauche en $x_0$ et :

$$ \lim\limits_{h \to 0^{+}} \dfrac{f(x_0+h)-f(x_0)}{h} = \lim\limits_{h \to 0^{+}} \dfrac{f(x_0-h)-f(x_0)}{-h} = \lim\limits_{h \to 0^{+}} \dfrac{f(x_0+h)-f(x_0-h)}{2h}$$

On appelle ces limites "dérivée de f en $x_0$" et elle se note $f'(x_0)$. 

La fonction dérivée d'une fonction $f$ se note $f'$ et est définie pour tout point $x$ où $f$ est dérivable. 

**Exemple :** La fonction $$
\begin{array}{rlll}
f: \mathbb{R} & \longrightarrow & \mathbb{R} \\
x & \longrightarrow & 3x^2+2
\end{array}
$$ est-elle dérivable en $x = 1$ ?

Calculons : 

$$ \dfrac{f(1+h)-f(1)}{h} = \dfrac{3(1+h)^2 + 2 - (3*1^2 + 2)}{h} 

= \dfrac{ 3(1+2h+h^2)+2-(3+2)}{h} = \dfrac{ 3+6h+3h^2+2-3-2}{h} 

= \dfrac{6h + 3h^2}{h} = 6+3h \to_{h \to 0^{+}} 6 $$

**En pratique :** Il convient de savoir quelles sont les fonctions usuelles dérivables, et le cas échéant, quel est leur intervalle de dérivabilité, ainsi que la fonction dérivée associée ! (cf. méthodes, tableau de dérivation)

### B. Détermination de l'équation de la tangente à une courbe

Le nombre dérivé d'une fonction en un point correspond au coefficient directeur de la tangente à la courbe représentative de la fonction en ce point. 

En d'autres termes : soit la fonction $f$ que l'on va considérer dérivable sur $\mathbb{R}$ et admettant pour dérivée $f'$. Alors, en un point d'abcisse $a$ donnée, la tangente à la courbe $C_f$ représentative de la fonction $f$ a pour coefficient directeur $f'(a)$.

Plus précisément, la tangente a pour équation : $y = f'(a) * (x-a) + f(a)$

**Exemple** : Quelle est l'équation de la tangente à la fonction $f$ définie dans le paragraphe précédent, au point d'abcisse $x=1$ ?

On peut directement appliquer la formule ci-avant, afin de trouver : $y = 6(x-1) + 5 \eq y = 6x - 1$

![image info](./img/Phy1_01.png)

### C. Définition d'une dérivée seconde, dérivée $n$-ième

Si $f$ est dérivable deux fois, on appelle fonction dérivée seconde de $f$ la fonction dérivée de $f'$, que l'on notera $f''$.

On peut généraliser cette définition de la manière suivante : si $f$ est dérivable $n$ fois, on appelle fonction dérivée $n$-ième de $f$ la fonction dérivée de $f'$, que l'on notera $f^{(n)}$.

## 2. Fonctions de plusieurs variables

Depuis tout petit, le lycéen considère les fonctions mathématiques comme des fonctions de la variable $x$, et prend l'habitude de noter $f'(x)$ le nombre dérivé de la fonction $f$ par rapport à la variable $x$. En revanche, le monde du physicien est autrement plus complexe. Nous sommes entourés de fonctions de plusieurs variables (on pourrait imaginer, par exemple, une modélisation de la température de la pièce en fonction de la température extérieure, du nombre d'individus présents, ...). Le physicien a donc pour habitude d'indiquer en permanence la variable par rapport à laquelle il dérive une fonction, en utilisant la notation suivante : $\dfrac{df}{dx}$ représente la dérivée de la fonction $f$ par rapport à la variable $x$.

