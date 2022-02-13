# Laboratorio 2 de Security Data Science
Sergio Marchena - 16387

## Datasets
Se utilizaron 2 datsets en conjunto para predecir SPAM. Estos fueron 'enronSpamSubset.csv' y 'completeSpamAssassin.csv'.

## Desarrollo 

### PARTE 1 - INGENIERIA DE CARACTERISTICAS

Para esta parte se hicieron las siguientes tareeas: 
  - Exploracion de datos
  - Preprocesamiento y
  - Representacion de Texto

### PARTE 2 - IMPLEMENTACION DE MODELOS

En esta seccion, se hicieron las siguientes tareas:
  - Separacion de los datos: 70% train, 30% test
  - Implementacion en cada uno de las representaciones numericas:
    - Para el modelo 1 (BOW) se obtuvieron los siguientes resultados: 
    ```
    0.7839634399667637
    Matriz de confusion [[2194  546]
    [ 494 1580]]
              precision    recall  f1-score   support

           0       0.82      0.80      0.81      2740
           1       0.74      0.76      0.75      2074

    accuracy                           0.78      4814
    macro avg      0.78      0.78      0.78      4814
    weighted avg   0.78      0.78      0.78      4814
    ```
    - Para el modelo 2 (Bi-grams) se obtuvieron los siguientes resultados: 
    ```
    0.7839634399667637
    Matriz de confusion [[2194  546]
    [ 494 1580]]
              precision    recall  f1-score   support

           0       0.82      0.80      0.81      2740
           1       0.74      0.76      0.75      2074

    accuracy                           0.78      4814
    macro avg      0.78      0.78      0.78      4814
    weighted avg   0.78      0.78      0.78      4814
    ```
    - Para el modelo 3 (TF-ID) se obtuvieron los siguientes resultados: 
    ```
    0.8315330286663897
    Matriz de confusion [[2390  350]
    [ 461 1613]]
              precision    recall  f1-score   support

           0       0.84      0.87      0.85      2740
           1       0.82      0.78      0.80      2074

    accuracy                           0.83      4814
    macro avg      0.83      0.82      0.83      4814
    weighted avg   0.83      0.83      0.83      4814
    ```
    
## Conclusion

> Qué representación numérica produjo el mejor resultado?

El mejor resultado a primera vista lo tiene la tercera representacion (TF-ID) con una accuracy de 0.83, lo cual estadisticamente es un valor bajo pero es el mejor obtenido con estas representaciones y algoritmo de Naive Bayes Multinomial. Los resultados de las representaciones de BOG (1 y 2) son exactos entre si, con 0.78 de accuracy para las dos, y los mismos valores de precision (0.82, 0.74), recall (0.80, 0.76) y f1-score (0.81, 0.75). Esto se debe a que es la misma forma de representacion numerica pero solo variaba el valor de n, lo cual en textos muy grandes de SPAM no ayuda mucho. Ahora bien para la representacion numerica de TF_ID se obtuvo una precision de (0.84 y 0.82), un recall de (0.87 y 0.78) y un valor de f1 de (0.85, 0.80). Lo cual es suficiente para concluir que el mejor resultado es con la representacion TF-ID
