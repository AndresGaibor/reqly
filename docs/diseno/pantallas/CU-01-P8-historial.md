---
id: CU-01-P8
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01]
requisitos: [RF-024, RNF-005]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P8 Historial

## Propósito

Ver los cambios de un elemento, con fecha, autor y resumen.

## Requisitos

RF-024, RNF-005.

## Componentes

- plantilla-app-shell
- atomo-insignia, tipo de autor: usuario o agente
- texto en fuente monoespaciada para los IDs de commit

## Estados

- principal: lista de cambios, del más reciente al más antiguo.
- vacío: texto "Sin cambios registrados".
- cargando: lista en esqueleto.

## Disposición

Plantilla plantilla-app-shell. Lista vertical. Cada entrada tiene fecha, autor, resumen y el ID corto del commit.

## Accesibilidad

La lista es una lista ordenada. La fecha se lee en formato completo para lectores de pantalla.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.