# Proyecto de Credit Scoring 🌐

## Problema de Negocio

Este proyecto tiene como objetivo desarrollar un modelo de machine learning para identificar a los potenciales malos pagadores. De esta forma, se busca:

- Negar el crédito a estos clientes o establecerles condiciones más restrictivas.
- Aplicar una mayor tasa de interés para reducir el tiempo de recuperación del capital.

Para lograrlo, se proporciona un dataset con información sobre los créditos y los clientes. Aquellos clientes que incumplieron su cronograma de pagos tienen el crédito en un estado de **default**.

---

## Etapas del Análisis

### 1. Preprocesamiento de Datos 🔧

En esta etapa, realizamos los siguientes pasos:

- **Limpieza de datos:** Omitir valores anómalos y corregir valores atípicos.
- **Manejo de datos perdidos:** Rellenar los datos faltantes de manera adecuada.
- **Datos cualitativos:** Eliminar las categorías menos frecuentes para mejorar la representatividad.

### 2. Exploración de Datos 🔍

Con los datos limpios, se analizan las relaciones y contribuciones al riesgo de default:

- **Variables numéricas:** Examinar la relación entre cada variable y el riesgo de default.
- **Variables categóricas:** Calcular la contribución al riesgo de cada categoría.

### 3. Construcción del Modelo 🎨

Esta etapa incluye:

1. **Partición de datos:** Dividir el dataset en conjuntos de entrenamiento y prueba.
2. **Transformación de variables categóricas:** Convertirlas a formato binario.
3. **Modelos a utilizar:**
   - **Logit**
   - **Árbol de Clasificación**
   - **Random Forest**
4. **Ajuste y evaluación inicial:** Calcular los indicadores de precisión inicial para cada modelo.
5. **Curva ROC:** Identificar el punto de corte óptimo y actualizar los indicadores de precisión.

### 4. Evaluación y Selección del Modelo 🏋‍♂️

Con las métricas ajustadas al punto de corte óptimo, evaluamos:

- **Tasa esperada de malos clientes:** ¿Cuántos clientes buenos perdemos con este punto de corte?
- **Restricciones de capital:** Si la entidad está limitada de recursos para otorgar créditos, determinamos:
  - El mejor modelo.
  - El score mínimo que se le pediría al cliente.
