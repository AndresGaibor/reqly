# Pendientes, supuestos y riesgos

Lista de los elementos [PENDIENTE] y [SUPUESTO] del diseño de reqly, con quién debe resolverlos.

## Supuestos

| ID | Descripción | Estado |
| --- | --- | --- |
| S-01 | Penpot y los tickets no son obligatorios para llegar a cero huecos, pero sí para ver el avance. | Aceptado |
| S-02 | El grafo visual de tickets queda fuera de v1. | Aceptado |
| S-03 | Si Penpot no responde o un frame no se puede mostrar, reqly muestra la referencia en texto. | Aceptado, confirmar al revisar |
| S-04 | Si la carpeta seleccionada no tiene documentos de reqly, reqly lo indica y no crea archivos. | Aceptado, confirmar al revisar |
| S-05 | reqly indica qué requisitos formales faltan por revisar. | Aceptado, confirmar al revisar |
| S-06 | En v1 no hay API propia para agentes: trabajan con los archivos del repo. | Aceptado, confirmar al revisar |
| S-07 | Los ADR entran en v1 y se crean por agente o por el usuario, como otros archivos del repo. Modo de edición por confirmar. | Por confirmar |
| S-08 | El avance cuenta solo los requisitos "debe". | Por confirmar |
| S-09 | La normativa no aplica en v1 por ser uso personal. | Por revisar con exportaciones |
| S-10 | El despliegue es un stack Docker Compose detrás de Traefik, con Sablier para escalar a cero. | Por confirmar al desplegar |
| S-11 | reqly se levanta al reiniciar la VM, sin intervención manual. | Por confirmar con la configuración de Sablier |
| S-12 | Si falla un commit al guardar, reqly conserva el archivo guardado en disco y muestra el error. | Por confirmar |

## Pendientes

| ID | Pendiente | Responde | Estado |
| --- | --- | --- | --- |
| P-01 | Cómo se da a reqly acceso a Penpot: token o usuario, y con qué permisos. | Usuario propietario | Abierto |
| P-02 | Qué identidad de git usa reqly para el usuario y para cada agente. Afecta al autor del historial. | Usuario propietario | Abierto |
| P-03 | Qué pasa si se pierde un dispositivo de la red Tailscale. | Usuario propietario | Abierto |
| P-04 | Proyecto de referencia y equipo para medir el rendimiento. | Usuario propietario | Abierto |
| P-05 | Si los pendientes y los supuestos cuentan en el avance. Cubre también si "debería" y "podría" cuentan. | Usuario propietario | Abierto |
| P-06 | Formato de los tickets y las pruebas dentro del repo: carpeta, nombre y campos del frontmatter. | Usuario propietario y diseño técnico | Abierto |
| P-07 | Herramienta de auditoría de accesibilidad y páginas que cubre. | Diseño técnico | Abierto |
| P-08 | Mecanismo para detectar cambios en disco. | Diseño técnico | Abierto |
| P-09 | Framework de interfaz además de React, y versiones exactas. | Diseño técnico | Abierto |
| P-10 | Formato de los documentos existentes que se migrarán en cada proyecto. | Usuario propietario, al migrar | Abierto |

## Riesgos y dependencias

- Penpot o Tailscale caídos: reqly muestra la referencia en texto y no se pierde ningún dato.
- Cambio de formato en las skills de Matt Pocock (versión 1.2.3) o en las del proyecto: se copian al repo con versión fijada, reqly avisa si algo no cuadra y el usuario decide cuándo actualizarlas.
- Agente que se detiene o pierde cuota a mitad de formalizar: lo escrito queda en un commit sin revisar, y al retomar continúa por bloques.
- Promociones de modelos gratuitos que terminan: el trabajo de los agentes depende de cuotas externas.
- Dependencias de terceros: Penpot, Tailscale, Docker, Traefik y Sablier del host, y los agentes de IA.