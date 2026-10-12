---
id: RF-019
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-02, CU-07]
---

# RF-019 No borrar elementos

Descripción: reqly no borra elementos. Retirar un elemento es cambiar su estado.

Criterios de aceptación:
- Dado un requisito retirado, Cuando el usuario abre la vista principal, Entonces el requisito no aparece y su archivo sigue en el repo.

Casos de uso: CU-02, CU-07