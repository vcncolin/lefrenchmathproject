---
layout: default
title:  "TNI : Contours"
date:   2024-07-01 12:19:36 +0200
categories: exercises
id: TNI_02
---

# Introduction

Dans cette séance, le but va être de modifier une image afin d'extraire le contour des objets présents dans l'image.

## A. Détection d'objet

Une des tâches principales de *computer vision* consiste à détecter des objets dans une image, et notamment les contours de ces objets. 

Pour ce faire, on va utiliser des opérations de filtrage sur l'image. 

## A0. Convolution

Les opérations de filtrage en traitement d'image vont être représentées mathématiquement par des opérations de convolution entre des matrices : 

![](./2D_Convolution_Animation.gif)

(Wikipédia, *Michael Plotke*)

Une matrice de base, notée *input*, est convoluée avec un filtre, souvent appelé *kernel*. On déplace le filtre afin de l'aligner successivement avec toutes les parties de l'input, où une multiplication terme à terme est effectuée. (Pour plus de détails mathématiques : https://en.wikipedia.org/wiki/Convolution#Discrete_convolution)

En fonction du filtre (ou kernel) utilisé, le résultat pourra être plus ou moins pertinent.

Dans les parties suivantes, on va utiliser la fonction *cv2.filter2D* avec différents types de kernel, et tenter de qualifier les différentes opérations ainsi réalisées. 

## A1. Kernels

> En utilisant les kernels suivants, pouvez-vous qualifier les opérations réalisées ? 

$K1 = \begin{pmatrix} 0&0&0 \\ 0&1&0 \\ 0&0&0\end{pmatrix}$

$K2 = \frac{1}{9} \begin{pmatrix} 1&1&1 \\ 1&1&1 \\ 1&1&1 \end{pmatrix}$

$K1 = \begin{pmatrix} -1&-1&-1 \\ 2&2&2 \\ -1&-1&-1 \end{pmatrix}$