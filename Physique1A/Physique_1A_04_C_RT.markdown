---
layout: default
title:  "Physique A1 - Chapitre 4 - Régime transitoire - Bases"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy1_04_C
---

# Chapitre 4 : Régimes transitoires dans les circuits linéaires du premier ordre

## 1. Notions de base

### A. Régime permanent

"En physique, un régime permanent est le régime d'un système stable qui peut être observé après un certain temps, lorsque le régime transitoire est terminé."

(Wikipédia)

### B. Régime stationnaire

Le régime stationnaire est un cas particulier du régime permanent, où les tensions et les intensités sont indépendants du temps. 

(On verra un autre cas particulier de régime permanent, le régime permanent sinusoïdal)


### C. Régime transitoire

"En physique, un régime transitoire est le régime d'évolution d'un système qui n'a pas encore atteint un état stable (**un régime permanent**)."

(Wikipédia)

En électronique, on peut rencontrer ce genre de régime transitoire typiquement à l'ouverture / fermeture d'un interrupteur. 

Dans ce chapitre, on va étudier les régimes transitoires dits du **premier ordre**.

Nous allons étudier ce phénomène à travers un exemple simple et courant : la charge et la décharge d'un condensateur.

## 2. Charge et décharge d'un condensateur

### A. Condensateur

Un condensateur est un **dipôle** électrique, composé de deux armatures conductrices, séparées par un isolant (appelé diélectrique)

Il présente la propriété de pouvoir stocker des charges électriques contraires sur ses armatures. Cette propriété est caractérisée par sa **capacité électrique $C$**, exprimée en farads ($F$).

![](./img/04_C/capacitor.webp)

Le courant électrique, généralement noté $i$, correspond lui à un mouvement de charges électriques. On peut le décrire comme étant le *débit de charge électrique*, c'est à dire : $i(t) = \frac{dq}{dt}$.

Le courant dans un condensateur est donc créé lorsque les charges sont en cours d'accumulation (ou de déplétion) sur les armatures. La relation caractéristique du condensateur s'écrit : 
$$ i_C(t) = C \dfrac{du_C}{dt} $$ 

En d'autres termes, il existe un courant électrique dans le condensateur lorsqu'il existe une modification de la tension du condensateur. 

En pratique, on peut relier la charge du condensateur à sa tension en remarquant : 

$$ i_C(t) = \dfrac{dq_C}{dt} = C \dfrac{du_C}{dt}  $$

$$ \Leftrightarrow q_C(t) = C u_C(t) $$

### B. Circuit RC série et charge d'un condensateur