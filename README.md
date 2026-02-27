# Arquitectura Analítica para la Planificación Territorial Educativa

Este repositorio contiene el código fuente, la documentación técnica y la estructura de datos. El proyecto implementa una arquitectura de ciencia de datos que conecta microdatos institucionales con el Censo de Población y Vivienda 2022 INEC del Ecuador mediante técnicas de aprendizaje mixto.
---
## Demo

https://hjdeun-christian0rolando-oyola0flores.shinyapps.io/UPS-SYSCLUS/

---
## Resumen del Proyecto


El objetivo central es superar la planificación educativa convencional mediante una arquitectura de ciencia de datos que identifica perfiles de demanda potencial. El proceso transita desde una muestra institucional etiquetada hacia una clasificación masiva a nivel nacional, permitiendo identificar no solo dónde están los perfiles, sino qué tan accesible es atenderlos mediante análisis geoespacial.

### Pipeline Técnico
1. **Segmentación:** Uso de Distancia de Gower y algoritmo jerarquico + PAM para identificar perfiles sociodemográficos complejos.
2. **Escalamiento:** Entrenamiento de un modelo supervisado (LightGBM) para clasificar el universo del Censo 2022.
3. **Geoprocesamiento:** Generación de isócronas y mapas de densidad para priorización territorial.

---

## Estructura del Repositorio
| Archivo / Carpeta | Descripción |
| :--- | :--- |
| **`TFM.ipynb`** | **Core Analítico.** Jupyter Notebook con el flujo completo: preprocesamiento, clustering (Gower/PAM), modelado predictivo con LightGBM y validación de resultados. |
| **`slides.pdf`** | **Presentación Ejecutiva.** Resumen visual del proyecto cubriendo contexto, metodología de escalamiento, resultados y conclusiones estratégicas. |
| **`TFM_COyola_31-12-2025.pdf`** | **Memoria Técnica (Tesis).** Documento académico integral que contiene el marco teórico, la justificación metodológica y el análisis de impacto social. |
| **`DICCIONARIO_BDD_CANTON.xlsx`** | **Metadata.** Diccionario de variables detallado para la interpretación de los indicadores generados a nivel de unidad administrativa local (LAU2/Cantón). |
| **`Images/`** | **Recursos Visuales.** Directorio que contiene los esquemas de la arquitectura analítica, diagramas de flujo y exportaciones cartográficas. |

## Acceso a Datasets (Fuentes Externas)
Debido al volumen de los registros procesados (Universo Censo 2022), los datasets se encuentran alojados en **Zenodo** bajo los siguientes accesos directos:

* **Dataset 01: Entrenamiento y Segmentación (Muestra):** [Acceder a Zenodo (ID: 18166576)](https://zenodo.org/records/18166576?token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6ImQ0YWY5YTQ1LTIyY2QtNGUxZC04OGQ2LWNiY2RjNTBkYWExZiIsImRhdGEiOnt9LCJyYW5kb20iOiJhMTAwOWMxMDYyNWYwOGYwNmJiYzQ4MGJlYTE4NjAxNSJ9.DKsQKjXgDPjK0GH5K3RmVrXjByfsjcnq6ATYYeSZ2w3iPs0s5sCt2fZxyKGtD7RWzLzx8ragkht1MNeU4WSBJA)
* **Dataset 02: Resultados de Inferencia Nacional (Censo):** [Acceder a Zenodo (ID: 18165393)](https://zenodo.org/records/18165393?token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6Ijg1NjE4YWU4LWI3NTMtNGQ3My1hOGZjLTFlNzUxZGU3NTc0YSIsImRhdGEiOnt9LCJyYW5kb20iOiIzYTIzNzRjMTE1Yzg4YmIzMGJkMTg3Yzg1ZWVjMDA3NCJ9.mELXqJUwybhcpMf71jlfsdE72nXdcfzxdVdfKFWpie3GLC13TLdblzK0iBgkPOIjSdbsPD8pAzSpe4VQP4QXGw)

## Stack Tecnológico
* **Análisis de Datos:** Python 3.10+ (Pandas, NumPy, Scikit-learn).
* **Machine Learning:** LightGBM (Gradient Boosting Framework).
* **Métricas de Similitud:** Gower Distance (para datos mixtos).
* **Geo-Intelligence:** Geopandas, OSMnx (Análisis de rutas e isócronas).

## Licencia y Uso
Este trabajo tiene fines académicos y de planificación pública. Se solicita citar al autor y el documento de tesis adjunto para cualquier réplica o uso de la metodología.
