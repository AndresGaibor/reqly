---
id: RNF-002
tipo: requisito-no-funcional
prioridad: Debe
estado: formal
casos_de_uso: [CU-05]
---

# RNF-002 Acceso solo por Tailscale

Descripción: reqly solo es accesible desde la red privada de Tailscale. No tiene login propio en v1.

Criterios de aceptación:
- Dado un dispositivo fuera de la red privada, Cuando intenta abrir reqly, Entonces no obtiene respuesta.

Casos de uso: CU-05