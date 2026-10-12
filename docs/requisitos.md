# Requisitos de reqly

Requisitos funcionales (RF) y no funcionales (RNF) de reqly v1. Prioridad según MoSCoW: Debe, Debería, Podría o No por ahora.

## Requisitos funcionales

### RF-001 Cargar un proyecto
Descripción: el usuario selecciona una carpeta del host y reqly carga los documentos Markdown del proyecto.
Prioridad: Debe
Criterios de aceptación:
- Dada una carpeta con documentos de reqly, Cuando el usuario la selecciona, Entonces reqly muestra los documentos sin pedir más datos.
- Dada una carpeta sin documentos de reqly, Cuando el usuario la selecciona, Entonces reqly lo indica y no crea ningún archivo.

### RF-002 Mostrar avance y huecos
Descripción: reqly muestra el número de huecos de trazabilidad y el avance del proyecto, con la lista de elementos afectados.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito "debe" sin caso de uso, Cuando el usuario abre el panel de avance, Entonces el requisito aparece en la lista de huecos y el número de huecos es al menos 1.

### RF-003 Ver documentos como documento continuo
Descripción: reqly une varios documentos del proyecto en una vista continua con índice lateral.
Prioridad: Debe
Criterios de aceptación:
- Dado un proyecto con tres documentos, Cuando el usuario abre la vista de documento, Entonces los tres aparecen en orden con un índice lateral que lleva a cada sección.

### RF-004 Ver elementos en tabla
Descripción: reqly muestra cada elemento en una tabla con id, prioridad, estado y relaciones, leídos del frontmatter.
Prioridad: Debe
Criterios de aceptación:
- Dado requisitos con frontmatter de id, prioridad y estado, Cuando el usuario abre la vista de tabla, Entonces cada fila muestra esos campos y sus relaciones.

### RF-005 Matriz de trazabilidad con huecos
Descripción: reqly muestra la matriz que une requisito, caso de uso, diseño, ticket y prueba, y marca los huecos.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito "debe" sin caso de uso, Cuando el usuario abre la matriz, Entonces la celda de caso de uso de ese requisito aparece marcada como hueco.

### RF-006 Editar Markdown con vista previa
Descripción: el usuario edita un documento y ve la vista previa antes de guardar.
Prioridad: Debe
Criterios de aceptación:
- Dado un documento abierto, Cuando el usuario edita el texto y activa la vista previa, Entonces la vista previa muestra el texto editado y el archivo en disco no cambia hasta guardar.

### RF-007 Commit automático por guardado
Descripción: cada guardado crea un commit con un mensaje generado a partir del archivo cambiado.
Prioridad: Debe
Criterios de aceptación:
- Dado un archivo guardado desde reqly, Cuando el guardado termina, Entonces existe un commit nuevo que contiene solo ese archivo y su mensaje nombra el archivo.

### RF-008 Detectar conflictos con agentes
Descripción: si un agente cambia en disco un archivo que el usuario está editando, reqly no guarda y muestra ambas versiones.
Prioridad: Debe
Criterios de aceptación:
- Dado que el usuario edita un archivo y un agente lo cambia en disco, Cuando el usuario intenta guardar, Entonces reqly no guarda y muestra la versión del usuario y la del disco lado a lado.

### RF-009 Ver el diseño de Penpot en solo lectura
Descripción: un requisito puede tener una referencia de diseño a Penpot. reqly muestra la vista gráfica del frame o, si no es posible, la referencia en texto.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito con referencia a un frame accesible de Penpot, Cuando el usuario abre el requisito, Entonces reqly muestra la vista gráfica del frame.
- Dado un requisito con referencia a un frame que no se puede mostrar, Cuando el usuario abre el requisito, Entonces reqly muestra la referencia en texto con archivo, página y frame, sin opciones de edición.

