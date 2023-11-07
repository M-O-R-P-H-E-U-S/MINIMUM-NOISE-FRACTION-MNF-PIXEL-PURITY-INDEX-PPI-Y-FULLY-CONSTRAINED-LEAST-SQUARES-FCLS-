---
bibliography: Bibliography.bib
csl: apa.csl
---

# MINIMUM NOISE FRACTION(MNF), PIXEL PURITY INDEX(PPI) Y FULLY CONSTRAINED LEAST SQUARES(FCLS) PARA LA EXTRACCION Y CLASIFICACION DE ENDMEMBERS, EN EL ESTUDIO DE IMAGENES HIPERESPECTRALES.

Abstract
-----
Preprocessing techniques such as Minimum Noise Fraction (MNF) and Pixel Purity Index (PPI) that reduce
dimensionality of the hypercube a Hyperspectral Imaging (HSI) data, a have been widely used to reduce the computational
cost when analyzing Hyperspectral Images (HSI). Pixel Purity Index (PPI) not only reduces the spatial dimension of our
hypercube, but also allows the extraction of endmembers, that is, it distinguishes the purest spectral signatures within each
pixel. For the classification of endmembers extracted from our hypercube, an abundance map of each endmember was
used, according to the Fully Constrained Least Squares (FCLS) algorithm. Finally, the spectra found in the abundance
maps were compared with reference spectra in the spectronon pro software.

Resumen
-----
Las técnicas de preprocesamiento, como Minimum Noise Fraction (MNF) y Pixel Purity Index(PPI) que reducen
dimensionalidad del hipercubo de datos a Imágenes Hiperespectrales (HSI), han sido usadas ampliamente para reducir el
costo computacional al analizar Imágenes Hiperespectrales (HSI). Píxel Purity Index(PPI) no solo nos reduce la dimensión
espacial de nuestro hipercubo, sino que además permite la extracción de endmembers, es decir, se distingue las firmas
espectrales mas puras dentro de cada píxel. Para la clasificación de endmembers extraídos de nuestro hipercubo, se uso un
mapa de abundancia de cada endmember, según el algoritmo de Fully Constrained Least Squares(FCLS). Finalmente los
espectros encontrados en los mapas de abundancia fueron comparados con espectros de referencia en el software spectronon
pro.

Index Terms— Minimum Noise Fraction (MNF), Pixel Purity Index(PPI), Fully Constrained Least Squares(FCLS),
Hyperspectral Imaging(HSI).

INTRODUCCION
-----

Las imágenes hiperespectrales son una recopilación de la reflectancia sobre cada pixel en el rango del espectro
electromagnético. Una imagen hiperespectral combina la naturaleza digital de una cámara y la naturaleza
espectroscopia de su muestra. Una cámara de naturaleza hiperespectral adquiere la intensidad de la luz de un gran
número de bandas espectrales contiguas. 

La finalidad de estudiar las imágenes hiper-espectrales
es obtener el espectro de una escena convertida en una imagen donde dicha imagen es representada por un cubo
de datos que encierra una dimensión espacial y espectral. Con la finalizar de caracterizar nuestra muestra o encontrar
objetos imperceptibles por el ojo humano. 

En este sentido el análisis de toda esta información que proporcionan las imágenes hiperespectrales consumen demasiados recursos de la computadora. Por ello se ha visto la necesidad de realizar un preprocesamiento a este conjunto de datos. Siendo necesarias técnicas de reducción de dimensionalidad. Recordando que las imagenes hiperespectrales tienen dimension espacial y espectral. Se requirierontecnicas de preprocesamiento que reduscan dichas dimensiones, en la siguiente tabla se mencionan algunas de estas técnicas1:

| Reduccion espectral | Reduccion espacial |
| ------------------- | ------------------ |
|         MNF         |          PPI       |   
|         PCA         |          VCA       |  
|         ICA         |          ICE       |    
|         UBD         |          N-FINDR   |   

Las imagenes hiperespectral se ven aplicadas en campos como minería, agricultura, fraude, contaminación, etc.


Con el avance de la tecnologia se ha podido desarrollar camaras hiperespectrales que registrar una mayor cantidad de bandas contiguas del espectro de reflectancia de la escena analizada. A la misma velocidad con la que se desarrollan
estas camaras se han visto nuevas publicaciones con nuevas tecnicas de procesamiento de imagenes hiperespectrales.
Dichas tecnicas facilitan el camino para una amplia gama de aplicaciones [1] [2].

Si bien es cierto la información contenida en los datos hiperespectrales permite la caracterización, identificación
y clasificación de distintas muestras. Sin embargo, hay problemas críticos que deben ser considerados en la clasificación de datos hiper-espectrales, entre los cuales:

1) El alto número de canales espectrales.
2) La variabilidad espacial de la firma espectral.

METODOS
-----

Minimum Noise Fraction(MNF)
-----

Minimum Noise Fraction(MNF) es una transformada lineal que consta de 2 pasos separados:

1) Usar el matriz de covarianza de ruido para decorrelacionar y reescalar el ruido en los datos (blanqueamiento de ruido). De esta forma, el ruido tiene varianza unitaria y no tiene correlaciones de banda a banda.

2) Realizar un estándar Transformación de PCA a los datos blanqueados por ruido.








METODOLOGIA
-----

