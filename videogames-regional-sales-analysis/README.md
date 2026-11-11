---
title: "Análisis y Dashboard de Ventas Globales de Videojuegos"
subtitle: "Análisis Exploratorio de Datos y Aplicación Web en Streamlit"
description: "Evaluación del impacto de las reseñas de críticos y usuarios en las ventas regionales por plataforma y género, desplegado como un dashboard interactivo."
categories: [EDA, Streamlit, Visualización de Datos, Python, Render]
---

# 🎮 Estrategia comercial 2017: Análisis regional de ventas de videojuegos

**Problema de negocio:** La tienda de videojuegos "Store 1" necesita identificar patrones en los datos históricos de ventas para planificar sus campañas publicitarias para el año 2017. El desafío radica en que el éxito de un videojuego varía drásticamente según la región (Norteamérica, Europa y Japón) y la plataforma.

**Objetivo:** Analizar el comportamiento del mercado, identificar plataformas y géneros líderes por región, y evaluar el impacto de las reseñas de usuarios y críticos en las ventas globales.

---

## 📊 Hallazgos Principales

- **Ciclo de vida de las consolas:** Las plataformas tienen una vida útil de aproximadamente 10 años. Para el modelo de 2017, solo se utilizaron datos del período reciente (2014-2016) para evitar sesgos de hardware obsoleto.
- **Diferencias regionales clave:**
  - **Norteamérica y Europa:** Mercados dominados por consolas de sobremesa (PS4, Xbox One). Los géneros más rentables son **Shooter** y **Action**.
  - **Japón:** Un ecosistema totalmente distinto. Dominado por consolas portátiles (Nintendo 3DS) y el género **Role-Playing (RPG)**. Los juegos de acción occidentales tienen poca penetración.
- **Impacto de las reseñas:** Las reseñas de la crítica profesional muestran una correlación positiva moderada (~0.40) con las ventas. Las reseñas de usuarios tienen una correlación casi nula, lo que sugiere que la opinión digital no dicta el éxito comercial masivo.

---

## 🛠️ Metodología y Pruebas Estadísticas

1. **Limpieza y preparación:** Manejo de valores nulos en `year_of_release`, `critic_score` y `user_score` (incluyendo el string `'tbd'`). Cálculo de las ventas totales globales.
2. **Filtrado temporal:** Selección de datos a partir de 2014 para capturar la octava generación de consolas.
3. **EDA y Visualización:** Distribución de ventas por plataforma, análisis de ventas por género y perfilado regional (NA, EU, JP).
4. **Pruebas de hipótesis:** 
   - *H0:* Las calificaciones promedio de los usuarios en Xbox One y PC son iguales.
   - *H0:* Las calificaciones promedio de los usuarios en los géneros de Acción y Deportes son iguales.
   *(Ambas pruebas evaluadas con un nivel de significancia α = 0.05).*

---

## 📁 Contenido del repositorio

- `notebooks/01-analisis-regional.ipynb`: Notebook con el EDA, gráficos y pruebas estadísticas.
- `requirements.txt`: Dependencias del proyecto.

---

## ▶️ Cómo ejecutar

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01-analisis-regional.ipynb