---
layout: default
title:  "TNI : Bases"
date:   2024-07-01 12:19:36 +0200
categories: exercises
id: TNI_01
---

# 0. Outils utilisés

Les manipulations seront effectuées via la librairie opencv de python. 

On utilisera les imports suivants : 

~~~
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
~~~

# A. Affichage de l'image / canaux RGB

La fonction *cv2.imread* permet d'importer une image dans une variable. 

~~~
img = cv2.imread('exemple.jpg')
print(img)
plt.imshow(img)
~~~

> Qu'affiche-t-on avec *print(img)* ?
> Qu'affiche-t-on avec *plt.imshow(img)* ? 
>
> Comment obtenir les informations de résolution / quantification de l'image ? 
>
> Les différents formats d'image sont-ils tous acceptés ? 

Dans le cas d'une image couleur, celle-ci est généralement composées de trois images superposées : un canal rouge, vert, et bleu. (Remarque : on a depuis bien longtemps abandonné l'utilisation des images indexées, mais bon, ça a existé).

Afin de séparer (ou recomposer) les différents canaux d'une image, on va utiliser les fonctions suivantes : 

~~~
C1, C2, C3 = cv2.split(img)
img_new = cv2.merge((C1, C2, C3))
~~~

> Afficher chaque canal indépendemment. Donner l'ordre de codage des différents canaux (remarque : cet ordonnancement n'est pas toujours le même en fonction des librairies !)
>
> Que se passe-t-il si on recomposer l'image "dans le mauvais sens" ? (i.e. inversion vert/bleu)

# B. Manipulations basiques

On va s'intéresser à quelques opérations de base. 

> Comment inverser une image en niveaux de gris ? 
>
> Comment augmenter la luminosité d'une image en niveau de gris ? 
> 
> Comment transférer votre image chez Amélie Poulain ? 