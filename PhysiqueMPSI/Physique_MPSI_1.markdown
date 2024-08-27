---
layout: default
title:  "Cours : Physique 1 MPSI"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy1
---

# Chapitre 1 : Outils mathématiques et physiques généraux

Il s'agit dans ce chapitre d'aborder quelques outils de base qui sont considérés comme des blocs élémentaires du calcul en physique. Un étudiant se doit donc à l'issue de ce chapitre de maîtriser les concepts suivants : 

- Analyse dimensionnelle d'une équation donnée
- Dérivation d'ordre quelconque d'une fonction de la variable réelle
- Dérivation d'une fonction de plusieurs variables
- Calcul d'incertitude statistique / propagée
## 1. Analyse dimensionnelle et unités

### A. Qu'est-ce qu'une grandeur physique ? 

![image info](./img/wiki_physique.png)

À partir de la définition précédente, on peut donc comprendre que la physique nécessite la mesure de certains paramètres, afin d'étudier, comme indiqué, leurs variations et leur évolution. Une grandeur physique peut alors être définie comme une propriété mesurable. L'action de mesurer permet de comparer par rapport à une référence, afin de mieux appréhender, et éventuellement comprendre.  

**Remarque :** Une grandeur peut être scalaire lorsqu'elle s'exprime par un simple nombre, ou vectorielle lorsqu'elle est exprimée par une direction, un sens, et un nombre. 

**Exemple :** Quelles sont les grandeurs physiques mesurables autour de nous à l'instant présent ? 

Il est important de distinguer la dimension et l'unité d'un grandeur physique. Par exemple, "$300 km$" a la dimension d'une longueur, et son unité est le $km$. Une même dimension peut être exprimée dans différentes unités (par exemple, on peut exprimer une vitesse en $km/h$, en $m/s$, en $mph$, en $kn$ ...)

Toute grandeur physique peut s'exprimer en fonction de sept dimensions fondamentales, qui forment par ailleurs le Système International des unités. 

### B. Unités du système international

Le système international des unités se compose d'un ensemble d'unités fondamentales, d'unités dérivées, et de préfixes multiplicateurs. 

- La **seconde** (s), unité fondamentale de temps, est définie comme la durée de 9 192 631 770 périodes de la radiation correspondant à la transition entre les deux niveaux hyperfins de l'état fondamental de l'atome de césium 133 à la température du zéro absolu. (Le césium c'est rigolo : https://youtu.be/uixxJtJPVXk?t=136)
- Le **mètre** (m), unité fondamentale de distance, définie comme la longueur du trajet parcouru dans le vide par la lumière pendant une durée de 1/299 792 458 de seconde.
- Le **kilogramme** (kg), unité fondamentale de masse, est défini grâce à la valeur numérique de la constante de Planck $h = 6,62607015.10^{-34} kg.m^2.s^{-1}$, en ayant au préalable défini le mètre et la seconde. 
- L'**ampère** (A), unité fondamentale d'intensité électrique, est défini en fixant la valeur numérique de la charge élémentaire $e=1,602176634.10^{-19} A.s$, en ayant défini au préalable la seconde.
- Le **kelvin** (K), unité fondamentale de température, est défini grâce à la valeur numérique de la constante de Boltzmann $k_B = 1,380649.10^{-23} kg.m^2.s^{-2}.K^{-1}$, en ayant au préalable défini le kilogramme, le mètre et la seconde. 
- La **mole** (mol), unité fondamentale de quantité de matière, correspond à un nombre d'entités élémentaires égal à $N_A = 6,02214076 .10^{23} $, appelé nombre d'Avogadro.
- La **candela** (cd) est définie en se basant sur l'efficacité lumineuse d'un rayonnement monochromatique de fréquence 540 THz, $K_{cd}=683 cd.sr.kg^{-1}m^{-2}s^3$en ayant au préalable défini le kilogramme, le mètre et la seconde.

| Grandeur  | Symbole | Unité | Constante associée |
| :---------------: |:----:| :-------:|:------------:|
| Temps |     $T$      | seconde ($s$) | Fréquence de transition $\Delta \nu _{Cs} = 9,193.10^9 s^{-1}$ |
| Longueur |     $L$      | mètre ($m$) | Vitesse de la lumière $c=3,00.10^8 m.s^{-1}$ |
| Masse |     $M$      | kilogramme ($kg$) | Constante de Planck $h = 6,626.10^{-34} kg.m^2.s^{-1}$ |
| Courant électrique |     $I$      | ampère ($A$) | Charge élémentaire $e = 1,602 . 10^{-19} A.s$ |
| Température |     $\Theta$      | kelvin ($K$) | Constante de Boltzmann $k_B=1,381 .10^{-23} kg.m^2.s^{-2}.K^{-1}$ |
| Quantité de matière |     $N$      | mole ($mol$) | $N_A=6,022.10^{23} mol^{-1}$ |
| Intensité lumineuse |     $J$      | candela ($cd$) | Efficacité lumineuse $K_{cd}=683 cd.sr.kg^{-1}m^{-2}s^3$ |

**Remarque :** le nom d'une unité est un nom commun et s'écrit sans majuscule dans tous les cas (i.e. un kelvin). Lorsque l'unité est basée sur un nom propre, son symbole prend une majuscule (i.e. "$1073 K$ c'est un peu chaud pour le jacuzzi Kévin"). L'exception est le litre (i.e. "$2L$ de bière le jeudi ne te t'aideront pas pour le DS du vendredi").

On rappelera que ces unités étaient initialement basées sur l'observation de phénomènes naturels (fraction du jour solaire, oscillation d'un pendule, ...)

