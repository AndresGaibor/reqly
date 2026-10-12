---
id: CU-07-P16
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-07]
requisitos: [RF-020, RF-018, RF-007]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-07-P16 Tickets

## Propósito

Ver los tickets por estado y cambiar su estado.

## Requisitos

- RF-020
- RF-018
- RF-007

## Componentes

- plantilla-app-shell
- molecula-pestanas: Pendiente, En curso, Hecho, Retirado
- organismo-tabla: ID, título, requisito enlazado, estado
- atomo-insignia: estados del ticket
- atomo-boton: secundario "Cambiar estado"
- atomo-banner: error de transición

## Estados

- principal: tabla de la pestaña activa.
- cambiar estado: menú con los estados permitidos desde el estado actual.
- transición no permitida: banner de error "No se puede pasar de retirado a en curso"; el estado no cambia.
- vacío: "No hay tickets en este estado".
- cargando: filas en esqueleto.

## Disposición

Pestañas arriba; tabla debajo; acción de cambiar estado en cada fila.

## Accesibilidad

El menú de estado se recorre con teclado; el banner se anuncia al aparecer.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.