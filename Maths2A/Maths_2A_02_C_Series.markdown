---
layout: default
title:  "Maths A2 - Chapitre 2 - Séries Numériques"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Mat2_02_C
---

# Introduction

$1 + 1 + 1 + 1 + 1 + ...  = \sum\limits_{n=0}^{+\infty} 1 = +\infty$

$1 + \dfrac{1}{2} + \dfrac{1}{4} + \dfrac{1}{8} + ...  = \sum\limits_{n=0}^{+\infty} \left(\dfrac{1}{2}\right)^n = \lim_{N \to +\infty} \sum\limits_{n=0}^{N} \left(\dfrac{1}{2}\right)^n = \lim_{N \to +\infty} \dfrac{1 - \left(\dfrac{1}{2}\right)^{N+1}}{1 - \dfrac{1}{2}} = 2$

$1 + \dfrac{1}{2} + \dfrac{1}{3} + \dfrac{1}{4} + ...  = \sum\limits_{n=0}^{+\infty} \dfrac{1}{n}= ?$

$1 + \dfrac{1}{2^2} + \dfrac{1}{3^2} + \dfrac{1}{4^2} + ...  = \sum\limits_{n=0}^{+\infty} \dfrac{1}{n^2}= ?$ 

$1 - 1 + 1 - 1 + 1 - 1 ... = 0 \hspace{2mm} \text{ou} \hspace{2mm} 1 ?$

# Notion de convergence et de divergence

**Définition :** 

Soit $(u_n)$ une suite de nombres réels ou complexes.

On appelle *somme partielle de rang $N$* de la série $\sum_{n\geq 0} u_n$ la quantité : 

 $$ S_N = u_0 + u_1 + u_2 + ... + u_N = \sum_{n=0}^N u_n $$

 $u_n$ est appelé le *terme général* de la série $\sum_{n\geq 0} u_n$.
 
 **Définition :**
 
 Soit $(u_n)$ une suite de nombres réels ou complexes.
 
 On dit que $\sum_{n\geq 0} u_n$, la série de terme général $u_n$ est *convergente* si la suite $S_N$ des sommes partielles est convergente. 

 $$\sum_{n=0}^{+\infty} u_n = \lim_{N \to +\infty} \sum_{n=0}^{N} u_n$$

 Dans le cas contraire, on dit que la série $\sum_{n\geq 0} u_n$ est *divergente*.
 
 **Exemple :** Série arithmétique
 
 $$
S_N=\sum_{n=0}^N n=0+1+2+\ldots+N=\frac{N(N+1)}{2} \underset{N \rightarrow+\infty}{\longrightarrow}+\infty .
$$
La série arithmétique $\sum n$ diverge et on peut écrire $\sum\limits_{n=0}^{+\infty} n=+\infty$.

**Exemple :** Série géométrique

$$
S_N=\sum_{n=0}^N q^n=1+q+q^2+\ldots+q^N= \begin{cases}\frac{1-q^{N+1}}{1-q} & \text { si } q \neq 1 \\ N+1 & \text { sinon. }\end{cases}
$$


**Exemple :** Série harmonique

