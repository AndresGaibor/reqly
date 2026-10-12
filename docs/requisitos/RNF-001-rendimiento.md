---
id: RNF-001
tipo: requisito-no-funcional
prioridad: Debe
estado: formal
casos_de_uso: []
---

# RNF-001 Rendimiento

Descripción: reqly carga proyectos de hasta 500 archivos Markdown con tiempos acotados, medidos en la red de Tailscale.

Criterios de aceptación:
- Dado un proyecto de 500 archivos, Cuando el usuario lo abre por primera vez en la red de Tailscale, Entonces la carga inicial termina en menos de 3 segundos.
- Dado un proyecto abierto, Cuando el usuario pasa de un documento a otro, Entonces el cambio se completa en menos de 1 segundo.

Casos de uso: ninguno