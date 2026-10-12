---
id: CU-02-P14
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-02]
requisitos: [RF-012, RF-013]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-02-P14 Captura de requerimiento

## Propósito

Escribir un requerimiento en texto libre y seguir su estado hasta que se formaliza.

## Requisitos

- RF-012
- RF-013

## Componentes

- plantilla-app-shell, variante de dos paneles
- molecula-elemento-lista: lista de requerimientos
- atomo-insignia: abierto, formalizado
- atomo-campo: área de texto larga, etiqueta "Qué quieres que haga reqly"
- atomo-boton: primario "Guardar requerimiento"

## Estados

- nuevo: campo vacío; el botón está inactivo hasta escribir.
- abierto: el requerimiento guardado con insignia abierto.
- formalizado: el requerimiento con insignia formalizado y una sección "Requisitos creados" con enlaces a cada requisito y caso de uso.
- vacío: "Todavía no hay requerimientos".
- cargando: lista en esqueleto.

## Disposición

A la izquierda, la lista de requerimientos con su insignia; a la derecha, el formulario o el detalle del requerimiento elegido. En móvil, la lista y el detalle se alternan.

## Accesibilidad

El campo tiene etiqueta visible; la lista tiene un encabezado con el número de requerimientos.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.