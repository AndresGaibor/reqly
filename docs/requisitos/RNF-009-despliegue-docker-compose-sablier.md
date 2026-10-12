---
id: RNF-009
tipo: requisito-no-funcional
prioridad: Debe
estado: formal
casos_de_uso: []
---

# RNF-009 Despliegue con Docker Compose y Sablier

Descripción: reqly corre como stack Docker Compose detrás de Traefik, con Sablier para escalar a cero cuando no se usa. [SUPUESTO] Ver docs/pendientes.md, S-10.

Criterios de aceptación:
- Dado el stack sin uso durante el tiempo configurado, Cuando llega una petición, Entonces Sablier levanta el servicio y lo sirve.

Casos de uso: ninguno