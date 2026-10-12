---
id: CU-01-P3
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01]
requisitos: [RF-005]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P3 Matriz de trazabilidad

## Propósito

Ver qué requisitos tienen caso de uso, diseño, ticket y prueba, y dónde hay huecos.

## Requisitos

RF-005.

## Componentes

- plantilla-app-shell
- molecula-celda-trazabilidad
- atomo-boton, secundario, para el filtro

## Estados

- principal: tabla con todas las filas.
- solo huecos: el filtro "Solo huecos" activo, solo quedan las filas con algún hueco.
- cargando: filas en esqueleto.

## Disposición

Plantilla plantilla-app-shell. Tabla con una fila por requisito (RF y RNF) y columnas Requisito, Caso de uso, Diseño, Ticket y Prueba. El filtro "Solo huecos" arriba a la derecha. La primera columna queda fija al desplazarse. En móvil, cada fila se convierte en una tarjeta.

## Accesibilidad

La tabla tiene encabezados de columna. Cada celda indica su estado con icono y texto.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.