# Detección Inteligente de Arritmias con Datos de ECG y Aprendizaje Automático - Ejercicios de Feedback 2
---
Máster en Inteligencia Artificial - Matemáticas y Estadística para la IA

Autor: Tania Évora Vargas Martínez

## 1. Descripción del proyecto
Este proyecto presenta un sistema de clasificación supervisada para la **detección de latidos cardíacos anómalos** a partir de señales ECG (electrocardiograma). El objetivo es distinguir entre latidos normales y arritmias, con aplicación en sistemas de monitorización mediante dispositivos wearables.

El análisis incluye:
- **Exploración de datos (EDA)**: Análisis estadístico descriptivo de las 5 clases de latidos
- **Reducción de dimensionalidad (PCA)**: Visualización y análisis de componentes principales
- **Modelos de clasificación**: Comparativa de Regresión Logística, Árbol de Decisión, Naive Bayes y Red Neuronal (MLP)
- **Teorema de Bayes**: Aplicación de probabilidades condicionales para estimar la probabilidad de anomalía

## 2. Estructura de directorios
El proyecto se organiza en las siguientes carpetas. Para la correcta ejecución, se recomienda mantener esta estructura:

```
.
├── README.txt
│
├── notebook/
│   └── Feedback_ECG_VargasMartinez_TaniaEvora.ipynb
│
├── informe/
│   └── informe.pdf
│
└── MEIA_P2_Enunciado.pdf
```

## 3. Dataset

Se utiliza el **ECG Heartbeat Categorization Dataset** de Kaggle, que contiene señales ECG segmentadas en latidos individuales:
- **187 características**: Valores de amplitud de la señal ECG muestreada a 125 Hz
- **5 clases originales**: Normal (N), Supraventricular (S), Ventricular (V), Fusión (F), Ruido (Q)
- **Clasificación binaria**: Normal vs Anómalo (agrupando las 4 clases de arritmias)

## 4. Librerías Necesarias

```python
# Librerías básicas
numpy
pandas

# Visualización
matplotlib
seaborn

# Machine Learning
scikit-learn

# Estadística
scipy
```

### Instalación

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy
```

## Resultados Principales

| Modelo | Accuracy | Precision | Recall | F1-Score |
|--------|----------|-----------|--------|----------|
| Regresión Logística | 91% | 85% | 55% | 67% |
| Árbol de Decisión | 96% | 89% | 89% | 89% |
| Naive Bayes | 81% | 45% | 49% | 47% |
| **Red Neuronal (MLP)** | **98%** | **97%** | **90%** | **94%** |

La **Red Neuronal (MLP)** obtiene los mejores resultados, siendo el modelo recomendado para sistemas de monitorización clínica donde la detección de arritmias es crítica.
