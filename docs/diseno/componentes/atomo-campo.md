---
id: atomo-campo
tipo: componente
nivel: atomo
estado: sin revisar
---

# Átomo: campo

## Propósito

Recoger texto o una elección.

## Anatomía

Etiqueta visible encima del campo, campo, texto de ayuda o de error debajo.

## Variantes

- texto de una línea
- área de texto para texto largo
- casilla de verificación con etiqueta a la derecha

## Estados

- vacío
- con texto
- error: borde en color.feedback.error y texto de error debajo
- deshabilitado
- foco: anillo de color.interactive.default

## Tokens

- color.border.default
- color.interactive.default
- color.feedback.error
- color.text.primary
- radio de 4 px
- relleno de 12 px

## Accesibilidad

La etiqueta siempre visible y asociada al campo. El texto de error se anuncia al aparecer.

## Reglas de uso

Nunca usar el texto de ejemplo como etiqueta.