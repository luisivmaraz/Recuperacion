# Actividad de recuperacion -Sistema de analisis mental-

Esta actividad de recuperacion se centro en un análisis exploratorio de un conjunto de datos relacionado con la salud mental en el trabajo, con el fin de extraer conocimientos útiles y entrenar un modelo de predicción sobre la necesidad de tratamiento (mental o físico) a partir de la edad y el género.

---

##  Contenido del Proyecto

- [`Survey`](survey.csv): Es el archivo CSV.
- [`Recuperacion`](Recuperacion.ipynb): Es el notebook donde se trabajo.
- [`imgs`](./imgs): imagenes utilizadas.
- [`README.md`](./README.md): Este documento que lees.

---

## 1. Descripción del Dataset

El dataset contiene registros de encuestas realizadas a personas trabajadoras sobre su salud mental y física. Las variables que se utilizaron fueron:

- **Age**: Edad.
- **Gender**: Género.
- **treatment**: Si ha recibido tratamiento (Mental o fisica).
- **mental_vs_physical**: Clasificación del tipo de tratamiento.
- **work_interfere**: Qué tanto interfiere su salud en el trabajo, entre otras.

---

##  2. Preprocesamiento de Datos

Se realizaron las siguientes transformaciones:

- **Renombrado del DataFrame** a `salud` para simplificar la manipulación.
- **Estandarización del campo `Gender`**, consolidando variaciones como `M`, `F`, `male`, `Male`, `female`, `FEMALE`, etc., en dos categorías principales:
  - `Male`
  - `Female`
- **Eliminación de valores nulos** o reemplazo con etiquetas como `Desconocido` donde fue necesario.

---

## 3. Análisis

### Valores Nulos

Se identificaron y visualizaron las columnas con más valores faltantes, destacando variables como `work_interfere` y `self_employed`.

### Visualizaciones (Graficos)

- **Personas que han recibido tratamiento** del total de quienes reciben tratamiento.
- **Distribución de edades** de los  que reciben tratamiento.
- **Tipo de tratamiento (mental o físico)** segmentado por género.
- **Número de personas por género y de tratamiento** que reciben y no reciben tratamiento.
- **Tipo de tratamiento por género** distribuido en fisico y mental.

> Las visualizaciones nos permitieron identificar patrones como:
> - Mayor tratamiento mental en mujeres.
> - Interferencia del trabajo con la salud mental en adultos jóvenes.

---

## 4. Sistema de Recomendación (Modelo Predictivo)

Se construyó el sistema de prediccion utilizando:

- **Variables**: Edad y género.
- **Salida esperada**: Tipo de tratamiento recomendado (`Mental` o `Physical`).

### Entrada esperada:

```python
edad = 28
genero = 'Male'
```

### Salida esperada: 

```python
Recomendación: Mental
```

### Conclusiones del analisis

- La mayoría de los encuestados que han recibido tratamiento lo han hecho por temas mentales.

- Las mujeres tienden a buscar más tratamiento en comparación con los hombres, especialmente para temas de salud mental.

- La edad influye: personas entre los 25 y 35 años reportan mayor interferencia de su salud en el trabajo.

#### Autor
- Luis Iván Márquez Azuara 
- Matricula: 220401
- Grado y grupo: 9°A
- Carrera: Ingeniería en Desarrollo y Gestión de Software