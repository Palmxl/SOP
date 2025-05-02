# Taller de Evaluación de Rendimiento  
**Curso:** Sistemas Operativos  
**Universidad:** Pontificia Universidad Javeriana  
**Profesor:** John Corredor
**Estudiante:** Juan Martín Sánchez 
**Fecha:** Mayo 2 del 2025  

---

## 📌 Descripción del taller

Este taller tiene como objetivo comparar el rendimiento de la multiplicación clásica de matrices bajo diferentes enfoques de paralelismo y configuraciones de hardware. Se busca medir los tiempos de ejecución y analizar cómo varía el rendimiento al utilizar distintas técnicas de programación concurrente:

- Procesos (`fork`)
- Hilos POSIX (`pthread`)
- Paralelismo con OpenMP

También se evalúa el impacto del número de hilos y el tamaño de las matrices sobre el rendimiento general.

---

## ⚙️ Implementaciones Incluidas

El proyecto contiene tres versiones del algoritmo de multiplicación de matrices:

- `mmClasicaFork.c`: Implementación utilizando procesos (`fork`)
- `mmClasicaPosix.c`: Implementación utilizando hilos POSIX (`pthread`)
- `mmClasicaOpenMP.c`: Implementación utilizando la librería OpenMP

Cada versión recibe dos argumentos:
```bash
./ejecutable TAM_MATRIZ NUM_HILOS
