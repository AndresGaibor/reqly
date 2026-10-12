---
id: CU-01-P5
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01, CU-02]
requisitos: [RF-006, RF-007, RF-016]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P5 Editor con vista previa

## Propósito

Editar un documento y ver la vista previa antes de guardar.

## Requisitos

RF-006, RF-007, RF-016.

## Componentes

- plantilla-app-shell, variante de dos paneles
- atomo-boton, primario, "Guardar"
- atomo-banner, error de validación
- atomo-insignia, estado del archivo

## Estados

- sin guardar: barra con el nombre del archivo y el estado "Sin guardar" en color.feedback.warning.text.
- guardado: estado "Guardado · commit <ID corto>" en color.feedback.success.text.
- guardando: botón "Guardar" en estado de carga.
- error de validación: banner de error que indica el campo que falta; el archivo no se guarda (RF-016).
- advertencia de referencia rota: banner de aviso que indica la referencia que no existe, por ejemplo un RF que no existe. El archivo sí se guardó (RF-016).
- error de commit: banner de error "No se pudo guardar el commit. El archivo queda guardado en disco." con el botón "Reintentar commit" (S-12).

## Disposición

Plantilla plantilla-app-shell. En escritorio, editor a la izquierda y vista previa a la derecha. Barra superior con el nombre del archivo, el estado y el botón "Guardar". En móvil, pestañas "Editar" y "Vista previa".

## Accesibilidad

El editor tiene etiqueta. El banner de error se anuncia al aparecer y enlaza al campo que falta.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.