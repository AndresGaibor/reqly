---
id: molecula-pestanas
tipo: componente
nivel: molecula
estado: sin revisar
---

# Molécula: pestañas

## Propósito

Cambiar entre vistas de un mismo tipo de elemento, por ejemplo tipos o estados.

## Anatomía

Fila horizontal de pestañas. Cada una con texto y, opcionalmente, un contador.

## Variantes

- activa: subrayado en color.interactive.default y texto color.text.primary
- inactiva: texto color.text.secondary

## Estados

- activa
- inactiva
- foco

## Tokens

- color.interactive.default
- color.text.primary
- color.text.secondary

## Accesibilidad

Se implementa como pestañas accesibles. La pestaña activa se indica también con un atributo de selección, no solo con color. Las flechas cambian de pestaña.

## Reglas de uso

Como máximo siete pestañas por fila. Más de siete pasan a un selector.