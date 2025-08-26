# Regresión logística binaria con dataset de Autismo — README corto

Entrené y validé un modelo de **regresión logística binaria** en el cuadernillo `lab3_autismo.ipynb`. Incluí el gráfico de costo, predicciones y una evaluación clara en datos de prueba.

## Dataset
- Archivo: `Autism_Screening_Data_Combined.csv`
- Tamaño: > 6000 filas (cumple m≥1000)
- Features usadas (5): `A1`, `A2`, `A3`, `A4`, `Age`
- Objetivo: `Class` mapeado a 1 (YES) y 0 (NO)

## Preprocesamiento (Pandas)
Limpieza básica de nulos y reindexado:
```python
data = data.dropna().reset_index(drop=True)
```

## Entrenamiento
- Agrego columna de unos (sesgo) y entreno con **descenso por gradiente** sobre la función de costo logística.
- Grafiqué `J_history` para ver la convergencia.

## Validación (80/20)
Separé el 20% para **prueba** antes de entrenar (sin fuga de datos). Reporto:
- **Accuracy** en test
- **TP, TN, FP, FN** (mini matriz de confusión)

## Cómo correr
- Colab: sube ambos archivos y usa `path = "/content"`.

## Estructura del repo
```
README.md
lab3_autismo.ipynb
Autism_Screening_Data_Combined.csv
```

## Notas
- El objetivo del cuadernillo es mostrar el flujo completo: datos → preprocesado → entrenamiento → gráfico → validación.
