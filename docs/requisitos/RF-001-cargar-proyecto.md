---
id: RF-001
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01]
---

# RF-001 Cargar un proyecto

Descripción: el usuario selecciona una carpeta del host y reqly carga los documentos Markdown del proyecto.

Criterios de aceptación:
- Dada una carpeta con documentos de reqly, Cuando el usuario la selecciona, Entonces reqly muestra los documentos sin pedir más datos.
- Dada una carpeta sin documentos de reqly, Cuando el usuario la selecciona, Entonces reqly lo indica y no crea ningún archivo.

Casos de uso: CU-01