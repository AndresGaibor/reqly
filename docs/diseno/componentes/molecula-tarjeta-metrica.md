---
id: molecula-tarjeta-metrica
tipo: componente
nivel: molecula
estado: sin revisar
---

# Molécula: tarjeta de métrica

## Propósito

Mostrar un número de avance del proyecto.

## Anatomía

Etiqueta, valor grande (30 px), indicador (barra o icono) y texto de ayuda.

## Variantes

- huecos: si el valor es mayor que cero, valor en color.feedback.error con icono de advertencia; si es cero, valor en color.feedback.success.text con icono de verificado.
- avance: porcentaje grande y barra de progreso en color.interactive.default sobre color.border.default.
- pendientes: valor en color.feedback.warning.text.

## Estados

Cargando (esqueleto), vacío (valor cero con texto de explicación).

## Tokens que usa

Los indicados; radio de 8 px; relleno de 24 px.

## Reglas de uso

Los contadores de "debería" y "podría" van en tarjetas secundarias, marcados como no contables en el avance.
