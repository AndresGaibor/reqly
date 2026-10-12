---
id: CU-05-P20
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-05]
requisitos: [RF-009]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-05-P20 Diseño de pantallas

## Propósito

Ver las pantallas diseñadas por caso de uso, su estado de revisión y su referencia en Penpot.

## Requisitos

- RF-009

## Componentes

- plantilla-app-shell
- atomo-campo (filtro por caso de uso)
- organismo-tabla (Pantalla, Caso de uso, Estado, Referencia)
- atomo-insignia (sin revisar, revisado)
- atomo-banner (Penpot no disponible)

## Estados

- **principal**: tabla de pantallas con su referencia.
- **Penpot no disponible**: banner de aviso; la columna Referencia muestra el texto "archivo · página · frame" sin enlace de vista gráfica.
- **sin resultados**: el filtro no coincide con ninguna pantalla.
- **vacío**: "Todavía no hay pantallas diseñadas".
- **cargando**: filas en esqueleto.

## Disposición

Filtro arriba; banner de aviso, si aplica, debajo del filtro; tabla con una fila por pantalla.

## Accesibilidad

Las referencias son texto legible, no solo enlaces; el filtro tiene etiqueta visible.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.