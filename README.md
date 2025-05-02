
# Taller de Evaluación de Rendimiento  
**Curso:** Sistemas Operativos 
**Universidad:** Pontificia Universidad Javeriana  
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
```

---

## 📈 Metodología de Evaluación

Para medir el rendimiento se utilizó la función `gettimeofday()` que permite capturar el tiempo de ejecución en microsegundos.  
Las pruebas se realizaron variando:

- El tamaño de la matriz: `200`, `400`, `800`
- El número de hilos: `1`, `2`, `4`, `8`
- 30 repeticiones por configuración para aplicar la ley de los grandes números

El script `lanza.pl` fue modificado para automatizar la ejecución de las pruebas por lotes.

---

## 🧪 Resultados (ejemplo)

| Tamaño de Matriz | Hilos | Promedio (μs) |
|------------------|--------|----------------|
| 400              | 1      | 303,922        |
| 400              | 2      | 174,386        |
| 400              | 4      | 134,211        |
| 400              | 8      | 121,512        |
| 800              | 1      | 3,119,355      |
| 800              | 2      | 1,580,788      |
| 800              | 4      |   931,369      |
| 800              | 8      |   904,013      |

---

## 📂 Estructura del Taller

```
.
├── mmClasicaFork.c
├── mmClasicaPosix.c
├── mmClasicaOpenMP.c
├── lanza.pl
├── datos/              # Resultados de ejecución (.csv)
├── README.md
├── ejecutable (MM_ejecutable)
└── Makefile
```

---

## 📌 Requisitos

- Sistema operativo Linux
- `gcc` 
- Perl (para ejecutar `lanza.pl`)

--- 
