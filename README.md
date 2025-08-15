📊 Date-Science-TelecomX-parte_2-Predicción de Cancelación de Clientes (Churn Prediction)
📌 Descripción

Este proyecto tiene como objetivo predecir la probabilidad de que un cliente cancele sus servicios, utilizando modelos de Machine Learning y análisis exploratorio de datos.
Se trabajó con datos históricos de clientes, aplicando técnicas de limpieza, ingeniería de variables, balanceo de clases y selección de características para optimizar el rendimiento del modelo.

🛠️ Tecnologías y Librerías Utilizadas

Python 3.10+
NumPy — Cálculos numéricos
Pandas — Manipulación de datos
Scikit-learn — Modelado y métricas
Matplotlib y Seaborn — Visualización
XGBoost — Modelos de Gradient Boosting
Imbalanced-learn (SMOTE) — Balanceo de clases
SHAP — Interpretabilidad de modelos

📂 Estructura del Proyecto
├── data/                   # Datos originales y procesados
├── notebooks/              # Jupyter notebooks con el análisis
├── models/                 # Modelos entrenados (archivos .pkl)
├── scripts/                # Scripts de entrenamiento y evaluación
├── README.md               # Este archivo
└── requirements.txt        # Dependencias del proyecto

📊 Flujo de Trabajo

1-Carga y exploración de datos
  Análisis de valores nulos y tipos de datos
  Estadísticas descriptivas y visualizaciones iniciales

2-Preprocesamiento
  Codificación de variables categóricas
  Eliminación de variables con alta multicolinealidad (VIF)
  Balanceo de clases con SMOTE
3-División de datos
  Train (56%), Validación (14%), Test (30%)
  Normalización de variables numéricas
4-Entrenamiento de Modelos
  Regresión Logística
  Árbol de Decisión
  Random Forest
  XGBoost
5-Evaluación de Modelos
  Métricas: Accuracy, Precision, Recall, F1-Score, ROC-AUC, Average Precision
  Matriz de confusión y curva ROC
  Comparación gráfica de modelos
6-Selección del Modelo Final
  Regresión Logística seleccionada por su mejor balance entre recall y ROC-AUC, lo que la hace más efectiva para identificar clientes que probablemente cancelen.

📈 Principales Factores de Cancelación

Basado en el análisis de importancia de variables, los factores más influyentes son:
Cargos Mensuales altos.
Meses de Contrato bajos (clientes nuevos tienden a cancelar más).
Tipo de Contrato (mensual más propenso a cancelación).
Uso de Servicios de Internet (fiber optic asociado a mayor cancelación).
Ausencia de servicios complementarios como soporte técnico o seguridad online.

💡 Estrategias de Retención Propuestas

Ofertas personalizadas a clientes con contrato mensual para migrarlos a planes anuales.
Descuentos escalonados en los primeros meses para nuevos clientes.
Paquetes combinados de servicios complementarios para aumentar fidelización.
Monitoreo proactivo de clientes con cargos mensuales altos para ofrecer alternativas.

🚀 Ejecución del Proyecto

1️⃣ Clonar el repositorio
  git clone https://github.com/Cesar-Solorza/Data-Science-TelecomX_LATAM_parte_2
  cd proyecto-churn
2️⃣ Instalar dependencias
  pip install -r requirements.txt
3️⃣ Entrenar el modelo
  python scripts/train_model.py
4️⃣ Cargar y usar el modelo entrenado
  import joblib
  modelo = joblib.load("models/modelo_evasion_clientes.pkl")
  predicciones = modelo.predict(X_nuevos_clientes)

📜 Licencia

Proyecto de uso educativo y libre, bajo licencia MIT.
  














