---
id: CU-07-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-07]
requisitos: [RF-018, RF-019, RF-020, RF-007]
---

# Flujo CU-07: Cambiar el estado de un ticket

Recorrido del caso de uso CU-07. El usuario o el agente cambian el estado de un ticket.

## Camino principal

1. Abrir la lista de tickets: CU-07-P16 (RF-020).
2. Elegir la pestaña del estado actual: CU-07-P16 (RF-020).
3. Cambiar el estado con el menú de la fila: CU-07-P16 (RF-018).
4. Guardar con commit: CU-07-P16, la fila muestra el nuevo estado (RF-007).

## Caminos alternos

- A1. Retirar el ticket porque el usuario lo pide: CU-07-P19 (RF-019).

## Errores

- E1. Transición no permitida, por ejemplo de retirado a en curso: CU-07-P16, estado transición no permitida (RF-018).

## Resultado

El ticket queda en el estado elegido y el cambio queda registrado en el historial del proyecto.
