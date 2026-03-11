# TelecomX-Latam_parte2

# Descripción:
Este informe final detalla el proceso completo de análisis para predecir el abandono de clientes (Churn) en TelecomX, desde la preparación de los datos hasta la evaluación de modelos y las conclusiones estratégicas.

# Tecnologías usadas

. Lenguaje: Python 3.12

. Manipulación de datos: random forest, panda, matplotlib, seaborn, numpy

. Entorno: Google Colab

# Analisis de correlación y visualización

- Correlación con Churn:
Se realizó un análisis de correlación para identificar las variables más influyentes en el abandono. Las variables con mayor correlación positiva con 'Churn' fueron:

. InternetService_Fiber optic

. PaymentMethod_Electronic check

. Monthly (Cargos Mensuales)

. PaperlessBilling_Yes

. SeniorCitizen

Las variables con mayor correlación negativa (que indican una menor probabilidad de Churn) fueron:

. tenure (Antigüedad)

. Contract_Two year

# Entrenamiento y Evaluación de Modelos
Se dividieron los datos balanceados (X_res, y_res) en conjuntos de entrenamiento (80%) y prueba (20%).

a. Regresión Logística:
Preprocesamiento: Se aplicó StandardScaler a las variables predictoras (X_train, X_test) debido a la sensibilidad de la Regresión Logística a la escala de las características.

Resultados:

. Accuracy: 0.8309

. Precision: 0.8427

. Recall (Sensibilidad): 0.8169

. F1-Score: 0.8296

b. Random Forest:
Preprocesamiento: No requiere escalado, por lo que se usaron los datos originales (sin escalar) para el entrenamiento.

Resultados:

. Accuracy: 0.8531

. Precision: 0.8570

. Recall (Sensibilidad): 0.8504

. F1-Score: 0.8537

Comparación:
El modelo Random Forest superó ligeramente a la Regresión Logística en todas las métricas de evaluación, demostrando una mayor capacidad para capturar las relaciones complejas en los datos.

# Interpretación y Conclusión Estratégica
El modelo Random Forest, al ser el de mejor desempeño, se utilizó para identificar los factores más influyentes en el abandono de clientes:

Top 10 Factores que influyen en la Cancelación (Random Forest):

. Total (Gasto Total)

. tenure (Antigüedad del Cliente)

. Monthly (Cargos Mensuales)

. PaymentMethod_Electronic check (Método de Pago: Cheque Electrónico)

. InternetService_Fiber optic (Servicio de Internet: Fibra Óptica)

. Contract_Two year (Contrato: Dos Años)

. PaperlessBilling_Yes (Facturación Electrónica)

. gender_Male (Género Masculino)

. Contract_One year (Contrato: Un Año)

. Partner_Yes (Tiene Pareja)

# Visualizaciones destacadas

. Top 10 factores que influyen en la cancelación (random forest)
<img width="1229" height="611" alt="image" src="https://github.com/user-attachments/assets/cd580298-b3b5-413d-ac30-53d367f29a33" />

. Matriz de confusión - Regresión logistica
<img width="660" height="544" alt="image" src="https://github.com/user-attachments/assets/53cc0ce4-ba4a-4ff9-8ae8-3fb1e16d0cf6" />

. Matriz de confusión - Random forest
<img width="670" height="546" alt="image" src="https://github.com/user-attachments/assets/d5114e26-2288-4d5e-94af-132f14f00998" />

# Como ejecutar el proyecto
Clona este repositorio:
https://github.com/Mayra-25/TelecomX-Latam_parte2.git
