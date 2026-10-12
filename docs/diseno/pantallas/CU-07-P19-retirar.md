---
id: CU-07-P19
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-07, CU-02]
requisitos: [RF-019]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-07-P19 Retirar elemento

## Propósito

Retirar un requisito, un ticket u otro elemento sin borrarlo.

## Requisitos

- RF-019

## Componentes

- organismo-dialogo
- atomo-boton (primario "Retirar"; secundario "Cancelar")
- atomo-banner (información: "El archivo se conserva en el repositorio")

## Estados

- **confirmación**: título "Retirar RF-005", texto que explica el cambio de estado y que el archivo se conserva.
- **retirado**: confirmación breve; el elemento sale de la vista principal.
- **error**: banner de error "No se pudo retirar el elemento"; el estado no cambia.

## Disposición

Diálogo centrado; texto explicativo; botones abajo a la derecha. El botón "Retirar" no usa rojo, porque no borra.

## Accesibilidad

Al abrir, el foco va a "Cancelar"; Escape cierra; el foco vuelve al elemento que lo abrió.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.