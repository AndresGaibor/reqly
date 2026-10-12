---
id: CU-01-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-01]
requisitos: [RF-001, RF-002, RF-003, RF-005, RF-006, RF-007, RF-008, RF-009, RF-016, RF-024, RF-028]
---

# Flujo CU-01: Revisar el estado del proyecto

Recorrido de punta a punta del caso de uso CU-01. Cada paso indica la pantalla que lo cubre.

## Camino principal

1. Seleccionar la carpeta del proyecto: CU-01-P1 (RF-001, RF-028).
2. Ver el avance y el número de huecos: CU-01-P2 (RF-002).
3. Abrir la matriz de trazabilidad y filtrar los huecos: CU-01-P3 (RF-005).
4. Abrir un requisito y ver su caso de uso y su diseño: CU-01-P7 (RF-009).
5. Editar el Markdown y revisar la vista previa: CU-01-P5 (RF-006).
6. Guardar: CU-01-P5 en estado "Guardado · commit" (RF-007).

## Caminos alternos

- A1. Ver el documento como texto continuo: CU-01-P4 (RF-003).
- A2. Penpot no responde o el frame no se puede mostrar: CU-01-P7, estado "diseño no disponible" (RF-009).
- A3. Consultar el historial de un requisito: CU-01-P8 (RF-024).
- A4. Ver los requisitos en tabla: CU-01-P9 (RF-004).

## Errores

- E1. La carpeta no tiene documentos de reqly: CU-01-P1, estado "error" (RF-001).
- E2. Un agente cambió el archivo en disco: CU-01-P6 (RF-008).
- E3. Falla una validación al guardar: CU-01-P5, estado "error de validación" (RF-016).
- E4. Falla el commit: CU-01-P5, estado 'error de commit' (S-12).