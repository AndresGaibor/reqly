---
id: CU-09-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-09]
requisitos: [RF-007, RF-022, RF-028]
---

# Flujo CU-09: Mantener las skills del proyecto

Recorrido del caso de uso CU-09. Ver y actualizar las skills instaladas en el proyecto.

## Camino principal

1. Abrir la vista de skills: CU-09-P17 (RF-022).
2. Ver la versión instalada y la de reqly de cada skill: CU-09-P17 (RF-022).
3. Actualizar una skill desactualizada: CU-09-P17, botón actualizar (RF-028).
4. Guardar el cambio con commit: CU-09-P17 (RF-007).

## Caminos alternos

- A1. La versión instalada es más nueva que la de reqly: CU-09-P17, aviso, no se sobrescribe (RF-028).

## Errores

- E1. Un archivo de skill no tiene el formato esperado: CU-09-P17, estado formato no válido; el resto del proyecto sigue visible (RF-022).

## Resultado

Las skills del proyecto quedan visibles con su versión y actualizadas cuando procede.
