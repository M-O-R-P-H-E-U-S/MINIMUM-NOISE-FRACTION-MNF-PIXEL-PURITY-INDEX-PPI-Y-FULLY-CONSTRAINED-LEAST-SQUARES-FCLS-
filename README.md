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


METODOS
-----


Minimum Noise Fraction(MNF)
-----

Minimum Noise Fraction(MNF) es una transformada lineal que consta de 2 pasos separados:

* Usar el matriz de covarianza de ruido para decorrelacionar y reescalar el ruido en los datos (blanqueamiento de ruido). De esta forma, el ruido tiene varianza unitaria y no tiene correlaciones de banda a banda.

* Realizar un estándar Transformación de PCA a los datos blanqueados por ruido.


METODOLOGIA
-----

Para el registro de las imágenes hiper-espectrales, se uso una cámara Pika NIR-320(Near-Infrared) que abarca desde 900 a 1700 nm. Para su uso primero se calibra la cámara respecto a la referencia en negro, que es cuando se tiene tapada la lente de la cámara. Posteriormente se toma una referencia en blanco donde se retira la tapada de la lente de la cámara y se toma a una superficie totalmente blanca, en nuestro caso una pieza de teflón.



Posteriormente se ajusta la velocidad de la plataforma donde se coloca la muestra respecto de la cámara para poder calibrar espacialmente la cámara.





En el presente trabajo se registro la imágen hiper-espectral
de una manzana (Imagen: 2) en comienzos de putrefacción

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


Minimum Noise Fraction(MNF)
-----




Pixel Purity Index(PPI)
-----


CLASIFICACIÓN DE ENDMEMBERS
-----


Fully Constrained Least Squares(FCLS)
-----



DISCUSIÓN DE RESULTADOS
-----








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

