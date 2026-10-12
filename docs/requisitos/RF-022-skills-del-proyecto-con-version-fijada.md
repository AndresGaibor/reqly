---
id: RF-022
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-09]
---

# RF-022 Skills del proyecto con versión fijada

Descripción: las skills del proyecto y las de Matt Pocock se copian al repo con versión fijada. reqly muestra la versión instalada y valida el formato al cargar.

Criterios de aceptación:
- Dada una skill copiada en el repo, Cuando reqly carga el proyecto, Entonces muestra la versión instalada.
- Dado un archivo que no cumple el formato esperado, Cuando reqly carga el proyecto, Entonces muestra un aviso y el resto del proyecto sigue visible.

Casos de uso: CU-09