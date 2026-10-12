---
id: plantilla-app-shell
tipo: plantilla
estado: sin revisar
---

# Plantilla: estructura de aplicación

## Propósito

Estructura común de todas las pantallas de reqly.

## Partes

- Cabecera (organismo-cabecera).
- Barra lateral (organismo-barra-lateral).
- Área de contenido.

## Área de contenido

- Ancho máximo de 1200 px, centrada.
- Margen lateral de 16 px en móvil y 24 px en escritorio.

## Breakpoints

- 1024 px: barra lateral fija.
- 768 px: barra contraída.
- Menos de 768 px: menú desplegable.

## Variantes

- Estándar (una columna).
- De dos paneles (editor y vista previa, en escritorio; pestañas en móvil).

## Estados

- Cargando: esqueleto del área de contenido, sin esqueleto de cabecera.
- Error de carga: banner de error en el área de contenido, con botón para reintentar.

## Reglas de uso

- La cabecera y la barra lateral no se desplazan con el contenido.
- Cada pantalla indica dónde está el usuario en el título de su área.
