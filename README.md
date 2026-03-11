# RoastAI
### Clasificación de granos de café y análisis de producción global

Especialización en Ciencia de Datos e Inteligencia Artificial · UTEC – MIT · 2025–2026  
**Equipo:** Catalina Vaz Martins · [Diego Aguiar](https://github.com/aguiar28d) · [Mariana Sambucetti](https://github.com/marianasambucetti)

---

## Descripción

Proyecto en dos partes: un análisis exploratorio de la producción mundial de café y un modelo de computer vision para clasificar granos por nivel de tostado.

**Parte 1 — EDA:** análisis de datos USDA sobre producción, distribución y exportación de café en 94 países entre 1960 y 2023. Se identificaron tendencias de producción global, concentración regional y posicionamiento en la cadena de valor.

**Parte 2 — Computer Vision:** modelo de clasificación de imágenes de granos de café en cuatro categorías (verde, claro, medio, oscuro) usando ResNet18 con transfer learning, entrenado en PyTorch. Incluye análisis de interpretabilidad con Grad-CAM.

## Contenido

El notebook `roastai.ipynb` está organizado en las siguientes secciones:

1. **EDA — Producción global** — evolución 1960–2023, concentración por región, cadena de valor
2. **Preparación del dataset** — descarga desde Kaggle, limpieza, detección de duplicados, split train/test
3. **Visualización** — distribución de clases, muestras por nivel de tostado
4. **Arquitectura del modelo** — ResNet18 preentrenado, capa final adaptada a 4 clases
5. **Entrenamiento** — Adam optimizer, early stopping, historial de pérdida y accuracy
6. **Evaluación** — matriz de confusión, classification report, accuracy por clase
7. **Grad-CAM** — visualización de las zonas de la imagen que activan la clasificación

## Resultados destacados

- Sudamérica concentra el mayor volumen de producción global de café
- La mayoría de las regiones exporta café verde (sin procesar), capturando menor valor en la cadena
- Modelo ResNet18: **precisión superior al 85%**
- Grad-CAM confirma que el modelo aprende características visuales relevantes del grano

## Stack

```
Python · PyTorch · ResNet18 · Transfer Learning · Grad-CAM · Pandas · NumPy · Plotly · Matplotlib · Kaggle API
```

## Fuente de datos

- **EDA:** USDA — Coffee Production, Supply and Distribution ([Kaggle](https://www.kaggle.com/datasets/parasrupani/coffee-distribution-across-94-counties))
- **Modelo:** Coffee Bean Dataset V1 ([Kaggle](https://www.kaggle.com/datasets/sot2542/coffee-bean-dataset-v1)) incrementado con fotos propias.