On peut déduire de ces unités fondamentales toutes les unités dérivées du système international (liste complète : https://en.wikipedia.org/wiki/SI_derived_unit). Par exemple, la capacité thermique s'exprime habituellement en $J.K^{-1}$, qui s'exprime dans le système fondamental : $kg.m^2.s^{-2}.K^{-1}$

**Remarque :** Dans beaucoup de domaines, on aura tendance a utiliser des unités dérivées pour un côté pratique. (voir les illustrations)

![alt-text-1](./img/barometre.jpeg "Baromètre de Papi") ![alt-text-2](./img/biner.jpg "Mousqueton d'escalade")

![alt-text-1](./img/compteur.jpg "Fiat Panda de Mamie") ![alt-text-2](./img/compteur-edf.jpg "Compteur électrique")





## 2. Dérivation des fonctions de la variable réelle

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

**Exemple :** La fonction $
\begin{array}{rlll}
f: \mathbb{R} & \longrightarrow & \mathbb{R} \\
x & \longrightarrow & 3x^2+2
\end{array}
$ est-elle dérivable en $x = 1$ ?

Calculons : 

$\dfrac{f(1+h)-f(1)}{h} = \dfrac{3(1+h)^2 + 2 - (3*1^2 + 2)}{h} 

= \dfrac{ 3(1+2h+h^2)+2-(3+2)}{h} = \dfrac{ 3+6h+3h^2+2-3-2}{h} 

= \dfrac{6h + 3h^2}{h} = 6+3h \to_{h \to 0^{+}} 6$

**En pratique :** Il convient de savoir quelles sont les fonctions usuelles dérivables, et le cas échéant, quel est leur intervalle de dérivabilité, ainsi que la fonction dérivée associée ! (cf. méthodes, tableau de dérivation)

### B. Détermination de l'équation de la tangente à une courbe

Le nombre dérivé d'une fonction en un point correspond au coefficient directeur de la tangente à la courbe représentative de la fonction en ce point. 

En d'autres termes : soit la fonction $f$ que l'on va considérer dérivable sur $\mathbb{R}$ et admettant pour dérivée $f'$. Alors, en un point d'abcisse $a$ donnée, la tangente à la courbe $C_f$ représentative de la fonction $f$ a pour coefficient directeur $f'(a)$.

Plus précisément, la tangente a pour équation : $y = f'(a) * (x-a) + f(a)$

**Exemple** : Quelle est l'équation de la tangente à la fonction $f$ définie dans le paragraphe précédent, au point d'abcisse $x=1$ ?

On peut directement appliquer la formule ci-avant, afin de trouver : $y = 6(x-1) + 5 \iff y = 6x - 1$

![image info](./img/Phy1_01.png)

### C. Définition d'une dérivée seconde, dérivée $n$-ième

Si $f$ est dérivable deux fois, on appelle fonction dérivée seconde de $f$ la fonction dérivée de $f'$, que l'on notera $f''$.

On peut généraliser cette définition de la manière suivante : si $f$ est dérivable $n$ fois, on appelle fonction dérivée $n$-ième de $f$ la fonction dérivée de $f'$, que l'on notera $f^{(n)}$.

## 3. Fonctions de plusieurs variables

### A. Notation

Depuis tout petit, le lycéen considère les fonctions mathématiques comme des fonctions de la variable $x$, et prend l'habitude de noter $f'(x)$ le nombre dérivé de la fonction $f$ par rapport à la variable $x$. En revanche, le monde du physicien est autrement plus complexe. Nous sommes entourés de fonctions de plusieurs variables (on pourrait imaginer, par exemple, une modélisation de la température de la pièce en fonction de la température extérieure, du nombre d'individus présents, ...). Le physicien a donc pour habitude d'indiquer en permanence la variable par rapport à laquelle il dérive une fonction, en utilisant la notation suivante : $\dfrac{df}{dx}$ représente la dérivée de la fonction $f$ par rapport à la variable $x$.

### B. Dérivée partielle

Soit une fonction $(x,y) \longrightarrow f(x,y)$ à deux variables définie sur $\mathbb{R}^2$. La dérivée de la fonction $f$ par rapport à $x$ lorsque $y$ est constant est appelée dérivée partielle de $f$ par rapport à $x$ et se note : 

$\left(\dfrac{\partial f(x,y)}{\partial x}\right)_{y = cst} \hspace{4mm}$ ou simplement $\hspace{4mm} \dfrac{\partial f}{\partial x}$

De même, la dérivée partielle de $f$ par rapport à $y$ se note : 

$\left(\dfrac{\partial f(x,y)}{\partial y}\right)_{x = cst} \hspace{4mm}$ ou simplement $\hspace{4mm} \dfrac{\partial f}{\partial y}$

**Exemple :** $f(x,y) = 3x^2 + 2y^2$; $g(x,y) = 2xy^2$

- $\dfrac{\partial f}{\partial x} = 6x$; $\dfrac{\partial f}{\partial y} = 4y$
- $\dfrac{\partial g}{\partial x} = 2y^2$; $\dfrac{\partial g}{\partial y} = 4xy$

**Remarque :** On peut généraliser cette définition à une fonction d'un nombre quelconque de variables.



