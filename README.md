# Encabezado
<p align="center"><img src="https://res-5.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco/v1455514364/pim02bzqvgz0hibsra41.png"width="200" height="200">
</img><br>
<i><b>Docente:</b></i> John Corredor, PhD.
<br>
<i><b>Asignatura:</b></i> Introducción HPC
<br>
<i><b>Estudiante:</b></i> Edna Sofía Orjuela Puentes
<br>
<i><b>Tema:</b></i> LinearRegression_HousingPrices
<br>
<i><b>Fecha:</b></i>26/10/22
<br>
</p>

# Objetivo General: 

Modelar las predicciones basadas en la Regresión Lineal


# Objetivos Específicos:

1 -  Seleccionar un dataset<br>
2 -  Hacer una análitica de datos sobre el dataset seleccionado<br>
3 -  Modelar usando la regresión lineal usando Scikit-Learn<br>
4 -  Modelar usando la regresión lineal usando C++<br>
5 -  Comparar los modelos<br>

# Introducción

El presente trabajo tiene como objetivo, realizar el análisis explorartorio de los datos, generar el modelo de gradiente descendente y evaluar el modelo implementado, tanto para lenguaje de c++ como para lenguaje de python, con el fin de comparar los resultados obtenidos en un lenguaje de alto y bajo nivel.<br>
Para ello se hace uso del dataset, "HousingPrices", el cual contiene hasta 80 características que influyen con respecto al precio de una casa, sin embargo, de este dataset se usan únicamente 4 características que corresponden a:<br>
*   $OverallQual:$ Material general y calidad de acabado.
*   $TotalBsmtSF:$ Pies cuadrados totales del área
*   $GrLivArea:$ Pies cuadrados de superficie habitable sobre el nivel del suelo (suelo)
*   $SalePrice:$ El precio de venta de la propiedad en dólares. Esta es la variable de destino que está tratando de predecir.


# Desarrollo
A continuación, se encuentra el código realizado en c++, el cual contiene:<br>
**Carpeta DataSets**
*   El dataset HousingPrices 
<br>**Extraccion**
*   Extraction.cpp: código fuente para la extracción del dataset, cuenta con los respectivos métocos para hallar el promedio, la desviación, la normalización de los datos y la división en datos de entrenamiento y prueba.
*   Extraction.h: es el header que contiene únicamente los métodos de Extraction.cpp.
<br>**Regresion**
*   Regresion.cpp: código fuente para hallar la función de costo, el gradiente descendente y el coeficiente de determinación.
*   Regresion.h: es el header que contiene únicamente los métodos de Regresion.cpp.
<br>**Otros**
*   CMakeLists: contiene las instrucciones que se deben ejecutar, como crear el objeto (-c)  y crear el ejecutable enlazando el objeto (-o), todo en un solo archivo, que a la vez se encargue de borrar los archivos creados a medida que se actualicen.
*   main.cpp: Invoca las funciones a usar, con sus respectivos parámetros
*   Archivos .txt: contienen los costos y thetas obtenidos tras implementar el modelo.

En cuanto al código realizado en python, se encuentra en el siguiente cuaderno:<br>

