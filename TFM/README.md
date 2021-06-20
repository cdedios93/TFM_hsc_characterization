# Sobre este repositorio

El **objetivo** de este Trabajo de Final de Máster ha sido caracterizar el envejecimiento de las células madre hematopoyéticas mediante técnicas de *computer vision* y *machine learning*

## Guía sobre documentos
Como cabe esperar puesto que pertenecen a un mismo trabajo, todos los notebooks son complementarios entre sí y siguen un orden temporal. En nuestro caso, ese orden temporal es: 

1) **Perimetraje CMH**: Recortaba la CMH de la imagen y guardaba una imagen en escala de grises para cada uno de sus canales.
2) **Verificación con la investigadora experimentada**: Comparte información de cada uno de los tres canales y explica motivos de duda a la investigadora experimentada
3) **Algoritmo_Segmentación_3D**: Realiza una segmentación basada en binarización por umbral de Otsu seguido por operaciones morfológicas. Tras la segmentación extrae características.
4) **Visualizacion_estadistica_caract_CMH**: Genera un boxplot para comparar características entre CMHs viejas y jóvenes y aplica un test estadístico para evaluar la significación de las diferencias entre grupos.
5) **Clasificador envejecimiento CMH**: Crea varios modelos de *machine learning* y los evalúa con las métricas de accuracy y AUC

Existen otros notebooks intermedios de las aproximaciones preliminares que pueden visualizarse en las carpetas Entregable 1 y 2.

## Librerías utilizadas
Las librerías utilizadas para este trabajo han sido las siguientes:

**Scikit-Image y OpenCV**: Son las librerías que se han usado para todo el proceso de *computer vision* y procesamiento de imagen y las que han permitido llegar a la segmentación y extracción de características

**Numpy**: Para el trabajo con los array. Recordemos que una imagen es una matriz multidimensional (2D si es en escala de grises y 3D si es a color). Todas las operaciones que se hacen sobre ellas deben contemplar el manejo de arrays y por tanto Numpy es esencial para ello.

**Pandas**: Para el manejo de los dataframe y la carga de Excel

**Matplotlib**: Para graficar las imágenes sobre el propio notebook y facilitar la visualización

**Seaborn**: Para la graficación del plotbox

**Scipy**: Para los test estadísticos

**Scikit-Learn**: Para la creación de los modelos de clasificación basados en *machine learning*