### RF-010 Lista de pendientes y supuestos
Descripción: reqly muestra las notas marcadas como pendiente o pregunta, y los elementos [PENDIENTE] y [SUPUESTO] del proyecto.
Prioridad: Debe
Criterios de aceptación:
- Dada una nota marcada como pendiente en un requisito, Cuando el usuario abre la lista de pendientes, Entonces la nota aparece junto al requisito al que pertenece.

### RF-011 Ver el glosario
Descripción: reqly muestra los términos del glosario del proyecto con su definición y sus sinónimos rechazados.
Prioridad: Debe
Criterios de aceptación:
- Dado un GLOSSARY.md con tres términos, Cuando el usuario abre el glosario, Entonces aparecen los tres con su definición y sus sinónimos rechazados.

### RF-012 Capturar un requerimiento
Descripción: el usuario escribe un requerimiento en texto libre, sin ID ni criterios.
Prioridad: Debe
Criterios de aceptación:
- Dado un requerimiento escrito sin ID, Cuando el usuario lo guarda, Entonces queda con estado abierto y no se exigen criterios.

### RF-013 Formalizar un requerimiento con un agente
Descripción: el proyecto incluye una skill que guía al agente para convertir un requerimiento abierto en requisitos formales y casos de uso, y enlazarlos al requerimiento.
Prioridad: Debe
Criterios de aceptación:
- Dado un requerimiento abierto, Cuando el agente aplica la skill, Entonces crea requisitos con ID y criterios, crea casos de uso y deja los requisitos en estado formal.
- Dado que el agente termina la formalización, Cuando la formalización acaba, Entonces el requerimiento pasa a formalizado y enlaza los requisitos creados.

### RF-014 Revisar requisitos formales
Descripción: el usuario marca un requisito formal como revisado.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito en estado formal, Cuando el usuario lo marca como revisado, Entonces su estado pasa a revisado y deja de aparecer como pendiente de revisión.

### RF-015 Añadir notas
Descripción: el usuario añade notas libres con fecha a un requerimiento, un requisito o un caso de uso, y puede marcarlas como pregunta o como pendiente.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito abierto, Cuando el usuario añade una nota marcada como pendiente, Entonces la nota aparece en la ficha del requisito y en la lista de pendientes.

### RF-016 Validar al guardar
Descripción: al guardar, reqly valida los campos obligatorios y el formato. Si fallan, bloquea el guardado con aviso. Las referencias rotas se avisan, pero el guardado se hace.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito sin criterios, Cuando el usuario guarda, Entonces reqly no guarda y muestra el campo que falta.
- Dado un caso de uso que cita un RF que no existe, Cuando el usuario guarda, Entonces reqly guarda y muestra una advertencia con la referencia rota.

### RF-017 Identificadores únicos
Descripción: los IDs RF-### y RNF-### son únicos y permanentes. Al formalizar, el agente usa el siguiente número libre. reqly verifica que no haya duplicados.
Prioridad: Debe
Criterios de aceptación:
- Dado que existe RF-004, Cuando el agente formaliza un nuevo requisito, Entonces el requisito recibe el siguiente número libre, sin reutilizar IDs retirados.
- Dado dos archivos con el mismo ID, Cuando reqly carga el proyecto, Entonces muestra un error de ID duplicado que identifica ambos archivos.

### RF-018 Estados de los elementos
Descripción: cada tipo de elemento tiene sus estados y solo se permiten las transiciones definidas en las reglas de negocio.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito en estado retirado, Cuando el usuario intenta cambiarlo a formal, Entonces reqly rechaza la transición.

### RF-019 No borrar elementos
Descripción: reqly no borra elementos. Retirar un elemento es cambiar su estado.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito retirado, Cuando el usuario abre la vista principal, Entonces el requisito no aparece y su archivo sigue en el repo.

