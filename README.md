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

# Objetivo General

Modelar las predicciones basadas en la Regresión Lineal


# Objetivos Específicos

1 -  Seleccionar un dataset<br>
2 -  Hacer una análitica de datos sobre el dataset seleccionado<br>
3 -  Modelar usando la regresión lineal usando Scikit-Learn<br>
4 -  Modelar usando la regresión lineal usando C++<br>
5 -  Comparar los modelos<br>

# Introducción

El presente trabajo tiene como objetivo, realizar el análisis explorartorio de los datos, generar el modelo de gradiente descendente y evaluar el modelo implementado, tanto para lenguaje de c++ como para lenguaje de python, con el fin de comparar los resultados obtenidos en un lenguaje de alto y bajo nivel.<br>
Para ello se hace uso del dataset, "HousingPrices", el cual contiene hasta 80 características que influyen con respecto al precio de una casa, sin embargo, de este dataset se usan únicamente 4 características que corresponden a:<br>
*   $OverallQual:$ Material general y calidad de acabado.
*   $TotalBsmtSF:$ Pies cuadrados totales del área.
*   $GrLivArea:$ Pies cuadrados de superficie habitable sobre el nivel del suelo.
*   $SalePrice:$ El precio de venta de la propiedad en dólares. Esta es la variable de destino que está tratando de predecir.


# Desarrollo
A continuación, se encuentra el código realizado en c++, el cual contiene:<br><br>
**Carpeta DataSets**
*   El dataset HousingPrices
<br><br>

**Extraccion**
*   *Extraction.cpp:* código fuente para la extracción del dataset, cuenta con los respectivos métodos para hallar el promedio, la desviación, la normalización de los datos y la división en datos de entrenamiento y prueba.
*   *Extraction.h:* es el header que contiene únicamente los métodos de Extraction.cpp.
<br><br>

**Regresion**
*   *Regresion.cpp:* código fuente para hallar la función de costo, el gradiente descendente y el coeficiente de determinación.
*   *Regresion.h:* es el header que contiene únicamente los métodos de Regresion.cpp.
<br><br>

**Otros**
*   *CMakeLists:* contiene las instrucciones que se deben ejecutar, como crear el objeto (-c)  y crear el ejecutable enlazando el objeto (-o), todo en un solo archivo, que a la vez se encargue de borrar los archivos creados a medida que se actualicen.
*   *main.cpp:* Invoca las funciones a usar, con sus respectivos parámetros
*   *Archivos .txt:* contienen los costos y thetas obtenidos tras implementar el modelo.
<br><br>

**Cuaderno**<br>
En cuanto al código realizado en python, se encuentra en el siguiente cuaderno:
https://colab.research.google.com/drive/1P1_q0L7fkEUcu9vk-sDrfwqnVVb4Vtgx?usp=sharing

# Conclusiones:
*  Se importan las bibliotecas requeridas, Pandas, Scikit Learn, Seaborn, etc.
*  El dataset cuenta con 3 características independientes y una dependiente, que corresponden al precio estimado de una casa.
*  Se dividen los datos, el 80% superior en entrenamiento, y el 20% inferior en prueba, para que el modelo aprenda con los datos de entrenamiento y luego pueda corroborar el ajuste del modelo, con los datos de prueba.
*  Se presentan visualizaciones de los valores atípicos, distriución de los datos, matriz de correlación, función de costo, modelo implementado, comparaciones de coeficiente de determinación para cada característica y una gráfica de dispersión de los valores reales vs los estimados.
*   Se visualiza que los datos no poseen valores nulos y se encuentran con el mismo tipo de dato, int.
*  Se detecta una gran cantidad de valores atípicos que perjudican el modelo, debido a que si se eliminan los datos con el fin de mantener una igualdad en los datos, el modelo pierde robustez, pero si se llenan con valores generados estos no reflejan los datos verdaderos presentando problemas en el modelo. 

* La matriz de dispersión permite observar que `Gr Liv Area, Overall Qual y TotalBsmtSF` presentan una correlación notable con la variable `SalePrice`, sin embargo, la variable con mayor correlación es "Overall Qual".

* Se observa en la gráfica de residuos, que los datos se encuentrar alrededor del eje x, es decir, logran ajustarse al modelo lineal, aunque se puede alcanzar mayor precisión con un modelo no lineal.

* Según la gráfica de cuantiles, los datos están sesgados un poco a la derecha.

* De las métricas usadas para medir la calidad del modelo, se obtiene que la mejor es el R2, con 0.77 para datos de entrenamiento y 0.61 para datos de prueba, lo cual es aceptable.

* Se recomienda realizar un estudio más detallado de los datos que tienen mayor correlación con el objetivo de generar un modelo más robusto.

* Se recomienda aumentar la cantidad y calidad de los datos evitando los datos atípicos.

* Finalmente, se evidencia que los valores obtenidos en python son muy similares a los calculados con Eigen.

# Referencias

* Heras, J. M. (2020, 20 septiembre). Gradiente Descendiente para aprendizaje automático. IArtificial.net. Recuperado 16 de octubre de 2022, de https://www.iartificial.net/gradiente-descendiente-para-aprendizaje-automatico/ Loukas, S. (2020, 30 mayo).<br>
* PCA clearly explained —When, Why, How to use it and feature importance: A guide in Python. Towards Data Science. https://towardsdatascience.com/pca-clearly-explained-how-when-why-to-use-it-and-feature-importance-a-guide-in-python-7c274582c37e<br> 
* Scikit Learn - 
Stochastic Gradient Descent. (s. f.). Recuperado 16 de octubre de 2022, de https://www.tutorialspoint.com/scikit_learn/scikit_learn_stochastic_gradient_descent.htm<br> 
* scikit-learn - sklearn.linear_model.LinearRegression - Regresión lineal de mínimos cuadrados ordinarios. LinearRegression se ajusta a u - Español. (s. f.). Recuperado 16 de octubre de 2022, de https://runebook.dev/es/docs/scikit_learn/modules/generated/sklearn.linear_model.linearregression<br>
*  sklearn.linear_model.SGDRegressor. (s. f.). scikit-learn. Recuperado 16 de octubre de 2022, de https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDRegressor.html


