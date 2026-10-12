---
id: RF-007
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01, CU-02, CU-03, CU-04, CU-06, CU-07]
---

# RF-007 Commit automático por guardado

Descripción: cada guardado crea un commit con un mensaje generado a partir del archivo cambiado.

Criterios de aceptación:
- Dado un archivo guardado desde reqly, Cuando el guardado termina, Entonces existe un commit nuevo que contiene solo ese archivo y su mensaje nombra el archivo.

Casos de uso: CU-01, CU-02, CU-03, CU-04, CU-06, CU-07