### RF-020 Tickets y pruebas como archivos del repo
Descripción: un agente crea tickets y pruebas como archivos del repo a partir de requisitos formales. El usuario y el agente pueden cambiar el estado de un ticket, y cada cambio es un commit.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito formal, Cuando el agente crea tickets, Entonces existe un archivo por ticket enlazado al requisito.
- Dado un ticket en curso, Cuando el agente cambia su estado a hecho, Entonces el cambio queda en un commit.

### RF-021 Migrar documentos y código existentes
Descripción: el proyecto incluye una skill que guía al agente para migrar documentos existentes y, si el usuario lo pide, código, a requerimientos. Trabaja por bloques y el usuario revisa cada bloque antes de seguir.
Prioridad: Debe
Criterios de aceptación:
- Dado un repo con documentos Markdown existentes, Cuando el agente aplica la skill, Entonces propone requerimientos por bloques.
- Dado un bloque propuesto sin revisar, Cuando el agente termina el bloque, Entonces no avanza al siguiente hasta que el usuario lo revisa.

### RF-022 Skills del proyecto con versión fijada
Descripción: las skills del proyecto y las de Matt Pocock se copian al repo con versión fijada. reqly muestra la versión instalada y valida el formato al cargar.
Prioridad: Debe
Criterios de aceptación:
- Dada una skill copiada en el repo, Cuando reqly carga el proyecto, Entonces muestra la versión instalada.
- Dado un archivo que no cumple el formato esperado, Cuando reqly carga el proyecto, Entonces muestra un aviso y el resto del proyecto sigue visible.

### RF-023 Registros de decisión (ADR)
Descripción: reqly muestra los ADR de docs/adr/ en orden numérico. El modo de edición está por confirmar (ver docs/pendientes.md, S-07).
Prioridad: Debe
Criterios de aceptación:
- Dado docs/adr con dos registros, Cuando el usuario abre la vista de decisiones, Entonces se listan en orden numérico con título y estado.

### RF-024 Historial por elemento
Descripción: reqly muestra el historial de commits que tocan el archivo de un elemento: fecha, autor del commit y resumen.
Prioridad: Debe
Criterios de aceptación:
- Dado un requisito con tres commits, Cuando el usuario abre su historial, Entonces aparecen los tres con fecha, autor y resumen.

## Fuera de v1

### RF-025 Diagramas Mermaid y HTML animado
Descripción: render de diagramas Mermaid y de archivos HTML animados dentro del documento.
Prioridad: No por ahora
Criterios de aceptación: Sin criterios en v1; se definen al entrar en alcance.

### RF-026 Exportar a Word o PDF
Descripción: exportar un documento o el proyecto a Word o PDF para entregar a clientes.
Prioridad: No por ahora
Criterios de aceptación: Sin criterios en v1; se definen al entrar en alcance.

### RF-027 Grafo visual de tickets
Descripción: grafo de tickets con sus dependencias.
Prioridad: No por ahora
Criterios de aceptación: Sin criterios en v1; se definen al entrar en alcance.

## Requisitos no funcionales

### RNF-001 Rendimiento
Descripción: reqly carga proyectos de hasta 500 archivos Markdown con tiempos acotados, medidos en la red de Tailscale.
Prioridad: Debe
Criterios de aceptación:
- Dado un proyecto de 500 archivos, Cuando el usuario lo abre por primera vez en la red de Tailscale, Entonces la carga inicial termina en menos de 3 segundos.
- Dado un proyecto abierto, Cuando el usuario pasa de un documento a otro, Entonces el cambio se completa en menos de 1 segundo.

### RNF-002 Acceso solo por Tailscale
Descripción: reqly solo es accesible desde la red privada de Tailscale. No tiene login propio en v1.
Prioridad: Debe
Criterios de aceptación:
- Dado un dispositivo fuera de la red privada, Cuando intenta abrir reqly, Entonces no obtiene respuesta.

### RNF-003 Acceso solo a carpetas registradas
Descripción: reqly lee y escribe solo dentro de las carpetas de proyecto que el usuario registró.
Prioridad: Debe
Criterios de aceptación:
- Dada una ruta fuera de las carpetas registradas, Cuando reqly o un agente intenta leerla o escribirla, Entonces reqly lo rechaza.

