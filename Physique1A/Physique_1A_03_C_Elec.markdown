---
layout: default
title:  "Physique A1 - Chapitre 3 - Électronique - Bases"
date:   2024-07-01 12:19:36 +0200
categories: courses
id: Phy1_03_C
---

# Chapitre 3 : Fondements de l'électrocinétique

## 1. Notions de base

Le terme électrocinétique renvoie à l'ensemble des phénomènes et des lois relatifs aux charges électriques en **mouvement**.

### A. Charge électrique

La charge électrique, notée $q$, caractérise la capacité de la matière à interagir par des champs électromagnétiques (on peut considérer que c'est une grandeur analogue à la masse, à la différence près qu'une charge électrique peut être négative). La charge électrique est quantifiée, avec une quantité élémentaire : $e = 1,6\times 10^{-19} C$. Ceci correspond à la charge d'un proton, ou celle d'un électron (à un signe près).

### B. Courant électrique

Le courant électrique, généralement noté $i$, correspond lui à un mouvement de charges électriques. On peut le décrire comme étant le *débit de charge électrique*, c'est à dire : $i(t) = \frac{dq}{dt}$.

Il existe différents types de porteurs de charges. Typiquement, dans les fils électriques, les porteurs de charges sont les électrons. Dans des solutions aqueuses, les porteurs de charges sont des ions. 

**Ordres de grandeur des courants électriques :**

| Intensité électrique | Phénomène / dispositif correspondant |
|--|--|
|$10mA$|LED|
|$100mA$|Début de risque d'électrocution*|
|$1 A$|Ampoule à incandescence|
|$10 A$|Radiateur électrique|
|$100 A$|Démarreur automobile|
|$500 A$|Moteur de locomotive TGV|
|$1 kA$|Lignes à haute tension|
|$10 - 100 kA$|Éclairs orageux|

*Un courant alternatif de $75mA$ à $50 Hz$ pendant une seconde produit une fibrillation ventriculaire.

### C. Potentiel électrique

Le **potentiel électrique** est intimement lié à la notion de **champ électrique**. Pour comprendre ce dernier, il peut être utile d'utiliser une analogie avec le champ gravitationnel. 

**Analogie charge-masse, champ électrique-gravitationnel**

Tout corps de masse $M$ produit autour de lui une force d'attraction sur tout objet de masse $m$ dans son environnement, définie par : 

$$\vec{F} = -\dfrac{GMm}{r^2}\vec{u_r}$$

On peut écrire cette relation sous la forme : 

$$\vec{F} = m \times \left(-\dfrac{GM}{r^2}\vec{u_r}\right)$$

Et on retrouve la relation bien connue des lycéens : $\vec{F} = m \vec{g}$ (dans le cas d'un objet à la surface de la Terre, notamment)

Or, en fonction de la distance du corps de masse $m$ à celui de masse $M$, on sait que la valeur de $\vec{g}$ peut varier. En fait, $\vec{g}$ est différent en tout point de l'espace. Plus on s'éloigne, plus sa valeur diminue. De plus, sa direction est toujours en direction du corps de masse $M$. 

On vient de définir un **champ vectoriel**, c'est à dire une fonction vectorielle, qui prend une valeur dépendant de la position où on la considère. 

**Quelques exemples d'autres champs :**

- Une carte des vents (champ vectoriel)
- Une carte de la température (champ scalaire)

<table>
  <tr>
    <td style="text-align: center;"><img src="./img/03_C/vent.png" alt="Image 1" style="width: 100%; max-width: 200px;"></td>
    <td style="text-align: center;"><img src="./img/03_C/temp.png" alt="Image 2" style="width: 100%; max-width: 200px;"></td>
  </tr>
  
</table>

