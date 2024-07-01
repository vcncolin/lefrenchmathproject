---
title: Home
author: Vincent G. COLIN
date: July 1, 2024
---

# Chapitre 3 : Compléments d'algèbre linéaire

## Sous-espaces vectoriels et familles de vecteurs

## Applications linéaires

### Exercice 11

Soient $n \in \mathbb{N}$ et $D$ l'application : 
$$
\begin{array}{rlll}
D: \mathbb{R}_n[X] & \longrightarrow & \mathbb{R}_n[X] \\
P & \longrightarrow & P^{\prime}
\end{array}
$$

1. Vérifier que $D$ est un automorphisme de $\mathbb{R}_n[X]$
2. On pose $\Gamma = id_{\mathbb{R}_n[X]} + D + D^2 + ... + D^n$. Montrer que $\Gamma$ est un automorphisme.
3. Rappeler une factorisation usuelle de $1 - X^{n+1}$
4. En déduire $\Gamma \circ (id - D)$
5. En déduire l'application réciproque de $\Gamma$ 

#### Corrigé :

1. $D$ est un endomorphisme car $D$ est linéaire, et $P' \in \mathbb{R}_n[X]$
2. $\Gamma$ transforme la base canonique de $\mathbb{R}_n[X]$ en famille libre de $\mathbb{R}_n[X]$, de dimension $n+1$. On peut donc dire que $\Gamma$ est une application linéaire (car somme d'applications linéaires), bijective, de $\mathbb{R}_n[X]$ vers $\mathbb{R}_n[X]$, donc $\Gamma$ est un automorphisme. 
3. $(1-X^{n+1}) = (1-X) . \sum_{k=0}^n X^k$ TMTC
4. En réécrivant l'égalité précédente en plissant un peu les yeux, on obtient : 
$\Gamma \circ (id - D) = (id - D^{n+1})$
Il est alors important de remarquer que dans $\mathbb{R}_n[X]$, $D^{n+1} = 0$. On en déduit alors que dans $\mathbb{R}_n[X]$, $\Gamma \circ (id - D) = id$

<ul>
{% for item in site.notes %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>

<!-- - [The Space Charge Geometry Factor](/g)
- [The **Effective** Space Charge Geometry Factor](/g_bar)
- [Closed Quasi-Elliptical Shapes](/shapes)
- [Generalized Quasi-Normal Distributions](/distributions)
- [Ray Tracing Intersection Algorithm](/ray_casting) -->
