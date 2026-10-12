---
id: organismo-cabecera
tipo: componente
nivel: organismo
estado: sin revisar
---

# Organismo: cabecera

## Nivel

Organismo.

## Propósito

Situar al usuario en el proyecto y mostrar el estado del archivo abierto.

## Medidas

- Altura: 56 px.
- Fondo: color.surface.raised, con borde inferior color.border.default.

## Anatomía

- Nombre "reqly" como texto de marca a la izquierda.
- Selector de proyecto como botón secundario con el nombre del proyecto.
- Estado del archivo a la derecha.

## Estados del archivo

- "Sin guardar": con icono y texto en color.feedback.warning.text.
- "Guardado · commit <ID corto>": con icono y texto en color.feedback.success.text.

## Estados de proyecto

- Sin proyecto seleccionado: el selector dice "Elegir proyecto".
- Con proyecto: el selector muestra el nombre.

## Responsivo

En móvil, el selector muestra solo el icono y el nombre truncado; el estado del archivo se muestra debajo del nombre.

## Accesibilidad

- Los controles son botones con etiqueta.
- El orden de tabulación sigue el orden visual.
