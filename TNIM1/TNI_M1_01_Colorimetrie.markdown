---
layout: default
title:  "TNI : Colorimétrie"
date:   2024-07-01 12:19:36 +0200
categories: exercises
id: TNI_01
---

# Introduction

Dans cette séance, le but va être de modifier une image en fonction des informations contenues dans les canaux RGB.

## A1. Histogrammes

Il peut être intéressant dans une image de dresser l'histogramme des valeurs de pixels. 

~~~
plt.hist(img.ravel(), 256)
~~~

> Que représente un tel histogramme ? 
>
> Que se passe-t-il si on applique la même fonction aux différents canaux ? 

## A2. Profil d'intensité lumineuse

L'histogramme nous permet d'avoir une répartition statistique de l'intensité de tous les pixels de l'image. Cependant, on perd alors l'information de localisation des pixels. 

Afin de passer outre cette limite, on peut tracer le profil d'intensité des pixels le long d'une ligne donnée. 

> Sur l'image de la section précédente, tracer une ligne verticale. 
>
> Tracer le profil d'intensité des pixels le long de cette ligne en utilisant les coordonnées des pixels considérés en abcisse, et leur valeur d'intensité en ordonnée. 

## A3. Binarisation / seuillage

On peut ensuite choisir de binariser l'image, c'est à dire de choisir une valeur seuil au dessus de laquelle les pixels deviennent blancs, et en dessous de laquelle les pixels deviennent noirs.

~~~
a, img_t = cv2.threshold(img, 200, 255, cv2.THRESH_BINARY)
~~~

> Effectuer cette opération sur une image en niveaux de gris, puis sur une image RGB.
>
> Commenter sur l'intérêt d'une telle opération.
>
> Effectuer la même opération en utilisant un seuillage dit "adaptatif" afin de tenir compte des variations de luminosité éventuelles dans l'image. (*cv2.adaptiveThreshold*)

## A4. Manipulations colorimétriques

> En utilisant les fonctions étudiées ci-dessus:
>
> _ séparer les manchots ci-dessous du reste de l'image, et emmenez-les en vacances vers la destination de votre choix. 
>
> _ quelles inversions de couleurs pouvez-vous effectuer sur l'image de Rubik's Cube ci-dessous ?

![](./manchots.jpg)

![](./Cube.png)