---
id: CU-04-P12
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-04]
requisitos: [RF-010, RF-015]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-04-P12 Pendientes y supuestos

## Propósito

Ver las notas marcadas como pendiente o pregunta, y los elementos [PENDIENTE] y [SUPUESTO] del proyecto.

## Requisitos

- RF-010
- RF-015

## Componentes

- plantilla-app-shell
- molecula-pestanas (Notas, Pendientes y supuestos)
- molecula-elemento-lista
- atomo-insignia (tipos: pendiente, pregunta, supuesto)
- atomo-campo (filtro por estado)

## Estados

- principal: lista de elementos abiertos.
- resueltos: el filtro muestra los elementos resueltos o descartados.
- vacío: "Sin pendientes abiertos".
- cargando: lista en esqueleto.

## Disposición

Pestañas arriba; filtro por estado a la derecha; lista de elementos, cada uno con su texto, su insignia de tipo, la fecha y el elemento de origen como enlace. La pantalla se construye sobre plantilla-app-shell.

## Accesibilidad

Cada elemento enlaza a su origen; el filtro tiene etiqueta visible.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.
