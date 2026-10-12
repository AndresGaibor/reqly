---
id: RF-018
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-02, CU-07]
---

# RF-018 Estados de los elementos

Descripción: cada tipo de elemento tiene sus estados y solo se permiten las transiciones definidas en las reglas de negocio.

Criterios de aceptación:
- Dado un requisito en estado retirado, Cuando el usuario intenta cambiarlo a formal, Entonces reqly rechaza la transición.

Casos de uso: CU-02, CU-07
