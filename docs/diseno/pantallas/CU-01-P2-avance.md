---
id: CU-01-P2
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01]
requisitos: [RF-002, RF-010]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P2 Avance

## Propósito

Ver de un vistazo cuántos huecos hay y cuánto avanza el proyecto.

## Requisitos

RF-002, RF-010.

## Componentes

- plantilla-app-shell
- molecula-tarjeta-metrica, con tres tarjetas: huecos, avance y pendientes abiertos
- atomo-insignia, tipo hueco

## Estados

- principal con huecos: las tres tarjetas con sus valores y la lista de huecos.
- sin huecos: la tarjeta de huecos en verde con el texto "Sin huecos de trazabilidad".
- cargando: tarjetas en esqueleto.

## Disposición

Plantilla plantilla-app-shell. Tres tarjetas en fila, en móvil en columna. Debajo, una sección "No cuentan en el avance" con los contadores de "debería" y "podría". Debajo, la lista de huecos, cada uno con su ID como enlace al requisito y su insignia de hueco.

## Accesibilidad

Las tarjetas tienen su etiqueta como texto. La lista de huecos es una lista ordenada por ID.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.