---
id: RF-009
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01, CU-05, CU-10]
---

# RF-009 Ver el diseño de Penpot en solo lectura

Descripción: un requisito puede tener una referencia de diseño a Penpot. reqly muestra la vista gráfica del frame o, si no es posible, la referencia en texto.

Criterios de aceptación:
- Dado un requisito con referencia a un frame accesible de Penpot, Cuando el usuario abre el requisito, Entonces reqly muestra la vista gráfica del frame.
- Dado un requisito con referencia a un frame que no se puede mostrar, Cuando el usuario abre el requisito, Entonces reqly muestra la referencia en texto con archivo, página y frame, sin opciones de edición.

Casos de uso: CU-01, CU-05, CU-10