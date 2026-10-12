---
id: RF-021
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-06]
---

# RF-021 Migrar documentos y código existentes

Descripción: el proyecto incluye una skill que guía al agente para migrar documentos existentes y, si el usuario lo pide, código, a requerimientos. Trabaja por bloques y el usuario revisa cada bloque antes de seguir.

Criterios de aceptación:
- Dado un repo con documentos Markdown existentes, Cuando el agente aplica la skill, Entonces propone requerimientos por bloques.
- Dado un bloque propuesto sin revisar, Cuando el agente termina el bloque, Entonces no avanza al siguiente hasta que el usuario lo revisa.

Casos de uso: CU-06