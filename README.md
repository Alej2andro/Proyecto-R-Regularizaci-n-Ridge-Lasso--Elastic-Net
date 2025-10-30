# ☀️ Predicción de Radiación Solar en Sector La Puntilla, Pichilemu con Machine Learning | Proyecto Elastic Net

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org/)
[![RStudio](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=rstudio&logoColor=white)](https://posit.co/products/open-source/rstudio/)
[![Machine Learning](https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://github.com/)

> **Análisis predictivo completo de radiación solar en Pichilemu utilizando métodos de regularización avanzados (Ridge, Lasso, Elastic Net) sobre datos satelitales NASA POWER**

---

## 🎯 Resumen Ejecutivo

Desarrollo de modelo predictivo que alcanza **96% de precisión (R²=0.96)** en estimación de radiación solar utilizando 17 variables meteorológicas. El proyecto demuestra dominio completo del flujo de ciencia de datos: desde preprocesamiento riguroso hasta validación estadística exhaustiva.

### 📊 Resultados Clave

| Métrica | Valor | Interpretación |
|---------|-------|----------------|
| **R² Test** | 0.9604 | Explica 96% de varianza en radiación solar |
| **RMSE** | 0.19 | Error promedio en escala estandarizada |
| **Mejora vs Baseline** | +95.8 pp | Reducción del 79.4% en error predictivo |
| **Hiperparámetros Óptimos** | α=0.10, λ=0.000886 | Balance entre selección y estabilidad |

---

## 🔗 Visualiza el Proyecto Completo

### 📄 [**Haz clic aquí para ver el análisis interactivo en HTML**](https://alej2andro.github.io/Proyecto-R-Regularizaci-n-Ridge-Lasso--Elastic-Net/)
### 👉 [Haz clic aquí para ver el análisis en formato HTML](https://alejzandro.github.io/Proyecto-R-Regularizaci-n-Ridge-Lasso-Elastic-Net/)

El informe incluye:
- 🗺️ Mapas interactivos con Leaflet
- 📈 Visualizaciones avanzadas con ggplot2
- 🔍 Análisis de correlaciones y distribuciones
- ✅ Validación de supuestos estadísticos
- 📊 Comparación exhaustiva de modelos

---

## 🛠️ Stack Tecnológico
```r
# Lenguaje y Entorno
R 4.5.1 | RStudio | R Markdown

# Machine Learning
glmnet      # Ridge/Lasso/Elastic Net
caret       # Validación cruzada y tuning

# Manipulación de Datos
dplyr, tidyr, tibble

# Visualización
ggplot2, ggcorrplot, leaflet

# Diagnóstico Estadístico
lmtest      # Breusch-Pagan, Durbin-Watson
moments     # Asimetría, curtosis
```

---

## 📁 Estructura del Proyecto
```
📦 Proyecto-R-Regularización-Ridge-Lasso-Elastic-Net/
│
├── 📄 Proyecto1R.Rmd                    # Análisis completo en R Markdown
├── 📄 Proyecto1R.html                   # Informe interactivo generado
├── 📊 Meteorologia_sector_la_puntilla_pichilemu.csv  # Dataset NASA POWER
│
├── 📸 Visualizaciones/
│   ├── panel_climatico.png              # Correlaciones clave
│   ├── validacion_cruzada.png           # Curva MSE vs λ
│   ├── radar_top10_variables.png        # Importancia de features
│   └── diagnostico_residuos.png         # QQ-plot, histograma, boxplot
│
└── 📝 README.md                         # Este archivo
```

---

## 🚀 Metodología

### 1️⃣ **Preprocesamiento Riguroso**
- ✅ Detección y conservación de 63 outliers meteorológicos extremos
- ✅ Tratamiento de valores faltantes (-999 → NA)
- ✅ Estandarización z-score para penalizaciones L1/L2

### 2️⃣ **Modelado Predictivo**
```r
# Optimización de hiperparámetros
Grid Search: 11 valores de α × 100 valores de λ
Validación Cruzada: 10-fold CV
Criterio: λ_min (máxima precisión)
```

### 3️⃣ **Comparación de Métodos**
| Método | α | R² Test | Variables Activas | Fortaleza |
|--------|---|---------|-------------------|-----------|
| Ridge | 0.0 | 0.9468 | 17/17 | Estabilidad ante colinealidad |
| Lasso | 1.0 | 0.9447 | 15/17 | Selección automática |
| **Elastic Net** | **0.1** | **0.9604** | **17/17** | **Balance óptimo** |

### 4️⃣ **Validación Estadística**
- ✅ **Normalidad**: Shapiro-Wilk + QQ-plot
- ✅ **Homocedasticidad**: Test Breusch-Pagan (p=0.1193)
- ✅ **Independencia**: Durbin-Watson + Ljung-Box (p=0.3524)

---

## 📈 Hallazgos Clave

### 🔥 Top 5 Variables Predictoras

| Variable | Ponderación | Interpretación Física |
|----------|-------------|----------------------|
| **Temperatura máx 2m** | 10.0 | Respuesta térmica directa a radiación |
| **Temperatura máx superficie** | 7.9 | Energía absorbida por el suelo |
| **Temperatura 2m** | 6.4 | Estado térmico atmosférico |
| **Temperatura húmeda** | 4.9 | Integra calor sensible + humedad |
| **Radiación directa normal** | 4.3 | Componente sin dispersión atmosférica |

### 🎯 Correlaciones Validadas Físicamente
```r
Radiación Solar ↔ Temperatura Máx:  r = 0.84  (R² = 71%)
Radiación Solar ↔ Humedad Relativa: r = -0.84 (anticorrelación)
```

---

## 💡 Competencias Demostradas

### 🧠 Habilidades Técnicas
- [x] **Machine Learning**: Regularización L1/L2, optimización de hiperparámetros
- [x] **Estadística Avanzada**: Validación de supuestos, inferencia, pruebas de hipótesis
- [x] **Programación en R**: Código modular, reproducible y documentado
- [x] **Visualización de Datos**: Dashboards interactivos con Leaflet/ggplot2
- [x] **Comunicación**: Reportes ejecutivos y documentación técnica

### 🎓 Fundamentos Aplicados
```r
Teoría ↔ Práctica:
- Álgebra lineal → Penalizaciones matriciales (λI)
- Cálculo → Descenso de gradiente coordinado
- Estadística → Intervalos de confianza, p-valores
- Física atmosférica → Validación de coherencia meteorológica
```

---

## 🎬 Cómo Reproducir el Análisis

### 📋 Requisitos Previos
```r
# 1. Instalar R (≥ 4.0) y RStudio
# 2. Clonar repositorio
git clone https://github.com/Alej2andro/Proyecto-R-Regularizaci-n-Ridge-Lasso--Elastic-Net.git

# 3. Instalar dependencias
install.packages(c("glmnet", "caret", "ggplot2", "dplyr", "leaflet", "lmtest"))
```

### ▶️ Ejecución
```r
# Opción 1: Abrir en RStudio
# Archivo → Abrir → Proyecto1R.Rmd → Knit to HTML

# Opción 2: Línea de comandos
rmarkdown::render("Proyecto1R.Rmd")
```

---

## 📚 Referencias Técnicas

- **Hastie, T., Tibshirani, R., & Friedman, J. (2009)** - *The Elements of Statistical Learning* (Fundamentos de regularización)
- **Friedman et al. (2010)** - Paquete `glmnet` para R
- **Gujarati, D. N. & Porter, D. C. (2010)** - *Econometría* (Diagnóstico de supuestos)
- **NASA POWER Project** - Datos satelitales MERRA-2 (https://power.larc.nasa.gov/)

---

## 👨‍💼 Sobre el Autor

**Alejandro Figueroa Rojas**  
*Analista de Datos | Ingeniero Comercial*

📧 contacto.figueroarejas.a@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/alejandro-figueroa-rojas-2052b6218)  
📂 [GitHub](https://github.com/Alej2andro)

### 🎯 ¿Por qué este proyecto?
Este análisis demuestra:
1. **Rigor metodológico** en cada fase del pipeline de datos
2. **Pensamiento crítico** al conservar outliers meteorológicos reales
3. **Transparencia científica** al documentar limitaciones (resolución satelital ~50km)
4. **Equilibrio** entre profundidad técnica y comunicación clara

---

## 📝 Licencia

Este proyecto es de código abierto bajo licencia MIT. Se invita a la comunidad a replicar, validar y mejorar el análisis.

---

## ⭐ ¿Te resultó útil?

Si este proyecto te pareció valioso:
- 🌟 Dale una estrella al repositorio
- 🔄 Comparte con colegas interesados en ciencia de datos
- 💬 Abre un issue para sugerencias o colaboraciones

---

<div align="center">

**Construido con ❤️ usando R, pasión por los datos y café ☕**

[Ver Análisis Completo](https://alej2andro.github.io/Proyecto-R-Regularizaci-n-Ridge-Lasso--Elastic-Net/) | [Reportar Issue](https://github.com/Alej2andro/Proyecto-R-Regularizaci-n-Ridge-Lasso--Elastic-Net/issues) | [Contactar](mailto:contacto.figueroarejas.a@gmail.com)

</div>
