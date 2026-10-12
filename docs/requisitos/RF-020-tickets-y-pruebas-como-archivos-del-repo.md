---
id: RF-020
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-02, CU-07]
---

# RF-020 Tickets y pruebas como archivos del repo

Descripción: un agente crea tickets y pruebas como archivos del repo a partir de requisitos formales. El usuario y el agente pueden cambiar el estado de un ticket, y cada cambio es un commit.

Criterios de aceptación:
- Dado un requisito formal, Cuando el agente crea tickets, Entonces existe un archivo por ticket enlazado al requisito.
- Dado un ticket en curso, Cuando el agente cambia su estado a hecho, Entonces el cambio queda en un commit.

Casos de uso: CU-02, CU-07