Para el registro de las imágenes hiper-espectrales, se uso una cámara Pika NIR-320(Near-Infrared) que abarca desde 900 a 1700 nm. Para su uso primero se calibra la cámara respecto a la referencia en negro, que es cuando se tiene tapada la lente de la cámara. Posteriormente se toma una referencia en blanco donde se retira la tapada de la lente de la cámara y se toma a una superficie totalmente blanca, en nuestro caso una pieza de teflón.

Posteriormente se ajusta la velocidad de la plataforma donde se coloca la muestra respecto de la cámara para poder calibrar espacialmente la cámara.

![pro](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/pro.jpeg)

En el presente trabajo se registro la imágen hiper-espectral de una manzana (Imagen: 2) en comienzos de putrefacción

![manzana_real](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/manzana_real.png)

A continuación se muestra la imagen hiperespectral de la manzana tomada con la cámara Pika 320.




En la siguiente imagen (4) se muestra las partes de la manzana que serán relevantes para nuestro estudio de la escena multipixel de la manzana.

![manzana_real](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/manzana_pro.jpeg)

A continuación se muestra la imagen en falso color de la manzana mostrando con mas claridad zonas que no son percibidas con facilidad para el ojo humano.

![manzana_real](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/pseudocolor.png)

El presente articulo se divide en dos partes:

**Primera Parte** - **Detección de Endmembers:** Analizamos las dimensiones espectrales y espaciales de las imágenes hiper-espectrales. De Minimum Noise Fraction(MNF) reducimos su dimensión espectral y de Pixel Purity Index(PPI) una reducción espacial. Recordando que MNF es un PCA, pero con la matriz de ruido redefinida. Podemos usar los primeros componentes principales para determinar el rango de los primeros redundantes. Dado que PPI proyecta cada píxel en un vector de un conjunto de vectores aleatorios(skewers) que pertenecen al espacio de reflectancia. Dichos píxeles reciben una puntuación cuando representan un extremo de todas las proyecciones. Los píxeles con las puntuaciones más altas son considerado espectralmente puro. Dándonos un nuevo conjunto de grupos dispersos.

**Segunda parte** - **Clasificación de Endmembers:** Con el nuevo conjunto de datos, pero de grupos diversos.
Elaboramos nuestro algoritmo de Fully Constrained Least Squares(FCLS) para clasificar estos endmembers segun la ubicación y cantidad de píxeles que se distinguen en el mapa de abundancia, y grupos que reconocemos de la imagen hiper-espectral.




DETECCIÓN DE ENDMEMBERS
-----




|Número de banda  |  Longitud de onda(nm)  |
| --------------- | ---------------------- |
|      1          |          894.48        |   
|      2          |          899.25        |  
|      3          |          904.02        |    
|      4          |          908.8         |   
|      5          |          913.58        |   
|      6          |          918.36        |  
|      7          |          923.15        |    
|      8          |          927.93        |   
|      9          |          932.72        |   
|      10         |          937.51        |  


![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/espec_norm.png)

![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/mapa_datos_manzana.jpg)


Minimum Noise Fraction(MNF)
-----

![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/mnf_manzana.jpg)

![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/CP_mnf_manzana.jpg)


|    Número de CP    |  Varianza  |
| ------------------ | ---------- |
|      CP 1          | 8.7378e-07 |   
|      CP 2          | 3.1030e-08 |  
|      CP 3          | 1.1267e-07 |    
|      CP 4          | 1.0859e-07 |   
|      CP 5          | 3.1810e-08 |   
|      CP 6          | 1.9613e-07 |



Pixel Purity Index(PPI)
-----

![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/ppi_manzana.jpg)




CLASIFICACIÓN DE ENDMEMBERS
-----


Fully Constrained Least Squares(FCLS)
-----

![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/abu_fcls_manzana.jpg)

![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/mean_end_manzana.jpg)



|      Componente    |  Número de Pixeles  |
| ------------------ | ------------------- |
|      Componente 1  |         3           |   
|      Componente 2  |         3010        |  
|      Componente 3  |         55          |    
|      Componente 4  |         13277       |   
|      Componente 5  |         12987       |   
|      Componente 6  |         3598        |



DISCUSIÓN DE RESULTADOS
-----





![espec_norm](https://github.com/M-O-R-P-H-E-U-S/MINIMUM-NOISE-FRACTION-MNF-PIXEL-PURITY-INDEX-PPI-Y-FULLY-CONSTRAINED-LEAST-SQUARES-FCLS-/blob/main/espectro_pro.jpg)


|Componente   |  Nombre         | Número de Endmember | 
| ----------  | --------------- |-------------------- |
|Componente 1 |  Mesocarpio     |    Endmember 1      |   
|Componente 2 |  Zona podrida   |    Endmember 2      |  
|Componente 3 |  Pedunculo      |    Endmember 3      |    
|Componente 4 |  Cascara        |    Endmember 4      |   
|Componente 5 |  Fondo          |    Endmember 5      |   
|Componente 6 |  Zona podrida   |    Endmember 6      |


CONCLUSION
-----

Con la metodología seguida es posible distinguir los componentes dentro de una escena multipixel. Contrastando con el promedio espectral obtenido del Datacube analizado en el software Resonon(fig: \ref{fig:Firma-Componentes.}). 

