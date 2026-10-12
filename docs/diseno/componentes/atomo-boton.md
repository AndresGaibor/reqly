---
id: atomo-boton
tipo: componente
nivel: atomo
estado: sin revisar
---

# Átomo: botón

## Propósito

Iniciar una acción.

## Cuándo no usarlo

Para navegar a otra pantalla; en ese caso usa un enlace.

## Anatomía

Contenedor, etiqueta de texto e icono opcional.

## Variantes

- primario: fondo color.interactive.default, texto color.text.on-interactive.
- secundario: borde color.border.default, texto color.text.primary.

## Tamaños

md, de 40 px de alto; en móvil, de 44 px.

## Estados

Por defecto, al pasar el cursor (hover), foco, deshabilitado.

## Propiedades

variante, tamaño, deshabilitado, icono.

## Tokens que usa

color.interactive.default, color.interactive.hover, color.text.on-interactive, color.border.default, color.text.primary; radio de 8 px; relleno horizontal de 16 px.

## Accesibilidad

Se implementa como elemento button; el anillo de foco es visible; el texto deshabilitado puede tener menor contraste, pero debe seguir legible.

## Reglas de uso

Como máximo un botón primario por sección.
