# Laboratorio 6: Benchmarking CSV vs Parquet

**Materia:** Fundamentos de Big Data (IDSD413)  
**Institución:** Escuela Politécnica Nacional  
**Docente:** David Esteban Galarza García
**Estudiante:** Paola Pacheco

## Descripción
Este laboratorio compara el rendimiento de los formatos CSV y Apache Parquet utilizando un conjunto sintético de 15 millones de transacciones comerciales en Google Colab.

## Objetivos
- Evaluar los tiempos de escritura y lectura.
- Comparar el almacenamiento y el consumo de memoria.
- Analizar la optimización columnar (Column Pruning).
- Implementar Predicate Pushdown con filtros múltiples.

## Herramientas
- Python
- Google Colab
- Pandas
- NumPy
- PyArrow

## Resultados principales

| Métrica | CSV | Parquet |
|---|---:|---:|
| Tamaño | 740,53 MiB | 225,39 MiB |
| Tiempo de lectura | 11,26 s | 2,62 s |
| Consulta avanzada | 13,0249 s | 1,3544 s |

La consulta avanzada recuperó exclusivamente el monto de las transacciones pertenecientes a la categoría `Juguetes` con estado `Completado`, con una aceleración aproximada de **9,62 veces** utilizando Parquet.

## Ejecución
1. Abrir el Notebook `.ipynb` en Google Colab.
2. Ejecutar las celdas en orden.
3. Revisar los resultados de benchmarking.
4. Comparar las consultas realizadas sobre CSV y Parquet.

Los archivos CSV y Parquet se generan durante la ejecución del Notebook.
