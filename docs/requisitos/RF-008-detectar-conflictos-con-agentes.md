---
id: RF-008
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01, CU-03]
---

# RF-008 Detectar conflictos con agentes

Descripción: si un agente cambia en disco un archivo que el usuario está editando, reqly no guarda y muestra ambas versiones.

Criterios de aceptación:
- Dado que el usuario edita un archivo y un agente lo cambia en disco, Cuando el usuario intenta guardar, Entonces reqly no guarda y muestra la versión del usuario y la del disco lado a lado.

Casos de uso: CU-01, CU-03