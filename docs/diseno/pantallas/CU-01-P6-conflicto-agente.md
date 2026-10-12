---
id: CU-01-P6
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01, CU-03]
requisitos: [RF-008, RF-007]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P6 Conflicto con un agente

## Propósito

Resolver un cambio hecho por un agente mientras el usuario editaba el mismo archivo.

## Requisitos

RF-008, RF-007.

## Componentes

- plantilla-app-shell, variante de dos paneles
- atomo-banner, aviso
- atomo-boton, primario, "Combinar a mano"
- atomo-boton, secundario, "Conservar la mía"
- atomo-boton, secundario, "Conservar la del disco"

## Estados

- principal: banner de aviso "Un agente cambió este archivo en disco"; dos columnas, "Tu versión" y "Versión del disco"; tres botones.
- resuelto: después de elegir, el archivo se guarda con commit y la pantalla vuelve al editor.

## Disposición

Plantilla plantilla-app-shell. Banner arriba. Dos columnas de igual ancho con sus encabezados. Botones debajo de cada columna y el botón de combinar a mano en el centro.

## Accesibilidad

Cada columna tiene su encabezado. El banner se anuncia al aparecer. Nada se sobrescribe sin una elección del usuario.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.