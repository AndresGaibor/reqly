# Cobertura del diseño

Qué requisito y qué caso de uso tiene pantalla o flujo. Un requisito sin pantalla no es un error si el requisito no tiene interfaz; se indica como 'sin pantalla' con la razón.

## Requisitos funcionales

| Requisito | Pantallas | Notas |
| --- | --- | --- |
| RF-001 | CU-01-P1 | Carga de la carpeta. |
| RF-002 | CU-01-P2 | Avance y huecos. |
| RF-003 | CU-01-P4 | Documento continuo. |
| RF-004 | CU-01-P9 | Tabla de elementos. |
| RF-005 | CU-01-P3 | Matriz de trazabilidad. |
| RF-006 | CU-01-P5 | Editor con vista previa. |
| RF-007 | CU-01-P5, CU-01-P6, CU-04-P13, CU-07-P16, CU-06-P18, CU-08-P11 | Commit por guardado en cada pantalla que guarda. |
| RF-008 | CU-01-P6 | Conflicto con agente. |
| RF-009 | CU-01-P7, CU-05-P20 | Diseño en solo lectura. |
| RF-010 | CU-01-P2, CU-04-P12 | Pendientes y supuestos. |
| RF-011 | CU-08-P10 | Glosario. |
| RF-012 | CU-02-P14 | Captura de requerimiento. |
| RF-013 | CU-02-P14 | Formalización visible como estado formalizado. La formalización la hace el agente. |
| RF-014 | CU-01-P7, CU-02-P15 | Marcar como revisado. |
| RF-015 | CU-04-P13, CU-04-P12, CU-06-P18 | Notas y su marca. |
| RF-016 | CU-01-P5, CU-02-P15 | Validación y advertencias. |
| RF-017 | CU-01-P1 | ID duplicado. |
| RF-018 | CU-07-P16 | Estados y transiciones. |
| RF-019 | CU-07-P19 | Retirar sin borrar. |
| RF-020 | CU-07-P16 | Tickets por estado. |
| RF-021 | CU-06-P18 | Migración por bloques. |
| RF-022 | CU-09-P17 | Versión de las skills. |
| RF-023 | CU-08-P11 | Decisiones (ADR). |
| RF-024 | CU-01-P7, CU-01-P8 | Historial. |
| RF-025 | sin pantalla | Fuera de v1: diagramas Mermaid y HTML animado. |
| RF-026 | sin pantalla | Fuera de v1: exportación a Word o PDF. |
| RF-027 | sin pantalla | Fuera de v1: grafo visual de tickets. |
| RF-028 | CU-01-P1, CU-09-P17 | Instalación de skills al seleccionar el proyecto. |
| RF-029 | sin pantalla en reqly | Proceso del agente en Penpot: lo guía reqly-disenar; el resultado está en este directorio. |

## Requisitos no funcionales

| Requisito | Pantallas | Notas |
| --- | --- | --- |
| RNF-001 | sin pantalla propia | Rendimiento: aplica a CU-01-P2, CU-01-P4 y P9. |
| RNF-002 | sin pantalla | Acceso solo por Tailscale. |
| RNF-003 | CU-01-P1 | Aplica al registrar carpetas. |
| RNF-004 | sin pantalla | Privacidad: sin envíos externos. |
| RNF-005 | CU-01-P8 | Historial de git. |
| RNF-006 | todas | Idioma español. |
| RNF-007 | fundamentos.md y componentes/ | Accesibilidad WCAG 2.2 AA. |
| RNF-008 | sin pantalla | Arranque tras reinicio. |
| RNF-009 | sin pantalla | Despliegue. |
| RNF-010 | sin pantalla | Stack obligatorio. |

## Casos de uso

| Caso de uso | Flujo | Notas |
| --- | --- | --- |
| CU-01 | flujos/CU-01-revisar-estado.md | Principal. |
| CU-02 | flujos/CU-02-capturar-formalizar.md | Opcional. |
| CU-03 | flujos/CU-03-conflicto-agente.md | Conflicto. |
| CU-04 | flujos/CU-04-nota-pendiente.md | Notas. |
| CU-05 | flujos/CU-05-ver-diseno.md | Diseño de un requisito. |
| CU-06 | flujos/CU-06-migracion-bloques.md | Migración. |
| CU-07 | flujos/CU-07-estado-ticket.md | Tickets. |
| CU-08 | flujos/CU-08-glosario-decisiones.md | Glosario y decisiones. |
| CU-09 | flujos/CU-09-mantener-skills.md | Skills. |
| CU-10 | sin flujo en reqly | Diseñar pantallas: lo hace el agente con reqly-disenar; el resultado está en este directorio. |

## Huecos de diseño

- Ningún requisito funcional de v1 queda sin pantalla, salvo RF-029, que es un proceso del agente.
- Los requisitos no funcionales sin pantalla propia se verifican con sus criterios, no con una pantalla.