$$
S_N=\sum_{n=1}^N \frac{1}{n}=1+\frac{1}{2}+\frac{1}{3}+\ldots+\frac{1}{N} .
$$
La fonction $x\mapsto\frac{1}{x}$ étant décroissante sur $[1; +\infty[$, on peut effectuer la comparaison avec une intervalle (faire un graphique pour mieux le représenter !)
$$
\text { pour tout } n \geq 1, \quad \frac{1}{n} \geq \int_n^{n+1} \frac{\mathrm{d} t}{t} \text {. }
$$

En effectuant la somme des $N$ premiers termes, on a :
$$
S_N=\sum_{n=1}^N \frac{1}{n} \geq \sum_{n=1}^N \int_n^{n+1} \frac{\mathrm{d} t}{t}=\int_1^2 \frac{\mathrm{d} t}{t}+\int_2^3 \frac{\mathrm{d} t}{t}+\ldots+\int_n^{N+1} \frac{\mathrm{d} t}{t}=\int_1^{N+1} \frac{\mathrm{d} t}{t}=\ln (N+1) \underset{N \rightarrow+\infty}{\longrightarrow}+\infty .
$$
La série harmonique $\sum\limits_{n \geq 1} \frac{1}{n}$ diverge.

**Exemple :** Une série télescopique

$$
S_N=\sum_{n=2}^N \frac{1}{n(n-1)}=\frac{1}{2}+\frac{1}{6}+\frac{1}{12}+\frac{1}{20}+\ldots+\frac{1}{N(N-1)}
$$
Mais le terme général $\frac{1}{n(n-1)}$ peut s'écrire aussi sous la forme $\frac{1}{n(n-1)}=\frac{1}{n-1}-\frac{1}{n}$ et ainsi :
$$
S_N=\sum_{n=2}^N\left(\frac{1}{n-1}-\frac{1}{n}\right)=\underbrace{1-\frac{1}{2}}_{\text {pour } n=2}+\underbrace{\frac{1}{2}-\frac{1}{3}}_{\text {pour } n=3}+\underbrace{\frac{1}{3}-\frac{1}{4}}_{\text {pour } n=4}+\ldots+\underbrace{\frac{1}{N-1}-\frac{1}{N}}_{\text {pour } n=N}=1-\frac{1}{N} \underset{N \rightarrow+\infty}{\longrightarrow} 1 .
$$
La série télescopique $\sum\limits_{n \geq 2} \frac{1}{n(n-1)}$ converge vers 1 . On peut même écrire $\sum\limits_{n=2}^{+\infty} \frac{1}{n(n-1)}=1$

# Propriétés, et critères de convergence

**Condition nécessaire, mais pas suffisante de convergence :**

Si la série $\sum u_n$ converge alors $u_n$ tend vers 0 .
Si $u_n$ ne tend pas vers 0 , on dit que la série de terme général $u_n$ *diverge grossièrement*.

- La série arithmétique $\sum n$ diverge grossièrement.
- Par contre la série harmonique $\sum \frac{1}{n}$ diverge bien que son terme général, $\frac{1}{n}$ tende vers 0 . Cette condition est bien nécessaire, mais pas suffisante.

## Séries à termes positifs 

**Définition :** 

Une série réelle $\sum u_n$ est dite *à termes positifs* lorsque $u_n\geq 0$ pour tout $n\in \mathbb{N}$.

**Convergence par domination :**

Soient $\sum u_n$ et $\sum v_n$ deux séries à termes positifs vérifiant $0\leq u_n \leq v_n$ pour tout $n\in \mathbb{N}$.
- si $\sum v_n$ converge alors $\sum u_n$ converge aussi.
- si $\sum u_n$ diverge alors $\sum v_n$ diverge aussi.

**Exemple :**

$\dfrac{1}{n^2} \leq \dfrac{1}{n(n-1)}$ pour tout $n \geq 2$, or $\sum\limits_{n \geq 2}\dfrac{1}{n(n-1)}$ converge (c'est notre exemple de série télescopique), donc la série $\sum\limits_{n\geq 2} \dfrac{1}{n^2}$ converge. 

On peut rajouter le terme en $n=1$, la série restera convergente : $\sum\limits_{n \geq 1}\dfrac{1}{n^2}$ converge.

**Rappel sur l'équivalence de suites :**

Deux suites $(u_n)$ et $(v_n)$ sont *équivalentes* et on note $u_n \sim v_n$ si $u_n-v_n$ est négligeable devant $v_n$. (c'est-à-dire si $u_n - v_n = \epsilon_n v_n$ avec $\epsilon_n \rightarrow 0$)

Le plus souvent on utilise cette propriété : 

Si $v_n$ ne s'annule pas : $u_n \sim v_n \Longleftrightarrow \lim_{n \to +\infty} \dfrac{u_n}{v_n} = 1$

**Séries équivalentes :**

Soient $\sum u_n$ et $\sum v_n$ deux séries à termes positifs. 

Si $u_n \sim v_n$ alors $\sum u_n$ et $\sum v_n$ sont de même nature. (i.e. DV ou CV)

**Exemples :**

- $\dfrac{1}{n^2+n} \sim \dfrac{1}{n^2}$ car $\dfrac{1}{n^2+n} \div \dfrac{1}{n^2} = \dfrac{n^2}{n^2+n} \xrightarrow[n \to +\infty]{} 1$ et ce sont des termes positifs.
Comme $\sum\limits_{n \geq 1} \dfrac{1}{n^2}$ converge alors $\sum\limits_{n \geq 1} \dfrac{1}{n^2+n}$ converge aussi.
- $\dfrac{1}{n+\sqrt{n}} \sim \dfrac{1}{n}$ car $\dfrac{1}{n + \sqrt{n}} \div \dfrac{1}{n} = \dfrac{n}{n+\sqrt{n}} \xrightarrow[n \to +\infty]{} 1$ et ce sont des termes positifs.
Comme $\sum\limits_{n \geq 1} \dfrac{1}{n}$ converge alors $\sum\limits_{n \geq 1} \dfrac{1}{n+\sqrt{n}}$ converge aussi.

### Séries de référence

**Série de Riemann :** (Rien à voir avec Riz-man)

La série à termes positifs $\sum\limits_{n \geq 1} \dfrac{1}{n^{\alpha}}$ converge si et seulement si $\alpha > 1$.

**Série géométrique :** 

$$
S_N=\sum_{n=0}^N q^n=1+q+q^2+\ldots+q^N= \begin{cases}\frac{1-q^{N+1}}{1-q} & \text { si } q \neq 1 \\ N+1 & \text { sinon. }\end{cases}
$$

Dans le cas $q \neq 1$, la limite de $S_N$ ne dépend que la limite de $q^{N+1}$ pour $N \rightarrow+\infty$. On peut alors conclure :

- Si $-1<q<1$ la série $\sum q^n$ converge vers $\frac{1}{1-q}$ et on peut écrire $\sum\limits_{n=0}^{+\infty} q^n=\frac{1}{1-q}$.
- Si $q \geq 1$ la série $\sum q^n$ diverge : $\sum\limits_{n=0}^{+\infty} q^n=+\infty$.
- Si $q \leq-1$ la série $\sum q^n$ diverge (il n'y a même pas de limite).

**Remarque :** Lorsqu'on voudra étudier la nature d'une série, on cherchera le plus souvent soit une comparaison, soit un équivalent à une série de référence. Pour tout le reste, il faudra utiliser d'autres critères. 

### When all else fails 

**Critère de d'Alembert :**

Soit la série $\sum u_n$ à termes positifs non nuls. 

On suppose que $\lim\limits_{n \to + \infty} \dfrac{u_{n+1}}{u_n} = L$ ($L$ étant éventuellement $+\infty$).

- Si $L>1$ alors $\sum u_n$ diverge \textbf{grossièrement}.
- Si $L<1$ alors $\sum u_n$ converge.
- Si $L=1$, cas litigieux, alors on ne peut pas conclure avec cette règle. 
        
(Toutefois, si $L=1^+$, alors la série est divergente.) 

*Remarque* :  C'est un critère très pratique lorsque le terme général s'exprime sous la forme de produit de facteurs dépendant de $n$, ou de puissances de $n$.

**Critère de Cauchy :** *(hors programme ?)*

Soit la série $\sum u_n$ à termes positifs.

On suppose que $\lim\limits_{n \to +\infty} (u_n)^{1/n} = L$ ($L$ étant éventuellement $+\infty$).
- Si $L>1$, alors $\sum u_n$ diverge grossièrement
- Si $L<1$, alors $\sum u_n$ converge
- Si $L=1$, cas litigieux, on fait appel à la VAR car on ne peut pas conclure avec cette règle. 

*Remarque* : C'est un critère très pratique lorsque le terme général est à la puissance $n$.

## Séries à termes de signe non constant

### Convergence absolue

**Définition :**
Une série $\sum u_n$ est dite \*absolument convergente* si et seulement si $\sum |u_n|$ est une série convergente. 


**Propriété :**
    Si la série $\sum u_n$ est absolument convergente alors la série est convergente et de plus on a : 
$$\left| \sum_{n=0}^{+\infty} u_n \right| \leq \sum_{n=0}^{+\infty} |u_n|$$

### Séries alternées

**Définition :**
Une série réelle $\sum u_n$ est dite \highl{alternée} si $u_{n+1}$ et $u_n$ sont de signe contraire.  


**Théorème :** Critère de Leibniz

Soit $\sum u_n$ une série à termes de signe non constant.
- Si $\sum u_n$ est une série alternée;
- Si $(\left|u_n\right|)$ est décroissante;
- Si $\lim\limits_{n \to +\infty} u_n = 0$

alors la série $\sum u_n$ est convergente. 

On a, de plus, une approximation de la somme partielle $\sum\limits_{n=0}^{N}u_n$ :
    
$$\left| \sum\limits_{n=0}^{+\infty}u_n - \sum\limits_{n=0}^{N}u_n \right| \leq |u_{N+1}|$$

**Définition :**

Toute série convergente sans être absolument convergente est dite *semi-convergente*.