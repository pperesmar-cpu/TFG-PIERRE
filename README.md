# 📊 Factores determinantes de la incidencia de tumores en España

Este repositorio contiene el código, notebooks y datasets utilizados en el Trabajo de Fin de Grado **“Factores determinantes de la incidencia de tumores en España”**.

El objetivo del proyecto es analizar cómo factores **demográficos, socioeconómicos y ambientales** influyen en la incidencia de tumores en las diferentes comunidades autónomas de España, utilizando técnicas de **ingeniería del dato, análisis exploratorio y machine learning**.

---

## 📁 Estructura del repositorio

```bash
.
├── DATOS_TFG.zip                    # Datos originales extraídos
├── DATOS_TFG_limpios.zip            # Datos procesados y listos para modelado
├── ETL.ipynb                     # Pipeline ETL: limpieza, transformación e imputación
├── IngenieriaAnalisisDato.ipynb  # Análisis exploratorio, modelado y evaluación
├── README.md
```
---

## ⚙️ Descripción del proyecto

El flujo de trabajo se divide en **dos grandes fases**:

### 🧹 1) Ingeniería del dato (`ETL.ipynb` e `IngenieriaAnalisisDato.ipynb`)
En esta fase se realiza:

- Carga de archivos CSV
- Homogeneización de nombres de comunidades autónomas
- Limpieza de columnas irrelevantes
- Unión de datasets en un único dataset maestro
- Detección y eliminación de outliers
- Imputación de valores faltantes con **KNNImputer**
- Validación estadística de la imputación
- Análisis exploratorio de variables
- Matriz de correlación
- Boxplots y análisis temporal
- 
### 🤖 2) Análisis y modelado (`IngenieriaAnalisisDato.ipynb`)
Incluye:

- División **train/test**
- Preprocesamiento:
  - One Hot Encoding
  - Escalado de variables
- Entrenamiento de modelos:
  - Árbol de regresión
  - Random Forest
  - XGBoost
- Optimización con **GridSearchCV**
- Evaluación de métricas
- Análisis de importancia de variables

---
## ▶️ Cómo ejecutar el proyecto

Para ejecutar correctamente el proyecto se recomienda utilizar **Google Colab**, ya que los notebooks han sido desarrollados y probados en este entorno.

### 📂 1) Subir los archivos a Google Drive
Sube al mismo directorio de tu Google Drive:

- la carpeta `DATOS_TFG`
- la carpeta `DATOS_TFG_limpios`
- el notebook `ETL.ipynb`
- el notebook `IngenieriaAnalisisDato.ipynb`

Es importante **mantener la estructura de carpetas**, ya que los notebooks acceden a los archivos mediante rutas relativas.

### ☁️ 2) Abrir los notebooks en Google Colab
Haz clic derecho sobre cada notebook en Google Drive y selecciona:

**Abrir con → Google Colaboratory**

Sigue este orden de ejecución:

1. `ETL.ipynb`
2. `IngenieriaAnalisisDato.ipynb`

### ▶️ 3) Ejecutar todas las celdas
Una vez abierto cada notebook en Colab:

- ve al menú **Entorno de ejecución**
- selecciona **Ejecutar todo**

Después de autorizar el acceso a google drive, el notebook podrá leer automáticamente las carpetas de datos.
