---
id: CU-06
tipo: caso-de-uso
actor: agente de IA y usuario propietario
estado: formal
requisitos: [RF-007, RF-013, RF-014, RF-015, RF-021]
---

# CU-06 Migrar documentos o código existentes a requerimientos

Actor: agente de IA y usuario propietario.

Requisitos: RF-007, RF-013, RF-014, RF-015, RF-021.

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