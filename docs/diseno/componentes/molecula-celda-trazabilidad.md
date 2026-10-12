---
id: molecula-celda-trazabilidad
tipo: componente
nivel: molecula
estado: sin revisar
---

# Molécula: celda de trazabilidad

## Nivel

Molécula.

## Propósito

Mostrar si un requisito está enlazado a un caso de uso, un diseño, un ticket o una prueba.

## Anatomía

- Icono.
- ID en fuente monoespaciada (color.text.secondary) o texto "Hueco".
- Fondo de color.surface.raised.

## Variantes

- Enlazada: icono de verificado en color.feedback.success.fill y el ID del elemento.
- Hueco: icono de advertencia en color.feedback.error y el texto "Hueco" en color.feedback.error.
- No aplica: texto "No aplica" en color.text.secondary, sin icono; se usa en los RNF sin caso de uso.

## Estados

- Por defecto.
- Foco (si la celda es un enlace).

## Tokens

Los indicados en la anatomía y en las variantes; radio de 4 px.

## Accesibilidad

- El icono y el texto van juntos.
- El ID es un enlace con anillo de foco.

## Reglas de uso

- Nunca mostrar solo el color para indicar un hueco.
