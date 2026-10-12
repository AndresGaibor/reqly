---
id: organismo-dialogo
tipo: componente
nivel: organismo
estado: sin revisar
---

# Organismo: diálogo

## Propósito

Pedir una confirmación o un dato sin salir de la pantalla.

## Anatomía

Título, texto explicativo, contenido opcional, botón secundario a la izquierda y botón primario a la derecha.

## Tamaño

480 px de ancho en escritorio. En móvil ocupa toda la pantalla.

## Estados

- abierto
- cargando: botón primario en estado de carga
- error: banner de error dentro del diálogo

## Tokens

- color.surface.raised
- color.border.default
- color.text.primary
- radio de 12 px

## Accesibilidad

Al abrir, el foco va al botón secundario. Escape cierra el diálogo. Al cerrar, el foco vuelve al elemento que lo abrió.

## Reglas de uso

Solo un diálogo abierto a la vez.