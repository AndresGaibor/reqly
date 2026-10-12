---
id: CU-04-P13
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-04]
requisitos: [RF-015, RF-007]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-04-P13 Añadir nota

## Propósito

Permitir añadir una nota a un requerimiento, un requisito o un caso de uso.

## Requisitos

- RF-015
- RF-007

## Componentes

- organismo-dialogo
- atomo-campo: área de texto para la nota, casillas "Marcar como pregunta" y "Marcar como pendiente"
- atomo-boton: primario "Guardar nota", secundario "Cancelar"

## Estados

- abierto: campo vacío; el botón "Guardar nota" no está activo hasta escribir.
- guardando: botón en estado de carga.
- guardado: confirmación breve y la nota aparece en la ficha del elemento.
- error: banner de error "No se pudo guardar la nota"; el texto escrito se conserva.

## Disposición

Diálogo con el elemento de origen en el título; fecha de hoy, en texto secundario; campo de texto; las dos casillas debajo; botones abajo a la derecha.

## Accesibilidad

Al abrir, el foco va al campo de texto; Escape cierra; al cerrar, el foco vuelve al elemento que abrió el diálogo.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.