# 📡 TelecomX – Análisis de Evasión de Clientes (Churn)

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**Challenge de Data Science | Análisis exploratorio del churn en una empresa de telecomunicaciones**

</div>

---

## 🎯 Objetivo

TelecomX enfrenta una tasa de cancelación de clientes que compromete su sostenibilidad comercial. Este proyecto tiene como objetivo **identificar los factores que llevan a un cliente a abandonar el servicio (churn)**, a través de un proceso completo de ETL y análisis exploratorio de datos (EDA), que sirva como base para futuros modelos predictivos y decisiones estratégicas de retención.

---

## 📁 Estructura del Repositorio

```
Challenge-Telecom-X-Latam/
│
├── TelecomX_LATAM.ipynb            # Notebook principal con todo el análisis
├── README.md                        # Este archivo

```

---

## 🔄 Metodología: Pipeline ETL + EDA

### 📌 Extracción y Limpieza

- Normalización de columnas anidadas: `customer`, `phone`, `internet`, `account`
- Consolidación en un único DataFrame (`df_final`)
- Traducción y renombrado estratégico de columnas al español
- Verificación y tratamiento de valores nulos y registros duplicados
- Corrección de inconsistencias en categorías

### 🔧 Transformación

- Estandarización binaria (0 y 1) de variables categóricas tipo Sí/No
- Creación de la variable derivada **`cuentas_diarias`** (cobro mensual ÷ 30)
- Transformación completa de columnas de texto a formato numérico

### 📊 Carga y Análisis

- Resumen estadístico general con `.describe()`
- Análisis comparativo por grupo de evasión (`groupby`)
- Análisis de variables categóricas y numéricas
- Cálculo de correlaciones de Pearson con la variable objetivo

---

## 📈 Visualizaciones Generadas

| # | Gráfico | Tipo |
|---|---------|------|
| 1 | Distribución de la variable Evasión | Dona + Barras |
| 2a | Evasión por Tipo de Contrato | Barras + Dona |
| 2b | Servicios y Perfil Demográfico por grupo | Barras agrupadas |
| 2c | Correlación de variables con la Evasión | Barras horizontales |
| 3a | Distribución de variables numéricas por grupo | KDE (densidad) |
| 3b | Comparación de variables numéricas | Boxplots |

---

## 🔍 Principales Hallazgos

- 📌 **26.6% de los clientes se dan de baja** — 1 de cada 4 clientes abandona el servicio.
- 📌 **El contrato mes a mes** concentra una tasa de evasión del ~43%, frente al 3% de los contratos bianuales.
- 📌 **Los primeros 18 meses** son el período crítico: la mayoría de los evasores se va antes de consolidar su relación con la empresa.
- 📌 **Soporte técnico y seguridad online** están fuertemente asociados a la retención (correlación negativa con evasión).
- 📌 **Mayor cobro mensual = mayor riesgo de fuga**, especialmente si el cliente no percibe valor equivalente.

---

## 💡 Recomendaciones Clave

1. **Migrar clientes a contratos anuales/bianuales** mediante incentivos (descuentos, meses gratis).
2. **Programa de onboarding activo** para los primeros 18 meses de vida del cliente.
3. **Promover soporte técnico y seguridad online** como servicios ancla de retención.
4. **Revisar la propuesta de valor** para clientes con alto cobro mensual y baja antigüedad.
5. **Construir un score de riesgo de churn** con las variables identificadas para priorizar acciones comerciales.

---

## 🛠️ Tecnologías Utilizadas

| Librería | Uso |
|----------|-----|
| `pandas` | Manipulación y limpieza de datos |
| `numpy` | Operaciones numéricas |
| `matplotlib` | Visualizaciones base |
| `seaborn` | Visualizaciones estadísticas (KDE, Boxplot) |

---

## ▶️ Cómo Ejecutar

1. Clona el repositorio:
```bash
git clone https://github.com/tu-usuario/Challenge-Telecom-X-Latam.git
cd Challenge-Telecom-X-Latam
```

2. Instala las dependencias:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Abre el notebook:
```bash
jupyter notebook TelecomX_LATAM.ipynb
```

4. Para ejecutar los gráficos de forma individual:
```bash
python graficos/grafico_01_distribucion_evasion.py
```

---

## 👤 Autor

Desarrollado como parte del programa de formación en Data Science — **Alura Latam + Oracle Next Education (ONE)**.

---

<div align="center">
  <sub>Hecho con 🐍 Python y muchos ☕</sub>
</div>
