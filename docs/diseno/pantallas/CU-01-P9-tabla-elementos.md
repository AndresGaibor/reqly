---
id: CU-01-P9
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01]
requisitos: [RF-004]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P9 Tabla de elementos

## Propósito

Ver requisitos, casos de uso, tickets y pruebas en una tabla, con su ID, prioridad, estado y relaciones.

## Requisitos

- RF-004

## Componentes

- plantilla-app-shell
- molecula-pestanas (Requisitos, Casos de uso, Tickets, Pruebas)
- atomo-campo (buscador)
- atomo-boton (secundario "Limpiar filtros")
- organismo-tabla

## Estados

- principal: tabla con las filas del tipo activo.
- sin resultados: el buscador no coincide con ningún elemento; texto "Ningún elemento cumple el filtro".
- cargando: filas en esqueleto.
- vacío: el tipo activo no tiene elementos.

## Disposición

Pestañas arriba; debajo, el buscador y el botón "Limpiar filtros"; la tabla con columnas ID, Título, Prioridad, Estado y Relaciones; orden por ID por defecto. La pantalla se construye sobre plantilla-app-shell. En móvil, cada fila pasa a tarjeta.

## Accesibilidad

Encabezados de columna con orden indicado por atributo; cada ID enlaza a su ficha.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.
