---
id: RF-013
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-02, CU-06]
---

# RF-013 Formalizar un requerimiento con un agente

Descripción: el proyecto incluye una skill que guía al agente para convertir un requerimiento abierto en requisitos formales y casos de uso, y enlazarlos al requerimiento.

Criterios de aceptación:
- Dado un requerimiento abierto, Cuando el agente aplica la skill, Entonces crea requisitos con ID y criterios, crea casos de uso y deja los requisitos en estado formal.
- Dado que el agente termina la formalización, Cuando la formalización acaba, Entonces el requerimiento pasa a formalizado y enlaza los requisitos creados.

Casos de uso: CU-02, CU-06
