# 📊 Dataset: Telco Customer Churn

## Descripción

Dataset público de IBM Watson Analytics sobre churn en telecomunicaciones.

## Fuente

**URL de descarga automática:**
```
https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv
```

El notebook descarga automáticamente el dataset. **No es necesario descargarlo manualmente.**

## Características del Dataset

- **Tamaño:** 7,043 registros × 21 variables
- **Tipo:** Datos tabulares
- **Target:** Churn (Yes/No)

### Variables

**Demográficas:**
- customerID
- gender
- SeniorCitizen
- Partner
- Dependents

**Servicios:**
- PhoneService, MultipleLines
- InternetService
- OnlineSecurity, OnlineBackup
- DeviceProtection, TechSupport
- StreamingTV, StreamingMovies

**Cuenta:**
- tenure (meses como cliente)
- Contract (tipo de contrato)
- PaperlessBilling
- PaymentMethod
- MonthlyCharges
- TotalCharges

**Target:**
- Churn (Yes/No)

## Uso

El notebook maneja automáticamente la descarga y carga:
```python
url = 'https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv'
df = pd.read_csv(url)
```

## Licencia

Dataset público de IBM para propósitos educativos y de investigación.
```
