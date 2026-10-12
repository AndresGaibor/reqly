---
id: RF-002
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01]
---

# RF-002 Mostrar avance y huecos

Descripción: reqly muestra el número de huecos de trazabilidad y el avance del proyecto, con la lista de elementos afectados. El avance cuenta solo los requisitos "debe" no retirados con ticket hecho.

Criterios de aceptación:
- Dado un requisito "debe" sin caso de uso, When el usuario abre el panel de avance, Entonces el requisito aparece en la lista de huecos y el número de huecos es al menos 1.
- Dado un requisito "debería" con ticket en estado hecho, Cuando se calcula el avance, Entonces ese requisito no suma al avance.

Casos de uso: CU-01