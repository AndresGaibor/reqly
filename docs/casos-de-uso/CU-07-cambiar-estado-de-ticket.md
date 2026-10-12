---
id: CU-07
tipo: caso-de-uso
actor: usuario propietario y agente de IA
estado: formal
requisitos: [RF-007, RF-018, RF-019, RF-020]
---

# CU-07 Cambiar el estado de un ticket

Actor: usuario propietario y agente de IA.

Requisitos: RF-007, RF-018, RF-019, RF-020.

Precondición: existe un ticket enlazado a un requisito formal.

Pasos principales:
1. El usuario o el agente abre el ticket.
2. Cambia su estado a en curso, hecho o retirado.
3. reqly guarda el cambio con un commit (RF-007).

Errores:
E1. El cambio no está permitido, por ejemplo de retirado a en curso: reqly lo rechaza (RF-018).

Resultado: el avance del proyecto se actualiza con el estado del ticket.