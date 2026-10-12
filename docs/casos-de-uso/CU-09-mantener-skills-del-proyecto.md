---
id: CU-09
tipo: caso-de-uso
actor: usuario propietario
estado: formal
requisitos: [RF-022]
---

# CU-09 Mantener las skills del proyecto

Actor: usuario propietario.
Requisitos: RF-022
Precondición: el proyecto tiene skills copiadas en el repo con versión fijada.

Pasos principales:
1. El usuario abre la vista de skills (RF-022).
2. reqly muestra la versión instalada de cada skill (RF-022).
3. El usuario decide si actualiza una skill. [SUPUESTO] El mecanismo de actualización está por definir (ver docs/pendientes.md, P-11).

Errores:
E1. Un archivo de skill no cumple el formato esperado: reqly muestra un aviso y el resto del proyecto sigue visible (RF-022).

Resultado: las skills del proyecto se mantienen con versiones conocidas.