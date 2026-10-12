---
id: CU-05-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-05]
requisitos: [RF-009]
---

# Flujo CU-05: Ver el diseño de un requisito en Penpot

Recorrido del caso de uso CU-05. El usuario ve el diseño de un requisito, o su referencia si no se puede mostrar.

## Camino principal

1. Abrir el requisito: CU-01-P7 (RF-009).
2. Ver el diseño como vista gráfica del frame: CU-01-P7, estado con diseño visible (RF-009).

## Caminos alternos

- A1. El diseño no se puede mostrar: CU-01-P7, estado diseño no disponible; la referencia aparece en texto (RF-009).
- A2. El requisito no tiene referencia de diseño: CU-01-P7, la sección Diseño no aparece (RF-009).
- A3. Ver todas las pantallas por caso de uso: CU-05-P20 (RF-009).

## Errores

- E1. La referencia apunta a un frame que no existe: CU-01-P7, estado diseño no disponible, con el aviso de referencia que no existe (RF-009).

## Resultado

El usuario ve el diseño o la referencia para abrirlo en Penpot.
