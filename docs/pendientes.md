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
| S-07 | Los ADR entran en v1 y se crean y leen desde reqly. Se editan con el editor de Markdown; un ADR aceptado se reemplaza, no se reescribe. | Decidido |
| S-08 | El avance cuenta los requisitos "debe" (RF y RNF) no retirados con ticket hecho. | Decidido |
| S-09 | La normativa no aplica en v1 por ser uso personal. | Por revisar con exportaciones |
| S-10 | El despliegue es un stack Docker Compose detrás de Traefik, con Sablier para escalar a cero. | Por confirmar al desplegar |
| S-11 | reqly se levanta al reiniciar la VM, sin intervención manual. | Por confirmar con la configuración de Sablier |
| S-12 | Si falla un commit al guardar, reqly conserva el archivo guardado en disco y muestra el error. | Por confirmar |
| S-13 | Los requerimientos usan el ID REQ-### con el siguiente número libre. | Confirmado |
| S-14 | La migración y la formalización trabajan en bloques de hasta 5 elementos. | Confirmado |
| S-15 | to-spec de Matt no se copia: reqly-formalizar cubre la especificación. | Decidido |
| S-16 | Los tokens viven en docs/diseno/tokens.json en formato DTCG, y Penpot los importa. El repo es la fuente. | Confirmado |
| S-17 | El diseño va en el archivo de Penpot conectado: páginas nuevas para la biblioteca (Foundations, Atoms, Molecules, Organisms, Templates) y una página por flujo. Las páginas existentes (Prueba, Design System, Componentes) no se tocan. | Confirmado |

## Pendientes

| ID | Pendiente | Responde | Estado |
| --- | --- | --- | --- |
| P-01 | Cómo se da a reqly acceso a Penpot: token o usuario, y con qué permisos. | Usuario propietario | Abierto |
| P-02 | Qué identidad de git usa reqly para el usuario y para cada agente. Afecta al autor del historial. | Usuario propietario | Abierto |
| P-03 | Qué pasa si se pierde un dispositivo de la red Tailscale. | Usuario propietario | Abierto |
| P-04 | Proyecto de referencia y equipo para medir el rendimiento. | Usuario propietario | Abierto |
| P-05 | Si los pendientes y los supuestos cuentan en el avance. Cubre también si "debería" y "podría" cuentan. | Usuario propietario | Resuelto |
| P-06 | Formato de los tickets y las pruebas dentro del repo: carpeta, nombre y campos del frontmatter. | Usuario propietario y diseño técnico | Abierto |
| P-07 | Herramienta de auditoría de accesibilidad y páginas que cubre. | Diseño técnico | Abierto |
| P-08 | Mecanismo para detectar cambios en disco. | Diseño técnico | Abierto |
| P-09 | Framework de interfaz además de React, y versiones exactas. | Diseño técnico | Abierto |
| P-10 | Formato de los documentos existentes que se migrarán en cada proyecto. | Usuario propietario, al migrar | Abierto |
| P-11 | Mecanismo para actualizar una skill fijada en el repo (CU-09). | Diseño técnico | Abierto |
| P-12 | Esquema definitivo de IDs para requerimientos (REQ-###) y tamaño de bloque en la migración y la formalización. | Usuario propietario | Resuelto |
| P-13 | Probar reqly-formalizar con un requerimiento real que aporte el usuario. | Usuario propietario | Descartado |
| P-14 | Adaptar to-tickets para que escriba en archivos del repo. Depende de P-06. | Diseño técnico | Abierto |
| P-15 | Confirmar que la versión de Penpot instalada importa tokens.json sin errores. | Diseño técnico | Abierto |
| P-16 | Acceso del agente a Penpot para diseñar. | Usuario propietario | Resuelto: el MCP de Penpot responde con el proyecto conectado. |
| P-17 | Usar el archivo de Penpot conectado para la biblioteca y las pantallas; las páginas existentes no se tocan. | Usuario propietario | Resuelto |
| P-18 | Primer caso de uso a diseñar: CU-01. | Usuario propietario | Resuelto |

## Riesgos y dependencias

- Penpot o Tailscale caídos: reqly muestra la referencia en texto y no se pierde ningún dato.
- Cambio de formato en las skills de Matt Pocock (versión 1.2.3) o en las del proyecto: se copian al repo con versión fijada, reqly avisa si algo no cuadra y el usuario decide cuándo actualizarlas.
- Agente que se detiene o pierde cuota a mitad de formalizar: lo escrito queda en un commit sin revisar, y al retomar continúa por bloques.
- Promociones de modelos gratuitos que terminan: el trabajo de los agentes depende de cuotas externas.
- Dependencias de terceros: Penpot, Tailscale, Docker, Traefik y Sablier del host, y los agentes de IA.