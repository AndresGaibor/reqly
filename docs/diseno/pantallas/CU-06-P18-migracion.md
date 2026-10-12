---
id: CU-06-P18
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-06]
requisitos: [RF-021, RF-007, RF-015]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-06-P18 Migración por bloques

## Propósito

Revisar cada bloque de requerimientos que propone el agente antes de seguir con el siguiente.

## Requisitos

- RF-021
- RF-007
- RF-015

## Componentes

- plantilla-app-shell
- organismo-tabla (requerimiento propuesto, origen, texto)
- atomo-boton (primario "Aprobar bloque"; secundario "Rechazar bloque"; por fila "No migrar")
- atomo-banner (aviso con el número de bloque)

## Estados

- **pendiente de revisión**: encabezado "Bloque 2 de 6" y el origen del bloque; la tabla con los requerimientos propuestos.
- **aprobado**: confirmación breve y botón "Siguiente bloque".
- **rechazado**: el bloque vuelve al agente; se muestra el motivo que escribió el usuario.
- **sin más bloques**: resumen de los requerimientos creados y de los que se marcaron "No migrar".
- **cargando**: tabla en esqueleto.

## Disposición

Encabezado con el número de bloque y el origen; banner de aviso debajo del encabezado; tabla; barra inferior con las acciones de bloque.

## Accesibilidad

Cada requerimiento enlaza a su origen; el encabezado del bloque es un encabezado de nivel 2.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.