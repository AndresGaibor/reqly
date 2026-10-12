# Glosario de reqly

Términos del negocio y del flujo de trabajo de reqly. Cada término tiene una sola definición; los sinónimos rechazados aparecen en Evitar.

**reqly**: aplicación web personal que muestra y edita los documentos de ingeniería de un proyecto, guardados como Markdown en su repositorio git. _Evitar_: Trama, Docweave (nombres descartados).

**Proyecto**: carpeta del repositorio git que contiene los documentos de reqly. Es lo que el usuario selecciona en reqly. _Evitar_: repo, cuando se habla de los documentos.

**Actor**: persona o sistema que interactúa con reqly.

**Usuario propietario**: persona que administra el proyecto y tiene control total sobre sus archivos. Es el único usuario humano en v1.

**Agente de IA**: actor automatizado, por ejemplo Claude Code, que lee y escribe archivos del repo y hace commits. _Evitar_: bot, asistente.

**Requerimiento**: idea informal que escribe el usuario en texto libre, sin ID ni criterios. Puede formalizarse en uno o más requisitos. _Evitar_: requisito; son cosas distintas.

**Requisito**: enunciado verificable de algo que el sistema debe hacer o cumplir. Tiene ID, criterios de aceptación y prioridad. _Evitar_: requerimiento.

**RF (requisito funcional)**: requisito sobre lo que hace el sistema. Se identifica como RF-### con tres dígitos.

**RNF (requisito no funcional)**: requisito sobre cómo se comporta el sistema: rendimiento, seguridad, privacidad, disponibilidad, auditoría, idioma y accesibilidad. Se identifica como RNF-###.

**Criterio de aceptación**: condición verificable escrita en formato Dado / Cuando / Entonces.

**Caso de uso**: secuencia de pasos entre un actor y reqly para lograr un objetivo, con caminos alternos y errores. Se identifica como CU-## y cita los RF que cubre.

**Prioridad MoSCoW**: una de cuatro: Debe, Debería, Podría o No por ahora.

**Formal**: estado de un requisito recién escrito, con ID y criterios, que el usuario todavía no ha revisado.

**Revisado**: estado de un requisito formal que el usuario ya revisó.

**Retirado**: estado final de un requisito o de un ticket que ya no aplica. Sale de la vista principal y su archivo se conserva en el repo.

**Abierto**: estado de un requerimiento que todavía no se ha formalizado.

**Formalizado**: estado de un requerimiento que ya tiene requisitos y casos de uso creados a partir de él.

**Sin revisar**: marca de un cambio de agente que el usuario todavía no ha revisado. Equivale al estado formal hasta que pasa a revisado.

**Nota**: texto libre con fecha, adjunto a un requerimiento, requisito o caso de uso. Puede marcarse como pregunta o como pendiente.

**Pendiente (nota marcada)**: cuestión abierta marcada en una nota o en la lista de pendientes del proyecto. No confundir con el estado pendiente de un ticket.

**Supuesto**: afirmación que se da por cierta sin confirmar. Se marca [SUPUESTO] y se valida con el usuario.

**[PENDIENTE]**: dato que el usuario todavía no tiene. Se marca con quién puede responderlo.

**Hueco de trazabilidad**: requisito funcional (RF) "debe" no retirado que no tiene caso de uso o no tiene criterios verificables. Los RNF se verifican con sus criterios y no requieren caso de uso. _Evitar_: error.

**Avance**: proporción de requisitos "debe" no retirados que tienen un ticket en estado hecho.

**Matriz de trazabilidad**: tabla que une requisito, caso de uso, diseño, ticket y prueba, y marca los huecos.

**Frontmatter**: bloque de metadatos al inicio de un archivo Markdown, con campos como id, prioridad, estado y relaciones.

**Referencia de diseño**: enlace a un frame de Penpot, indicado por archivo, página y frame. reqly la muestra en solo lectura.

**Penpot**: herramienta de diseño que corre en la VM. reqly solo la lee.

**Ticket**: unidad de trabajo de desarrollo. Es un archivo del repo que un agente crea a partir de requisitos formales, enlazado a ellos. Estados: pendiente, en curso, hecho, retirado.

**Prueba**: verificación de un requisito o caso de uso, guardada como archivo del repo.

**ADR (registro de decisión de arquitectura)**: documento corto y numerado en docs/adr/ que guarda una decisión, su contexto y sus consecuencias. Formato docs/adr/NNNN-slug.md.

**Commit automático**: commit que reqly crea al guardar un archivo, con un mensaje generado a partir del archivo cambiado.

**Conflicto**: situación en la que un agente cambia en disco un archivo que el usuario está editando en reqly.

**Historial**: commits de git que tocan un archivo, mostrados por elemento con fecha, autor y resumen.

**Skill del proyecto**: instrucciones para un agente que guían un flujo concreto. Se instalan en el repo con versión fijada.

**Formalización**: paso en el que un agente convierte un requerimiento abierto en requisitos formales y casos de uso.

**Migración**: paso en el que un agente convierte documentos o código existentes en requerimientos, por bloques y con revisión del usuario.