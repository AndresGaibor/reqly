---
id: CU-08-P10
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-08]
requisitos: [RF-011]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-08-P10 Glosario

## Propósito

Consultar los términos del proyecto con su definición y sus sinónimos rechazados.

## Requisitos

- RF-011

## Componentes

- plantilla-app-shell
- atomo-campo (buscador)
- molecula-elemento-lista (un elemento por término)

## Estados

- principal: lista de términos en orden alfabético.
- sin resultados: el buscador no coincide con ningún término.
- vacío: el proyecto no tiene glosario; texto "Este proyecto no tiene glosario".
- cargando: lista en esqueleto.

## Disposición

Buscador arriba; cada término como título de nivel 3, con su definición debajo y, en texto secundario, la línea "Evitar: ..." con los sinónimos rechazados. La pantalla se construye sobre plantilla-app-shell.

## Accesibilidad

Cada término es un encabezado; el buscador tiene etiqueta visible.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.
