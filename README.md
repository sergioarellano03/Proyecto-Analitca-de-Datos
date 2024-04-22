# COLEGIO DE CIENCIAS E INGENIERIA

# INGENIERIA INDUSTRIAL

### IIN-3007

### NRC: 2209

### Avance 1 Proyecto

### SEMESTRE: Segundo Semestre 2023-2024 (202320)

### NOMBRE(S) Y CÓDIGO DE ESTUDIANTE(S): 
### Ignacio Castillo 00326465

### Sergio Arellano 00325565

### PROFESORA: 
### María Gabriela Baldeón Calisto

### FECHA DE ENTREGA: 03-04-2024

#### Descripción del proyecto:

El proyecto consiste en el desarrollo de un modelo que sirva para la predicción de si la probabilidad de un paciente de tener una ataque cerebral es alta o baja. Para esto se ha recibido una base de datos de un hospital público con información anónima. En la base de datos se encuentran 12 variables predictivas que describen el estado socio-demográfico y médico del paciente. Además, presenta una variable de respuesta que indica si el paciente ha sufrido o no un ataque cerebral.
A través de el código presentado a continuación se ha seguido una proceso para crear y encontrar este modelo. En primer lugar, se ha analizado la base de datos obtenida para asegurar su integridad. Se encontraron valores nulos en algunas variables predictivas y los registros con esta información faltante se han eliminado. También, se encontraron registros con valores inconsistentes con la información, estos registros fueron evaluados y la información fue corregida dentro de las posibilidades o se eliminaron los registros si no se podía corregir.
El siguiente paso fue analizar la distribución de las variables predictivas, su correlación y la distribución de la variable de respuesta. Aquí se encontró que la distribución de la variable de respuesta estaba muy desbalanceada. Esto podía ser un problema en cuanto al desarrollo del modelo de predicción. Por esto, se realizó un análisis de la mejor estrategia para sortear este problema entre el oversampling y el undersampling. Se dividieron los datos en particiones de entrenamiento, validación y prueba con una distribución de 70/15/15. No se encontraron diferencias estadísticamente significativas entre estas herramientas, por lo que basado en otras métricas como la precisión o la sensibilidad se eligió utilizar el método de undersampling para el desarrollo del modelo. 
A continuación, se entrenaron cuatro modelos predictivos con diferentes algoritmos detrás. Se realizaron modelos con Random Forest, Regresión Logística, Naive Bayes y Gradient Boosting. Al revisar los rendimientos de los modelos en los sets de entrenamiento, validación y prueba se decidió utilizar el modelo que utilizó Random Forest debido a su alta sensibilidad y su rendimiento consistente en las tres particiones de datos. Se decidió que la sensibilidad sea la métrica de evaluación decisiva para minimizar los falsos negativos que serían catastróficos al momento de predecir la probabilidad del paciente de sufrir un ataque cerebral. 
Se encontraron también las variables predictivas más importantes a través del modelo de Random Forest. Se seleccionaron las 7 más importantes que fueron la edad, el nivel promedio de glucosa, los ingresos, el BMI, si se trabaja con niños, si el paciente sufre de hipertensión y el número de hijos.
