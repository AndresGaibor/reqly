---
id: CU-09-P17
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-09, CU-01]
requisitos: [RF-022, RF-028]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-09-P17 Skills del proyecto

## Propósito

Ver las skills instaladas en el proyecto, su versión y si se pueden actualizar.

## Requisitos

- RF-022
- RF-028

## Componentes

- plantilla-app-shell
- organismo-tabla (Skill, Versión instalada, Versión de reqly, Estado)
- atomo-insignia (instalada, actualizable, versión más nueva)
- atomo-boton (primario "Actualizar")
- atomo-banner (aviso de formato)

## Estados

- **principal**: tabla con las cinco skills de reqly y su estado.
- **actualizable**: la fila muestra el botón "Actualizar" activo.
- **versión más nueva**: banner de aviso "La versión instalada es más nueva; no se sobrescribe" (RF-028).
- **formato no válido**: banner de aviso que indica la skill con formato no válido; el resto de la tabla sigue visible (RF-022).
- **cargando**: filas en esqueleto.

## Disposición

Tabla arriba; banner de aviso, si aplica, encima de la tabla; botón "Actualizar" en la fila correspondiente.

## Accesibilidad

Cada botón indica su skill, por ejemplo "Actualizar reqly-formalizar"; el banner se anuncia al aparecer.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.