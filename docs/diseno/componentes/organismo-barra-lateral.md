---
id: organismo-barra-lateral
tipo: componente
nivel: organismo
estado: sin revisar
---

# Organismo: barra lateral

## Nivel

Organismo.

## Propósito

Navegar entre las secciones de reqly.

## Anchos

- 240 px desde 1024 px de ancho de pantalla.
- Contraída a 64 px, solo iconos, entre 768 y 1023 px.
- En pantallas menores, se abre como menú desplegable.

## Elementos

En este orden:

1. Avance
2. Matriz
3. Documentos
4. Requisitos
5. Casos de uso
6. Pendientes
7. Glosario
8. Decisiones
9. Diseño
10. Skills

## Elemento activo

- Fondo color.interactive.default con 10% de opacidad.
- Texto color.interactive.default.
- Marca de la sección actual con aria-current.

En el elemento Avance se muestra el número de huecos como insignia de tipo hueco, si hay huecos.

## Accesibilidad

- Navegable con teclado.
- El orden de tabulación sigue el orden de la lista.
- Cada icono tiene etiqueta de texto visible o accesible.
