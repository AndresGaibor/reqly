---
id: molecula-elemento-lista
tipo: componente
nivel: molecula
estado: sin revisar
---

# Molécula: elemento de lista

## Propósito

Mostrar un elemento en una lista: término, nota, decisión, pendiente o requerimiento.

## Anatomía

Título (enlace), línea de metadatos (ID, fecha u origen) en color.text.secondary, insignia opcional a la derecha.

## Estados

- por defecto
- al pasar el cursor: fondo color.background.default
- seleccionado: borde en color.interactive.default
- foco

## Tokens

- color.text.primary
- color.text.secondary
- color.background.default
- color.interactive.default
- radio de 8 px
- relleno de 16 px

## Accesibilidad

El título es un enlace. Los metadatos se leen en el mismo orden visual.

## Reglas de uso

No mezclar más de dos metadatos en la línea.