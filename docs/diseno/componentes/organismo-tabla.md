---
id: organismo-tabla
tipo: componente
nivel: organismo
estado: sin revisar
---

# Organismo: tabla

## Propósito

Mostrar elementos en filas y columnas.

## Anatomía

Encabezados de columna (con botón de orden), filas, celdas y, opcional, una barra de pie con el número de filas.

## Variantes

- estándar
- con selección: casilla al inicio de cada fila

## Estados

- cargando: filas en esqueleto
- vacía: texto explicativo
- sin resultados de filtro: texto "Ningún elemento cumple el filtro"

## Tokens

- color.surface.raised
- color.border.default
- color.text.primary
- color.text.secondary

## Accesibilidad

Encabezados de columna. El orden activo se indica con un atributo de orden, no solo con color. Cada fila enlaza a su elemento.

## Reglas de uso

En escritorio, la primera columna queda fija al desplazarse. En móvil, cada fila se convierte en una tarjeta con las mismas etiquetas de columna.