### RNF-004 Privacidad
Descripción: reqly no envía datos a servicios externos y no tiene telemetría ni analítica. Solo los agentes de IA que el usuario ya usa leen los archivos del proyecto.
Prioridad: Debe
Criterios de aceptación:
- Dado reqly en ejecución, Cuando se usa durante una hora, Entonces no se registra ninguna conexión saliente a Internet desde el servicio de reqly.

### RNF-005 Auditoría con el historial de git
Descripción: el historial de git es la auditoría de cambios. Cada elemento lo muestra.
Prioridad: Debe
Criterios de aceptación:
- Dado un elemento modificado, Cuando el usuario consulta su historial, Entonces cada cambio muestra fecha, autor y resumen.

### RNF-006 Idioma español
Descripción: la interfaz y los documentos generados están en español. Los términos técnicos ya usados en inglés (commit, ticket, Penpot, Markdown) se mantienen.
Prioridad: Debe
Criterios de aceptación:
- Dada la interfaz abierta, Cuando el usuario revisa cualquier texto, Entonces el texto está en español salvo los términos técnicos del glosario.

### RNF-007 Accesibilidad WCAG 2.2 AA
Descripción: la interfaz cumple WCAG 2.2 nivel AA.
Prioridad: Debe
Criterios de aceptación:
- Dado cualquier pantalla, Cuando se ejecuta una auditoría automática, Entonces no hay errores de nivel crítico.
- Dado texto sobre fondo, Cuando se mide el contraste, Entonces el contraste es de al menos 4.5:1.
- Dado cualquier pantalla, Cuando el usuario navega solo con teclado, Entonces todas las acciones son alcanzables.

### RNF-008 Arranque tras reinicio
Descripción: no hay requisito de alta disponibilidad. reqly responde tras reiniciar la VM, sin intervención manual.
Prioridad: Debe
Criterios de aceptación:
- Dado un reinicio de la VM, Cuando la VM termina de arrancar, Entonces reqly responde a la primera petición sin intervención manual.

### RNF-009 Despliegue con Docker Compose y Sablier
Descripción: reqly corre como stack Docker Compose detrás de Traefik, con Sablier para escalar a cero cuando no se usa. [SUPUESTO] Ver docs/pendientes.md, S-10.
Prioridad: Debe
Criterios de aceptación:
- Dado el stack sin uso durante el tiempo configurado, Cuando llega una petición, Entonces Sablier levanta el servicio y lo sirve.

### RNF-010 Stack obligatorio
Descripción: el entorno de ejecución es Bun y la interfaz usa React.
Prioridad: Debe
Criterios de aceptación:
- Dado el repo, Cuando se revisa su configuración, Entonces el entorno de ejecución es Bun y la interfaz usa React.

## Reglas de negocio

### Estados
- Requisito: formal, revisado o retirado. De formal a revisado cuando el usuario lo revisa. Retirado es final.
- Ticket: pendiente, en curso, hecho o retirado. Retirado es final.
- Requerimiento: abierto o formalizado. De abierto a formalizado cuando la formalización termina.

### Identificadores
- RF-### y RNF-###, con tres dígitos. El agente usa el siguiente número libre al formalizar.
- Los IDs son únicos y permanentes. Un ID retirado no se reutiliza. reqly verifica que no haya duplicados.

### Huecos y avance
- Hueco de trazabilidad: requisito "debe" no retirado sin caso de uso o sin criterios verificables.
- Avance: proporción de requisitos "debe" no retirados que tienen un ticket en estado hecho. [SUPUESTO] Ver docs/pendientes.md, S-08.

### Validaciones
- Campos obligatorios y formato: bloquean el guardado con aviso.
- Referencias rotas: se avisan y el guardado se hace.

Los supuestos y pendientes están en docs/pendientes.md.
