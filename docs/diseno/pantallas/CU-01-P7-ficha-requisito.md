---
id: CU-01-P7
tipo: pantalla
estado: sin revisar
casos_de_uso: [CU-01, CU-05]
requisitos: [RF-009, RF-014, RF-024]
penpot:
  archivo: pendiente
  pagina: pendiente
  frame: pendiente
---

# CU-01-P7 Ficha de requisito

## Propósito

Ver un requisito completo: criterios, casos de uso, diseño e historial.

## Requisitos

RF-009, RF-014, RF-024.

## Componentes

- plantilla-app-shell
- atomo-insignia, prioridad y estado
- atomo-boton, secundario, "Marcar como revisado"
- atomo-boton, primario, solo si el estado es formal
- atomo-banner, aviso de diseño no disponible

## Estados

- con diseño visible: la sección Diseño muestra la vista gráfica del frame.
- diseño no disponible: la sección Diseño muestra la referencia en texto "archivo · página · frame" y un banner de aviso; no hay botón de edición (RF-009).
- sin referencia: la sección Diseño no aparece.
- historial abierto: pestaña Historial activa con los commits del requisito.

## Disposición

Plantilla plantilla-app-shell. Encabezado con ID, título y las insignias de prioridad y estado. Debajo, criterios en lista Dado / Cuando / Entonces. Después, casos de uso enlazados. Después, la sección Diseño. Pestañas Detalle e Historial.

## Accesibilidad

Las pestañas siguen el patrón de pestañas accesibles con teclado. La vista gráfica del diseño tiene un texto alternativo con la referencia.

## Penpot

Archivo pendiente, página pendiente, frame pendiente.