# Casos de uso de reqly

Flujos de punta a punta de reqly. Cada caso de uso indica el actor, los requisitos que cubre, los pasos principales, los caminos alternos (A) y los errores (E).

## CU-01 Revisar el estado del proyecto
Actor: usuario propietario.
Requisitos: RF-001, RF-002, RF-003, RF-005, RF-006, RF-007, RF-009, RF-024.
Precondición: reqly está abierto desde la red de Tailscale.
Pasos principales:
1. El usuario selecciona la carpeta del proyecto (RF-001).
2. reqly carga los documentos y muestra el avance y el número de huecos (RF-002).
3. El usuario abre la matriz de trazabilidad y filtra los huecos (RF-005).
4. El usuario abre un requisito y ve su caso de uso y su referencia de diseño (RF-003, RF-009).
5. El usuario edita el Markdown y revisa la vista previa (RF-006).
6. El usuario guarda. reqly escribe el archivo y crea un commit (RF-007).
Caminos alternos:
A1. El usuario abre la vista de tablas en lugar de la matriz (RF-004).
A2. Penpot no responde o el frame no se puede mostrar: reqly muestra la referencia en texto (RF-009).
A3. El usuario consulta el historial de un requisito (RF-024).
Errores:
E1. La carpeta no tiene documentos de reqly: reqly lo indica y no crea archivos (RF-001).
E2. Un agente cambió el archivo en disco mientras se edita: reqly no guarda y muestra ambas versiones. Ver CU-03 (RF-008).
E3. Falla una validación al guardar: reqly no guarda y muestra el campo que falta (RF-016).
E4. Falla el commit: reqly conserva el archivo guardado en disco y muestra el error. [SUPUESTO] Ver docs/pendientes.md, S-12.
Resultado: el usuario sabe qué falta para terminar el proyecto.

## CU-02 Capturar y formalizar un requerimiento (opcional)
Actor: usuario propietario y agente de IA.
Requisitos: RF-012, RF-013, RF-014, RF-015, RF-016, RF-017, RF-018, RF-020.
Precondición: existe un requerimiento abierto.
Pasos principales:
1. El usuario escribe el requerimiento en texto libre (RF-012).
2. El usuario añade notas si hace falta (RF-015).
3. El usuario pide al agente formalizarlo (RF-013).
4. El agente aplica la skill del proyecto y crea requisitos con ID y criterios, y los casos de uso. Los deja en estado formal (RF-013, RF-017).
5. El agente marca el requerimiento como formalizado y lo enlaza a los requisitos creados (RF-013).
6. El usuario revisa los requisitos y marca cada uno como revisado (RF-014).
Caminos alternos:
A1. El usuario retira un requisito en lugar de revisarlo (RF-018, RF-019).
A2. El agente se detiene a mitad: lo escrito queda en un commit marcado sin revisar. Al retomar, continúa por bloques (RF-013, RF-007).
Errores:
E1. Un requisito no tiene criterios: reqly no guarda y muestra el campo que falta (RF-016).
E2. Un caso de uso cita un RF que no existe: reqly guarda y muestra una advertencia (RF-016).
E3. Dos archivos tienen el mismo ID: reqly muestra un error de ID duplicado (RF-017).
Resultado: el requerimiento queda trazado a requisitos formales y casos de uso, listos para revisión.

## CU-03 Resolver un conflicto con un agente
Actor: usuario propietario y agente de IA.
Requisitos: RF-007, RF-008.
Precondición: el usuario tiene un archivo abierto para editar.
Pasos principales:
1. El usuario edita un archivo.
2. Un agente cambia el mismo archivo en disco.
3. El usuario intenta guardar.
4. reqly no guarda y muestra ambas versiones lado a lado.
5. El usuario elige conservar una versión, o combina las dos a mano.
6. reqly guarda la versión elegida y crea un commit (RF-007).
Resultado: nada se sobrescribe sin decisión del usuario.

## CU-04 Añadir una nota y marcarla como pendiente
Actor: usuario propietario y agente de IA.
Requisitos: RF-010, RF-015.
Precondición: existe un requerimiento, un requisito o un caso de uso.
Pasos principales:
1. El usuario abre el elemento.
2. El usuario escribe una nota con fecha (RF-015).
3. El usuario marca la nota como pendiente o como pregunta, si aplica (RF-015).
4. reqly guarda la nota con un commit (RF-007).
5. La nota aparece en la lista de pendientes (RF-010).
Resultado: la cuestión queda visible y trazada al elemento.

## CU-05 Ver el diseño de un requisito en Penpot
Actor: usuario propietario.
Requisitos: RF-009, RNF-002.
Precondición: el requisito tiene una referencia de diseño.
Pasos principales:
1. El usuario abre el requisito.
2. reqly intenta mostrar el frame de Penpot.
3. El usuario ve la vista gráfica del frame.
Caminos alternos:
A1. Penpot no responde: reqly muestra la referencia en texto (RF-009).
A2. El requisito no tiene referencia: reqly no muestra la sección de diseño.
Errores:
E1. La referencia apunta a un frame que no existe: reqly muestra la referencia y un aviso de referencia rota. [SUPUESTO] Ver docs/pendientes.md, S-03.
Resultado: el usuario ve el diseño o la referencia para abrirlo en Penpot.

## CU-06 Migrar documentos o código existentes a requerimientos
Actor: agente de IA y usuario propietario.
Requisitos: RF-021, RF-013, RF-014.
Precondición: el proyecto tiene documentos o código existentes y el usuario pide la migración.
Pasos principales:
1. El agente aplica la skill de migración y lee los documentos (y el código, si el usuario lo pide).
2. El agente propone los requerimientos del primer bloque (RF-021).
3. El usuario revisa el bloque y responde las preguntas.
4. El agente corrige el bloque y lo guarda con un commit (RF-007).
5. Se repite con el siguiente bloque hasta terminar.
6. Los requisitos formales resultantes pasan por la revisión del usuario (RF-014).
Caminos alternos:
A1. El usuario decide no migrar un bloque: el agente lo deja fuera y lo anota como pendiente (RF-015).
Errores:
E1. El agente pierde cuota a mitad de un bloque: lo escrito queda sin revisar y se retoma por bloques (RF-013).
Resultado: el proyecto tiene requerimientos trazables a partir de lo existente, con revisión del usuario.

## CU-07 Cambiar el estado de un ticket
Actor: usuario propietario y agente de IA.
Requisitos: RF-018, RF-019, RF-020, RF-007.
Precondición: existe un ticket enlazado a un requisito formal.
Pasos principales:
1. El usuario o el agente abre el ticket.
2. Cambia su estado a en curso, hecho o retirado.
3. reqly guarda el cambio con un commit (RF-007).
Errores:
E1. El cambio no está permitido, por ejemplo de retirado a en curso: reqly lo rechaza (RF-018).
Resultado: el avance del proyecto se actualiza con el estado del ticket.
