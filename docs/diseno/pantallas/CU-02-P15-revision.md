---
id: CU-02-P15
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-02, CU-06]
requisitos: [RF-014, RF-016]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-02-P15 Revisión de requisitos formales

## Propósito

Revisar los requisitos formales y marcarlos como revisados.

## Requisitos

- RF-014
- RF-016

## Componentes

- plantilla-app-shell
- organismo-tabla: ID, título, prioridad, estado
- atomo-insignia: formal, revisado
- atomo-boton: secundario "Marcar como revisado" por fila
- atomo-banner: aviso de bloque sin revisar, error de validación

## Estados

- principal: tabla con los requisitos formales pendientes de revisión y el contador "N por revisar" arriba.
- vacío: "No hay requisitos por revisar".
- bloque sin revisar: banner de aviso "Este bloque quedó sin revisar porque el agente se detuvo". Los requisitos del bloque aparecen con su insignia formal.
- error de validación: banner de error "Este requisito no tiene criterios; no se puede marcar como revisado". La fila queda en estado formal.
- cargando: filas en esqueleto.

## Disposición

Contador arriba a la izquierda; tabla debajo; cada fila con su botón de revisión.

## Accesibilidad

Cada botón indica su elemento, por ejemplo "Marcar RF-005 como revisado"; el banner se anuncia al aparecer.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.