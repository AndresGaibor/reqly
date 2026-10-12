---
id: CU-08-P11
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-08]
requisitos: [RF-023, RF-007]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-08-P11 Decisiones (ADR)

## Propósito

Ver las decisiones de arquitectura del proyecto, con su estado, y leer cada una.

## Requisitos

- RF-023
- RF-007

## Componentes

- plantilla-app-shell (variante de dos paneles)
- molecula-elemento-lista (un elemento por ADR)
- atomo-insignia (estados propuesto, aceptado y reemplazado)
- atomo-boton (primario "Nueva decisión"; secundario "Reemplazar decisión")
- organismo-dialogo (para crear o reemplazar)

## Estados

- principal: lista de ADR en orden numérico (0001, 0002...), con título, estado y fecha; el panel de detalle muestra el primero.
- detalle abierto: título, contexto, decisión, consecuencias y, si aplica, el ADR que lo reemplaza, como enlace.
- reemplazando: diálogo para crear el ADR que reemplaza; el ADR original queda en estado reemplazado al guardar.
- vacío: "Sin decisiones registradas".
- cargando: lista en esqueleto.

## Disposición

En escritorio, lista a la izquierda y detalle a la derecha; en móvil, la lista y, al elegir una decisión, el detalle ocupa la pantalla. La pantalla se construye sobre plantilla-app-shell en su variante de dos paneles.

## Reglas

Un ADR aceptado no se edita; solo se reemplaza (S-07).

## Accesibilidad

La lista se recorre con teclado; el detalle se anuncia al cambiar de decisión.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.
