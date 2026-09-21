---
title: "Clustering Jerárquico"
author: ["Avila Agramonte, Edgar"]
date: "20/09/2026"
subject: "Clustering Jerárquico"
keywords: [Clustering Jerárquico, Machine Learning]
subtitle: "MCD202 - Machine Learning"
lang: "es"
titlepage: true,
titlepage-text-color: "FFFFFF"
titlepage-rule-color: "360049"
titlepage-rule-height: 0
titlepage-background: "background.pdf"
---

# Tarea 8: Machine Learning - Clustering Jerárquico

## 1. 20 Newsgroups

Vectorizamos 2378 documentos de cuatro categorías (sci.med, sci.space, rec.autos,
rec.sport.baseball) con TF-IDF a 500 características. Usando 2 linkages en
4 clusters.

Resultados: ward logra un silhouette de 0.0313 y complete de 0.0124. Ambos son
bajos por la alta dimensión de los textos, pero ward casi triplica a complete.

## 2. Segmentación de clientes

Creamos 150 clientes sintéticos en 4 grupos con make_blobs. Aplicamos ward y
complete con 4 clusters. Al generarse los datos con centros bien separados,
ambos linkages recuperan los cuatro grupos.

## 3. Segmentación de imágenes

Usamos la imagen coins de skimage y aplica segmentación con linkage ward con
conectividad de vecindad (grid_to_graph), la cual sirve para que la
segmentación tome en cuenta la cercanía de los píxeles y no solo su color.

La imagen queda dividida en 25 regiones (monedas y el fondo), en su mayoría
coincide con las monedas, pero en las 2 monedas de la parte superior izquierda
se desvía y no logra segmentarlas correctamente, muy posible debido a la 
iluminación y la región de sombra alrededor de toda la imagen que se segmentó
en un color morado un poco mas oscuro.
