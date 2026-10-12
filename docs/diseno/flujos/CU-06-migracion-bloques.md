---
id: CU-06-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-06]
requisitos: [RF-021, RF-013, RF-014, RF-015, RF-007]
---

# Flujo CU-06: Migrar documentos o código a requerimientos

Recorrido del caso de uso CU-06. La migración la hace un agente con la skill reqly-migrar; el usuario revisa cada bloque en reqly.

## Camino principal

1. Pedir la migración al agente con la skill reqly-migrar (RF-021). Ocurre fuera de reqly.
2. Revisar el bloque propuesto: CU-06-P18 (RF-021).
3. Aprobar el bloque: CU-06-P18, estado aprobado (RF-007).
4. Revisar los requisitos formales que resulten, si el usuario pidió formalizar: CU-02-P15 (RF-014).
5. Pasar al siguiente bloque: CU-06-P18 (RF-021).
6. Al terminar, revisar el resumen: CU-06-P18, estado sin más bloques (RF-021).

## Caminos alternos

- A1. No migrar un elemento del bloque: CU-06-P18, "No migrar"; el elemento queda como pendiente (RF-015).
- A2. Rechazar un bloque: CU-06-P18, estado rechazado; el agente lo vuelve a proponer (RF-021).

## Errores

- E1. El agente pierde cuota a mitad de un bloque: CU-02-P15, estado bloque sin revisar (RF-013).

## Resultado

Cada bloque migrado queda aprobado o rechazado en reqly y sus elementos son requisitos formales revisables.
