---
id: CU-04
tipo: caso-de-uso
actor: usuario propietario y agente de IA
estado: formal
requisitos: [RF-007, RF-010, RF-015]
---

# CU-04 Añadir una nota y marcarla como pendiente

Actor: usuario propietario y agente de IA.

Requisitos: RF-007, RF-010, RF-015.

Precondición: existe un requerimiento, un requisito o un caso de uso.

Pasos principales:
1. El usuario abre el elemento.
2. El usuario escribe una nota con fecha (RF-015).
3. El usuario marca la nota como pendiente o como pregunta, si aplica (RF-015).
4. reqly guarda la nota con un commit (RF-007).
5. La nota aparece en la lista de pendientes (RF-010).

Resultado: la cuestión queda visible y trazada al elemento.