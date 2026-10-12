---
id: RNF-004
tipo: requisito-no-funcional
prioridad: Debe
estado: formal
casos_de_uso: []
---

# RNF-004 Privacidad

Descripción: reqly no envía datos a servicios externos y no tiene telemetría ni analítica. Solo los agentes de IA que el usuario ya usa leen los archivos del proyecto.

Criterios de aceptación:
- Dado reqly en ejecución, Cuando se usa durante una hora, Entonces no se registra ninguna conexión saliente a Internet desde el servicio de reqly.

Casos de uso: ninguno