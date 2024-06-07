![proyecto](https://github.com/gaudikarina/Orange/assets/71100137/ff862f00-2964-48a8-ac88-7af211a863a5)# DETECTOR DE CONTRACCION MUSCULAR UTILIZANDO
SEÑALES ELECTROMIOGRÁFICAS SUPERFICIALES

Realizado por: Gaudi Morantes
Julio 2022

## OBJETIVOS
### GENERAL
Diseñar un detector de contracción muscular utilizando herramientas de
inteligencia artificial.
### ESPECÍFICOS
1. Preprocesar los datos a utilizar en el detector de contracción muscular utilizando
herramientas de inteligencia artificial.
2. Proponer el modelo de detector de contracción muscular utilizando
herramientas de inteligencia artificial.
3. Evaluar el detector con datos de prueba de contracción muscular utilizando
herramientas de inteligencia artificial.

## ENMARCADO DEL PROBLEMA DE MACHINE LEARNING
Está constituido en cinco pasos o etapas que son:
1. Definir el problema /Proponer solución.
2. Construir el juego de datos.
3. Transformar los datos.
4. Entrenar el Modelo.
5. Hacer Predicciones con el Modelo.

![fig1](https://github.com/gaudikarina/Orange/assets/71100137/c2de1deb-2037-4160-acf5-53037f87f4dd)

Preprocesamiento de Datos de entrenamiento y prueba en Orange

## ENTRENAR EL MODELO
Una vez obtenidos los datos preprocesados y trasformados, se entrena con los algoritmos SVM, Random Forest y Redes Neuronales, los hiperparámetros utilizados para estos algoritmos se muestran en la figura 10, se realizaron varios ajustes llegándose al mejor resultado para cada método con estos hiperparámetros.

![fig2](https://github.com/gaudikarina/Orange/assets/71100137/76acbe18-68d7-449d-a9dc-05c3de0b4d3d)

Parámetros de los algoritmos: a) SVM, b) NN, c) RF.


## DISCUSIÓN DE LOS RESULTADOS
En primer lugar, se realizó el preprocesamiento de los datos, combinando las técnicas que proporciona orange, siguiendo los principios del enmarcado de un problema de ML y en base al preprocesamiento básico que debe tener una señal bioeléctrica EMG. Esto dio como resultado una señal que respondió muy bien a los entrenamientos de los modelos propuestos.
En segundo lugar, se propusieron tres modelos: Máquinas de Soporte Vectorial, Bosques Aleatorios y Redes Neuronales, en este sentido, Redes Neuronales es un poco mejor que Bosques Aleatorios, para realizar la detección presentado un área bajo la curva del 93.7%, seguido muy de cerca por los bosques aleatorios con 92.7% y la máquina de soporte vectorial con un comportamiento bastante pobre de 50.9%, en los tres casos 
se realizaron variaciones en los hiperparámetros, obteniéndose el mejor resultado con los mostrados en la figura 10. En el caso de Test and Score se escogió una validación cruzada de 10 folds, debido a que ese fue el mismo criterio que se utilizó en el diseño de este detector utilizando un umbral optimizado como método de detección [6].
En tercer lugar se evalúo el modelo en unos datos de prueba, los mismos pertenecen a los datos de dos sujetos que no estaban en los datos de entrenamiento, para ello se utilizó el widget Test and score en este caso configurado como test on test data. Los resultados muestran un clasificador con una alta precisión del 88.3% para las redes neuronales y un área bajo la curva ROC de 95.2%. Es de destacar, que en los datos de prueba el método SVM desmejora notablemente y baja a un 19.1% en el área bajo la curva y una precisión de solo el 27,1%.
Comparando estos resultados con el trabajo realizado en [6] se obtuvo un área bajo la curva de 93%, por lo que el detector con redes neuronales significa una mejora del modelo en un 2.2%. 




