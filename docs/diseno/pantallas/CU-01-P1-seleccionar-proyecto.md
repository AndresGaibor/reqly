---
id: CU-01-P1
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01]
requisitos: [RF-001, RF-028]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P1 Seleccionar proyecto

## Propósito

Elegir un proyecto registrado o registrar una carpeta nueva.

## Requisitos

RF-001, RF-028.

## Componentes

- plantilla-app-shell
- atomo-boton, primario, con el texto "Registrar carpeta"
- atomo-banner

## Estados

- principal: lista de tarjetas de proyecto, con nombre, ruta y último commit.
- vacío: texto que explica qué es un proyecto, con el botón "Registrar carpeta".
- cargando: tarjetas en esqueleto.
- error: banner de aviso "La carpeta no tiene documentos de reqly. No se crea ningún archivo."
- instalando skills: lista de las skills de reqly con su versión y su estado (instalada, actualizada, o aviso porque la versión instalada es más nueva).
- ID duplicado: banner de error que muestra el ID repetido y los dos archivos que lo tienen. El proyecto muestra el error y no oculta el resto (RF-017).

## Disposición

Plantilla plantilla-app-shell. Título "Proyectos". Botón primario "Registrar carpeta" alineado a la derecha. Lista de tarjetas en columna.

## Accesibilidad

Cada tarjeta es un enlace con su nombre. El banner de error se anuncia al aparecer.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.