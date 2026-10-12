---
id: CU-02-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-02]
requisitos: [RF-007, RF-012, RF-013, RF-014, RF-015, RF-016, RF-017, RF-018, RF-019]
---

# Flujo CU-02: Capturar y formalizar un requerimiento

Recorrido del caso de uso CU-02, opcional. El requerimiento se escribe en reqly y un agente lo formaliza en requisitos y casos de uso.

## Camino principal

1. Escribir el requerimiento en texto libre: CU-02-P14, estado nuevo (RF-012).
2. Guardarlo: CU-02-P14, estado abierto (RF-012).
3. Añadir notas si hace falta: CU-04-P13 (RF-015).
4. Pedir la formalización al agente con la skill reqly-formalizar. Ocurre fuera de reqly (RF-013).
5. Ver el requerimiento formalizado con sus requisitos y casos de uso: CU-02-P14, estado formalizado (RF-013).
6. Revisar cada requisito formal y marcarlo como revisado: CU-02-P15 (RF-014).

## Caminos alternos

- A1. Retirar un requisito en lugar de revisarlo: CU-07-P19 (RF-019).
- A2. El agente se detiene a mitad: CU-02-P15, estado bloque sin revisar; al retomar, continúa por bloques (RF-013, RF-007).

## Errores

- E1. Un requisito no tiene criterios: CU-02-P15, estado error de validación (RF-016).
- E2. Un caso de uso cita un RF que no existe: CU-01-P5, estado advertencia de referencia rota (RF-016).
- E3. Dos archivos tienen el mismo ID: CU-01-P1, estado ID duplicado (RF-017).

## Resultado

El requerimiento queda trazado a requisitos formales y casos de uso, listos para revisión.
