# Modelos Lineales Predictivos para <span style="color: rgb(138, 92, 245);">Precios de Autos</span>

## <span style="color: rgb(138, 92, 245);">OBJETIVO</span>

Este proyecto tiene como objetivo **predecir el precio de automóviles usados** a partir de un dataset con características como marca, modelo, año, kilometraje, tipo de combustible, transmisión, entre otras.  

Se implementaron técnicas de **limpieza de datos, tratamiento de outliers, manipulación de variables categóricas** y se evaluaron modelos de regresión lineal regularizados utilizando **validación cruzada y Grid Search**.  

---
```
# Estructura de Repositorio

used_cars_price_prediction/
│
├── modelos_lineales.ipynb      # Notebook principal del proyecto
├── df_final.csv                # Dataset limpio y procesado
├── requirements.txt            # Librerías necesarias
├── .gitignore                  # Exclusiones de Git (entornos, datos sensibles, etc.)
└── README.md                   # Documentación del proyecto

```

>[!Example] Estructura Completa de Pipeline
>1. Extracción de Datos
>2. Transformación de Datos
>* 2.1 Limpieza e Ingeniería de Datos
>* 2.2 Análisis Exploratorio de Datos
>* 2.3 Construcción de Nuevas Variables
>1. Construcción de Modelos Lineales Predictivos 
>* 3.1 Regresión Lineal
>* 3.2 Regresión Logística
>* 3.3 Regresión LASSO
>* 3.4 Regresión LARS
>* 3.5 Regresión de Cresta
>* 3.6 Regresión de Red Elástica
>* 3.7 Regresión Bayesiana
>4. Análisis de Modelos Predictivos


---

## Principales pasos del análisis

1. **Exploración y limpieza de datos**
    
    - Revisión de valores faltantes y duplicados.
        
    - Tratamiento de outliers usando **DBSCAN**.
        
        
2. **Feature Engineering (creación de variables)**
    
    - Generación de nuevas variables derivadas del dataset original para enriquecer el modelo.
        
3. **Modelado**
    
    - Se probaron **modelos lineales**:
        
        - Regresión Lineal.
            
        - **Ridge** (regularización L2).
            
        - **Lasso** (regularización L1).
            
        - **ElasticNet**.
            
        - **Bayesian Ridge**.
            
        - **Lars**.
            
    - Búsqueda de hiperparámetros con **Grid Search + Validación Cruzada (CV=5)**.
        
4. **Métricas de evaluación**
    
    - R² (Coeficiente de Determinación).
        
    - MAE (Error Absoluto Medio).
        

---

## Resultados

- **Mejor modelo:** Ridge Regression
    
- **Mejor alpha:** `0.01`
    
- **R² (entrenamiento):** `0.906`
    
- **R² (validación):** `0.909`
    
- **MAE (validación):** `1926.78`
    

Estos resultados indican que el modelo explica aproximadamente el **91% de la variabilidad de los precios** con un error promedio cercano a **£1900** en las predicciones.
