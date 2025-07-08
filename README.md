Este proyecto aplica técnicas de Machine Learning para predecir la calidad del vino basándose en características físico-químicas.

## 🎯 Objetivo

Desarrollar y evaluar modelos de clasificación que puedan predecir la calidad del vino utilizando variables como alcohol, acidez, sulfatos, etc.

## 📊 Dataset

- **Archivo**: `WineQT.csv`
- **Muestras**: 1,143 vinos tintos
- **Características**: 11 variables físico-químicas
- **Variable objetivo**: Calidad del vino (escala 3-8)

### Variables analizadas:
- `fixed_acidity`: Acidez fija
- `volatile_acidity`: Acidez volátil
- `citric_acid`: Ácido cítrico
- `residual_sugar`: Azúcar residual
- `chlorides`: Cloruros
- `free_sulfur_dioxide`: Dióxido de azufre libre
- `total_sulfur_dioxide`: Dióxido de azufre total
- `density`: Densidad
- `ph`: Potencial de hidrógeno
- `sulphates`: Sulfatos
- `alcohol`: Contenido alcohólico

## 🚀 Ejecución

### 1. Análisis Principal
```bash
jupyter notebook Wine_Quality_Classification.ipynb
```

### 2. Generar Informe PDF
```bash
python create_pdf_report.py
```

## 📋 Estructura del Proyecto

```
📁 Estudios-ML/
├── 📓 Wine_Quality_Classification.ipynb   # Notebook principal
├── 📄 WineQT.csv                          # Dataset
├── 🐍 create_pdf_report.py               # Generador de informe
├── 📚 README.md                          # Este archivo
├── 📄 CLAUDE.md                          # Documentación técnica
├── 📊 model_results.csv                  # Resultados (generado)
├── 📊 model_predictions.csv              # Predicciones (generado)
├── 📄 Wine_Quality_Analysis_Report.pdf   # Informe final (generado)
└── 📁 models/                            # Modelos entrenados (generado)
```

## 🤖 Modelos Implementados

1. **K-Nearest Neighbors (KNN)**
   - Optimización de hiperparámetros: n_neighbors, weights, p
   - Preprocesamiento: StandardScaler

2. **Random Forest Classifier**
   - Optimización: n_estimators, max_depth, min_samples_split, min_samples_leaf
   - Mejor rendimiento típico

3. **Regresión Logística**
   - Optimización: C (regularización), penalty, solver
   - Preprocesamiento: StandardScaler

## 📈 Evaluación

### Métricas utilizadas:
- **Accuracy**: Proporción de predicciones correctas
- **Precision**: Precisión por clase
- **Recall**: Sensibilidad por clase
- **F1-Score**: Media armónica de precision y recall
- **Matriz de Confusión**: Análisis detallado de errores
- **Curvas ROC**: Capacidad discriminativa

## 📄 Informe PDF

El script `create_pdf_report.py` genera un informe profesional de 8 páginas con:

1. **Portada**: Resumen del proyecto
2. **Resumen Ejecutivo**: Hallazgos principales
3. **Análisis Exploratorio**: Visualizaciones y estadísticas
4. **Comparación de Modelos**: Métricas y ranking
5. **Matrices de Confusión**: Análisis de errores
6. **Importancia de Características**: Factores clave
7. **Conclusiones**: Recomendaciones y próximos pasos
8. **Apéndice Técnico**: Detalles de implementación

## 🔧 Dependencias

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## 📊 Resultados Esperados

- **Mejor modelo**: Random Forest (típicamente ~65% accuracy)
- **Características clave**: Alcohol, sulfatos, acidez volátil
- **Desafío principal**: Clases desbalanceadas y calidades adyacentes

## 💡 Conclusiones

- Los modelos ensemble superan a los individuales
- La calidad del vino es multifactorial
- Se requiere balanceo de clases para mejor rendimiento
- Potencial aplicación en industria vinícola

## 🎯 Próximos Pasos

1. Implementar técnicas de balanceo (SMOTE)
2. Explorar feature engineering
3. Probar modelos avanzados (XGBoost)
4. Validar con datos de diferentes regiones

---

**Autor**: Proyecto de Machine Learning  
**Fecha**: 2024  
**Tecnologías**: Python, scikit-learn, pandas, matplotlib
