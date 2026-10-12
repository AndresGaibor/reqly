---
id: CU-03-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-03]
requisitos: [RF-006, RF-007, RF-008]
---

# Flujo CU-03: Resolver un conflicto con un agente

Recorrido del caso de uso CU-03. Un agente cambia en disco un archivo que el usuario está editando.

## Camino principal

1. Editar un archivo en el editor: CU-01-P5 (RF-006).
2. Un agente cambia el mismo archivo en disco. Ocurre fuera de reqly (RF-008).
3. Intentar guardar: CU-01-P6, estado principal (RF-008).
4. Elegir: conservar la mía, conservar la del disco o combinar a mano: CU-01-P6 (RF-008).
5. Guardar la elección con commit: CU-01-P6, estado resuelto (RF-007).

## Caminos alternos

- A1. Combinar las dos versiones a mano antes de guardar: CU-01-P6, botón combinar a mano (RF-008).

## Errores

- E1. El usuario no elige: el archivo no se guarda (RF-008). Se muestra CU-01-P6, estado principal.

## Resultado

Nada se sobrescribe sin decisión del usuario.
