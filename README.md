# 🌱 Fertilizer Recommendation Challenge – Kaggle Playground Series S5E6

Este proyecto forma parte de la competición **[Kaggle Playground Series - Season 5, Episode 6](https://www.kaggle.com/competitions/playground-series-s5e6)**, cuyo objetivo es predecir el tipo de fertilizante más adecuado para un cultivo, a partir de información del suelo, el tipo de cultivo y otras variables numéricas.

El reto consiste en recomendar las **3 opciones más probables** para cada registro, optimizando la métrica **MAP@3 (Mean Average Precision at 3)**.

---

## 📂 Estructura del Proyecto


---

## 🚀 Flujo de Trabajo

1. **Carga de datos**:  
   - `train.csv`, `test.csv`, `sample_submission.csv` desde el dataset oficial de Kaggle.
   
2. **Análisis Exploratorio de Datos (EDA)**:  
   - Verificación de valores nulos.  
   - Distribución de categorías (`Fertilizer Name`, `Soil Type`, `Crop Type`).  
   - Estadísticas descriptivas.

3. **Preprocesamiento**:  
   - *One-Hot Encoding* de variables categóricas (`Soil Type`, `Crop Type`).  
   - Alineación de columnas entre train y test para evitar desajustes.

4. **División del conjunto de datos**:  
   - Train/Test Split estratificado para mantener la proporción de clases.

5. **Entrenamiento del modelo**:  
   - `LightGBMClassifier` con parámetros iniciales.
   
6. **Evaluación**:  
   - Cálculo de **MAP@3** en el conjunto de validación.
   
7. **Generación de predicciones**:  
   - Obtención de las 3 clases más probables por muestra.
   - Creación de `submission.csv` listo para Kaggle.

---

## 📏 Métrica

La métrica usada en la competición es:

**Mean Average Precision at 3 (MAP@3)**  
Evalúa si las predicciones correctas están dentro de las 3 primeras recomendaciones para cada observación, ponderando su posición.

---

## 🛠️ Tecnologías Usadas

- **Lenguajes**: Python  
- **Librerías**: pandas, numpy, scikit-learn, lightgbm  
- **Entorno**: Jupyter Notebook (Kaggle Kernels)  
- **Métrica**: MAP@3  

---

## 📊 Ejemplo de Salida (`submission.csv`)

| id   | Fertilizer Name          |
|------|--------------------------|
| 0    | Fertilizer_A Fertilizer_C Fertilizer_D |
| 1    | Fertilizer_B Fertilizer_A Fertilizer_E |

---

## 📌 Notas

- El modelo inicial usa parámetros por defecto en LightGBM.  
- El flujo puede mejorarse ajustando hiperparámetros y realizando ingeniería de características más profunda.

---

## 📬 Autor

**Jorge Leonardo Loreto**  
[LinkedIn](https://www.linkedin.com/in/jorge-loreto) • [GitHub](https://github.com/jorge-loreto)

