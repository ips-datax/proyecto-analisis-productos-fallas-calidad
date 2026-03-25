# Análisis de fallas en productos y su impacto económico

## Contexto de negocio

Una empresa realiza inspecciones de calidad sobre sus productos. Sin embargo, la información se encuentra distribuida en múltiples archivos Excel con inconsistencias en formatos, categorías y registros.

Esto dificulta responder preguntas clave como:

- ¿Quiénes son los responsables con mayor incidencia de fallas?
- ¿Qué áreas generan mayor impacto?
- ¿Qué tipos de fallas afectan más económicamente?
- ¿Qué tan confiables son los datos?

El objetivo de este proyecto es transformar datos desordenados en información accionable para la toma de decisiones.

---

## Fuentes de datos

Se integraron múltiples archivos Excel:

- inspecciones_calidad.xlsx
- responsables_maestro.xlsx
- productos_maestro.xlsx
- costos_fallas.xlsx

Los datos presentan problemas reales como:

- categorías duplicadas y mal escritas
- inconsistencias en textos (mayúsculas/minúsculas)
- valores faltantes
- registros sin trazabilidad

---

## Proceso de análisis

El proyecto fue desarrollado en Python utilizando pandas y matplotlib.

Etapas principales:

1. Carga de múltiples fuentes de datos
2. Diagnóstico de calidad de datos
3. Limpieza y estandarización:
   - normalización de textos
   - homologación de categorías
   - conversión de fechas
4. Validaciones de negocio
5. Cruce de tablas (joins)
6. Construcción de base consolidada
7. Cálculo de KPIs
8. Análisis de impacto económico
9. Visualización de resultados
10. Exportación final

---

## Resultados clave

### Responsables con mayor impacto

- Nicolás Ibarra:
  - 7 fallas
  - tasa: 46.6%
  - costo: 564

- Jorge Núñez:
  - 6 fallas
  - costo más alto: 570

- Luis Peña:
  - tasa alta: 40%

Se identifican responsables con alta tasa de falla y alto impacto económico, lo que sugiere problemas estructurales en sus procesos.

---

### Análisis por área

- Calidad:
  - 25 fallas
  - mayor costo total: 2,271

- Producción:
  - tasa más alta: 31.1%
  - costo: 1,036

Producción presenta problemas en origen, mientras que Calidad concentra la detección del impacto.

---

### Tipos de falla y costo

- Más frecuentes:
  - Etiquetado incorrecto: 21 casos
  - Golpe: 18 casos

- Mayor impacto económico:
  - Sellado defectuoso: 928
  - Empaque abierto: 705
  - Fuga: 506

No todas las fallas tienen el mismo impacto: algunas menos frecuentes generan mayor costo.

---

### Insight clave de negocio

Las fallas operativas no deben priorizarse solo por frecuencia, sino por su impacto económico.

---

### Problemas de calidad de datos

Se detectaron:

- 33 registros sin estado de caso
- 10 casos aprobados con fallas
- registros sin correspondencia en maestros

Esto afecta directamente la confiabilidad del análisis y la toma de decisiones.

---

## Insights estratégicos

- Existen responsables con tasas superiores al 40%, lo que indica problemas estructurales.
- Producción es un punto crítico en la generación de fallas.
- Calidad concentra el mayor costo total, reflejando impacto acumulado.
- Algunas fallas tienen bajo volumen pero alto impacto económico.
- La calidad de los datos es un problema relevante dentro del proceso.

---

## Recomendaciones

- Auditar procesos de responsables con mayor tasa de falla
- Revisar procesos en Producción (origen del problema)
- Priorizar fallas con mayor impacto económico
- Implementar validaciones en captura de datos
- Estandarizar categorías desde origen
- Mejorar la gestión del estado de los casos

---

## Tecnologías utilizadas

- Python
- Pandas
- Matplotlib
- Google Colab

---

## Estructura del proyecto

- datos/: archivos Excel utilizados
- notebooks/: análisis en Python
- README.md: documentación del proyecto

---

## Ejecución

El análisis fue desarrollado en Google Colab.

El notebook se encuentra disponible en la carpeta `/notebooks`.

---

## Conclusión

Este proyecto demuestra cómo transformar múltiples fuentes de datos desordenadas en información accionable, identificando no solo dónde ocurren los problemas, sino también cuáles generan mayor impacto económico.

El valor del análisis no está en los gráficos, sino en la capacidad de conectar datos con decisiones de negocio.
