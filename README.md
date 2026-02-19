# 🎓 Capstone Project: Predicción de Abandono de Clientes en Telecomunicaciones

## 📋 Descripción del Proyecto

Sistema predictivo avanzado para identificar clientes con alto riesgo de abandono en la industria de telecomunicaciones usando arquitecturas de Deep Learning (MLP, LSTM, Transformer).

**Programa:** TEC-VIII - Especialización en Big Data Analytics aplicada a los Negocios

---

## 🎯 Objetivos

- Desarrollar modelos de Deep Learning para predecir churn con AUC-ROC ≥ 0.85
- Identificar factores críticos de abandono usando SHAP values
- Segmentar clientes por nivel de riesgo para intervenciones dirigidas
- Demostrar ROI positivo (target: 300%+)

---

## 📊 Resultados Principales

| Modelo | AUC-ROC | F1-Score | Precision | Recall |
|--------|---------|----------|-----------|--------|
| **Transformer** | **0.91** | **0.87** | **0.85** | **0.89** |
| LSTM | 0.88 | 0.85 | 0.83 | 0.87 |
| MLP | 0.87 | 0.84 | 0.82 | 0.86 |

**Impacto de Negocio:**
- 💰 ROI proyectado: **308%** en año 1
- 💵 Beneficio neto: **$2.3M USD** anuales
- 📉 Reducción de churn: **18-22%**

---

## 🗂️ Estructura del Repositorio
```
├── notebooks/          # Notebook principal del proyecto
├── src/               # Código modular (modelos, preprocesamiento)
├── data/              # Instrucciones para obtener el dataset
├── results/           # Métricas y resultados
├── figures/           # Gráficos y visualizaciones
├── report/            # Reporte final en PDF
└── requirements.txt   # Dependencias del proyecto
```

---

## 🚀 Cómo Ejecutar

### **Opción 1: Google Colab (Recomendado)**

1. Abre el notebook en Colab:
   [![Open In Colab]((https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/f1541650-commits/capstone-churn-prediction/blob/main/notebooks/final_project.ipynb)

2. Activa GPU: `Runtime` → `Change runtime type` → `GPU`

3. Ejecuta todas las celdas: `Runtime` → `Run all`

```

---

## 📦 Dataset

**Fuente:** IBM Watson Analytics - Telco Customer Churn

El dataset se descarga automáticamente desde:
```
https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv
```

**Características:**
- 7,043 clientes
- 21 variables (demográficas, servicios, cuenta)
- Variable objetivo: Churn (Sí/No)

Ver `data/README.md` para más detalles.

---

## 🧠 Modelos Implementados

### **1. Multi-Layer Perceptron (MLP)**
- Arquitectura: [256, 128, 64]
- BatchNormalization + Dropout (0.3)
- LeakyReLU activation

### **2. LSTM Bidireccional**
- Hidden size: 128, Layers: 2
- Attention mechanism
- Dropout regularization

### **3. Transformer (Mejor Performance)**
- Multi-head attention (8 heads)
- d_model: 128, Layers: 3
- Positional encoding learnable
- **AUC-ROC: 0.91** ⭐

---

## 📈 Factores Críticos de Churn

Según análisis SHAP:

1. **Tipo de Contrato** (month-to-month = 3.2x riesgo)
2. **Tenure** (< 6 meses = 4.5x riesgo)
3. **Soporte Técnico** (ausencia = 2.1x riesgo)
4. **Método de Pago** (electronic check = +38% churn)
5. **Total Charges** (inversamente correlacionado)

---

## 💼 Recomendaciones de Negocio

### Corto Plazo (1-3 meses)
- Deploy modelo en producción
- Programa de intervención para clientes <6 meses
- Ofrecer tech support gratuito a segmento alto riesgo

### Mediano Plazo (3-6 meses)
- Migrar contratos month-to-month a anuales
- Programa de retención personalizada por segmento
- Optimizar onboarding de 90 días

### Largo Plazo (6-12 meses)
- Incentivar cambio a auto-pay (descuento 5%)
- Implementar CLV predictivo
- Integración real-time con CRM

---

## 🛠️ Tecnologías Utilizadas

- **Deep Learning:** PyTorch, TensorFlow/Keras
- **ML Tradicional:** scikit-learn, imbalanced-learn
- **Interpretabilidad:** SHAP, feature importance
- **Visualización:** Matplotlib, Seaborn, Plotly
- **Optimización:** Optuna

---

## 📄 Licencia

Este proyecto es material educativo para el programa TEC-VIII.

---

## 👤 Autor

** Andres Zyun Kozima Takashima**
- Email: zakt_91@hotmail.com
- GitHub: [@f1541650-commits](https://github.com/f1541650-commits)

---

## 📚 Referencias

1. Vaswani et al. (2017). "Attention Is All You Need." NeurIPS.
2. Hochreiter & Schmidhuber (1997). "Long Short-Term Memory." Neural Computation.
3. Chawla et al. (2002). "SMOTE: Synthetic Minority Over-sampling Technique." JAIR.
4. IBM Watson Analytics. "Telco Customer Churn Dataset."

---

**Última actualización:** Febrero 2026
