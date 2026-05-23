# 📈 Financial Market Analysis · Python Portfolio Project

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat-square&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Interactive-3D4CB?style=flat-square&logo=plotly&logoColor=white)
![JupyterLab](https://img.shields.io/badge/JupyterLab-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

> Análisis cuantitativo de activos financieros con simulación Monte Carlo, optimización de portafolios y visualizaciones interactivas.

---

## 🎯 ¿De qué trata este proyecto?

Este notebook explora el rendimiento histórico de **5 activos** (AAPL, GOOGL, MSFT, AMZN, BTC) a lo largo de 2 años de trading, aplicando técnicas de análisis cuantitativo para identificar el portafolio de máximo Sharpe Ratio mediante simulación Monte Carlo.

**Ideal para:** Data Analysts, Financial Analysts, y cualquier persona que quiera mostrar skills de Python aplicados a finanzas.

---

## 📊 Visualizaciones incluidas

| # | Análisis | Descripción |
|---|----------|-------------|
| 1 | **Retorno Acumulado** | Evolución temporal de cada activo (2022–2024) |
| 2 | **Frontera Eficiente** | 5,000 portafolios simulados con Monte Carlo |
| 3 | **Matriz de Correlación** | Heatmap de correlaciones entre activos |
| 4 | **Dashboard Ejecutivo** | 4 paneles: riesgo/retorno, Sharpe, distribuciones, precios normalizados |

---

## 🛠️ Stack Tecnológico

```
pandas      → manipulación y análisis de datos
numpy       → cálculos estadísticos y simulaciones
plotly      → visualizaciones interactivas
scipy       → distribuciones estadísticas
jupyterlab  → entorno de desarrollo
```

---

## 🚀 Instalación y uso

### 1. Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/financial-analysis-portfolio.git
cd financial-analysis-portfolio
```

### 2. Instalar dependencias
```bash
pip install pandas numpy plotly scipy jupyterlab
```

### 3. Abrir en JupyterLab
```bash
jupyter lab
```

Luego abrir `analisis_financiero_portfolio.ipynb` y ejecutar todas las celdas (`Run → Run All Cells`).

---

## 📐 Métricas calculadas

- **Retorno Anual (%)** — retorno promedio anualizado
- **Volatilidad Anual (%)** — desviación estándar anualizada
- **Sharpe Ratio** — retorno ajustado por riesgo
- **Maximum Drawdown (%)** — caída máxima desde el pico
- **Retorno Total (%)** — ganancia/pérdida acumulada del período

---

## 🎲 Simulación Monte Carlo

Se generaron **5,000 portafolios aleatorios** con pesos distribuidos mediante distribución de Dirichlet, permitiendo trazar la frontera eficiente y encontrar la combinación óptima de activos que maximiza el **Sharpe Ratio**.

```python
# Ejemplo del núcleo de la simulación
for _ in range(5000):
    pesos = np.random.dirichlet(np.ones(n_activos))
    retorno = np.dot(pesos, retornos_medios) * 252
    volatilidad = np.sqrt(pesos @ matriz_covarianza @ pesos)
    sharpe = retorno / volatilidad
```

---

## 💡 Hallazgos principales

- **MSFT** presentó el mejor balance riesgo/retorno entre las acciones tecnológicas
- **BTC** ofreció los mayores retornos potenciales con volatilidad ~3x superior al promedio de acciones
- La correlación entre acciones tech fue alta (>0.6), sugiriendo **menor beneficio de diversificación** dentro del mismo sector
- El portafolio óptimo tendió a **sobreponderar activos de baja volatilidad** como ancla de estabilidad

---

## 📁 Estructura del proyecto

```
📦 financial-analysis-portfolio
 ┣ 📓 analisis_financiero_portfolio.ipynb   ← Notebook principal
 ┣ 📄 README.md                             ← Este archivo
 ┗ 📄 requirements.txt                      ← Dependencias
```

---

## 📋 requirements.txt

```
pandas>=2.0.0
numpy>=1.24.0
plotly>=5.15.0
scipy>=1.11.0
jupyterlab>=4.0.0
```

---

## ⚠️ Disclaimer

Este proyecto es con **fines educativos y de portfolio profesional**. Los datos son simulados con parámetros estadísticos reales. No constituye asesoramiento financiero ni recomendación de inversión.

---

## 👤 Autor

**[Tu Nombre]**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/tu-perfil)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/tu-usuario)

---

## 📝 Licencia

MIT © 2024 — libre para usar, modificar y compartir con atribución.
