---
layout: default
title:  "TNI : Bases"
date:   2024-07-01 12:19:36 +0200
categories: exercises
id: TNI_00
---

# Outils utilisés

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

![](./Queyras.jpg)

(Crédits photo : https://github.com/DaluS)

> Qu'affiche-t-on avec *print(img)* ?
> Qu'affiche-t-on avec *plt.imshow(img)* ? L'image s'affiche-t-elle correctement ? 
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

## A1. Image en niveaux de gris (grayscale)

On peut également choisir d'afficher une image RGB en niveau de gris :

~~~
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
~~~

> Comment est calculé la valeur du pixel sur l'image en niveaux de gris ? 

# B. Manipulations basiques

On va s'intéresser à quelques opérations de base. 

## B1. Manipulations sur les valeurs de pixels

> Comment inverser une image en niveaux de gris ? 
>
> Comment augmenter la luminosité d'une image en niveau de gris ? 
> 
> Comment transférer votre image chez Amélie Poulain ? 

## B2. Manipulations sur les coordonnées des pixels

> Comment créer une sous-image ? (cropping)
>
> (On pourra également dessiner un rectangle sur l'image de base en utilisant la fonction *cv.rectangle*)
>
> Comment effectuer une symétrie de l'image ? (symétrie axiale verticale, horizontale, ou symétrie centrale)

## B3. Changement de taille de l'image

> Pour une image donnée, changer la taille pour correspondre à un format donné. 
>
> Est-il possible d'augmenter le nombre de pixels d'une image ainsi? Cela permet-il d'augmenter la résolution d'une image ? 