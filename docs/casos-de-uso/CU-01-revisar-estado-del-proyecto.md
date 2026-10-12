---
id: CU-01
tipo: caso-de-uso
actor: usuario propietario
estado: formal
requisitos: [RF-001, RF-002, RF-003, RF-004, RF-005, RF-006, RF-007, RF-008, RF-009, RF-016, RF-024, RF-028]
---

# CU-01 Revisar el estado del proyecto

Actor: usuario propietario.

Requisitos: RF-001, RF-002, RF-003, RF-004, RF-005, RF-006, RF-007, RF-008, RF-009, RF-016, RF-024, RF-028.

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