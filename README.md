# 📊 DCDDyAA - Trabajo Final Integrador - Grupo U

Proyecto final de la **Diplomatura en Ciencia de Datos y Análisis Avanzado**  
**Predicción de abandono de clientes bancarios (Customer Churn Prediction)**  

---

## 📘 Descripción del Proyecto  

El objetivo del trabajo fue **predecir la probabilidad de abandono (churn)** de clientes de un banco, utilizando un conjunto de datos con información **demográfica, financiera y de comportamiento**.  

Se aplicaron técnicas de **preprocesamiento, balanceo de clases, selección de variables y modelado supervisado**, comparando diversos algoritmos de *Machine Learning* con enfoque interpretativo mediante **SHAP Values**.

---

## ⚙️ Modelos Utilizados

- **Regresión Logística**
- **K-Nearest Neighbors (KNN)**
- **Random Forest**
- **XGBoost**
- **LightGBM**

---

## 🧠 Metodología General

1. **Análisis Exploratorio de Datos (EDA):** identificación de patrones de abandono y correlaciones.  
2. **Tratamiento de Datos:** eliminación de variables irrelevantes, imputación de faltantes y codificación categórica.  
3. **Balanceo de clases:** aplicación de **SMOTE** para corregir el desbalance entre clientes que abandonan y los que permanecen.  
4. **Entrenamiento y validación:** división 80/20 y validación cruzada estratificada (5 folds).  
5. **Evaluación de modelos:** uso de métricas AUC, precisión, recall y F1-score.  
6. **Interpretabilidad:** análisis de importancia global y local con **SHAP Values**.  

---

## 📈 Métricas Principales (AUC Test)

| Modelo                | AUC    | Observaciones |
|-----------------------|--------|----------------|
| **XGBoost**           | 0.9995 | Máxima performance; `Complain` dominante |
| **Regresión Logística** | 0.9988 | Modelo simple, interpretable y robusto |
| **Random Forest**     | 0.9983 | Alta estabilidad y precisión |
| **LightGBM**          | 0.9980 | Mejor balance explicativo |
| **KNN**               | 0.9698 | Resultados correctos pero sensibles al escalado |

---

## 🧾 Principales Conclusiones

- En todos los modelos, la variable **`Complain`** (reclamo registrado) resultó ser el predictor más influyente del abandono.  
- Variables de **engagement** como **`IsActiveMember`**, **`NumOfProducts`** y **`Satisfaction Score`** mostraron un peso importante, especialmente en modelos no lineales.  
- Los valores de **AUC** obtenidos (≈ 0.99) son excepcionalmente altos, lo que sugiere la presencia de variables con fuerte poder discriminatorio.  
  Se recomienda validar con datos reales de una institución bancaria para confirmar la robustez del modelo.  
- Los **SHAP Values** permitieron explicar el impacto global y local de cada variable, destacando que **`Complain`**, **`Age`** e **`IsActiveMember`** son los principales impulsores del abandono.

---

## 🧩 Requisitos y Librerías Utilizadas

El proyecto fue desarrollado en **Python 3.10** utilizando las siguientes librerías principales:

- `pandas`  
- `numpy`  
- `matplotlib`  
- `seaborn`  
- `scikit-learn`  
- `imbalanced-learn`  
- `xgboost`  
- `lightgbm`  
- `shap`  

## 🚀 Ejecución en Google Colab

A continuación se detallan los pasos para ejecutar este proyecto directamente desde Google Colab 👇

## 🔹 1. Clonar el repositorio
!git clone https://github.com/L07IA/DCDDyAA-Trabajo-Final-Integrador-GrupoU.git

%cd DCDDyAA-Trabajo-Final-Integrador-GrupoU

## 🔹 2. Verificar archivos del proyecto
import os

print(os.listdir())

## 🔹 3. Instalar dependencias
!pip install -r requirements.txt

## 🔹 4. (Opcional) Montar Google Drive

Si deseás guardar resultados o el notebook ejecutado:

from google.colab import drive

drive.mount('/content/drive')

## 🔹 5. Ejecutar el notebook completo

Esto correrá todas las celdas del notebook automáticamente y generará un archivo con los resultados:

!jupyter nbconvert --to notebook --execute DCDDyAA_TrabajoFinalIntegrador_Grupo_U.ipynb \

  --ExecutePreprocessor.timeout=1200 \
  
  --output DCDDyAA_TrabajoFinalIntegrador_Grupo_U.executed.ipynb

## 🔹 6. Abrir el proyecto en Colab

También podés abrirlo manualmente desde:

👉 https://colab.research.google.com/github/L07IA/DCDDyAA-Trabajo-Final-Integrador-GrupoU

O directamente con este botón:


## 🔹 7. Ejecutar todo

Una vez abierto el cuaderno, seleccioná:
➡️ Entorno de ejecución → Ejecutar todo

## 🧾 Resultado final

Se generará un nuevo notebook ejecutado:

DCDDyAA_TrabajoFinalIntegrador_Grupo_U.executed.ipynb


que contendrá todos los outputs, métricas y gráficos del proyecto.



 ## 👨‍💻 Autor

Leandro Toledo
leandro.toledo93@email.com

📅 Octubre 2025
