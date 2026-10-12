---
id: RF-023
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-08]
---

# RF-023 Registros de decisión (ADR)

Descripción: reqly lista los ADR de docs/adr/ en orden numérico. Se leen y se crean desde reqly; se editan con el editor de Markdown como cualquier otro archivo del repo. Estados: propuesto, aceptado y reemplazado.

Criterios de aceptación:
- Dado docs/adr con dos registros, Cuando el usuario abre la vista de decisiones, Entonces se listan en orden numérico con título y estado.
- Dado un ADR en estado aceptado, Cuando la decisión cambia, Entonces se crea un ADR nuevo que lo reemplaza y el original pasa a estado reemplazado.

Casos de uso: CU-08