---
id: RF-028
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01]
---

# RF-028 Instalar las skills del proyecto al seleccionarlo

Descripción: al seleccionar un proyecto, reqly instala en su carpeta .claude/skills/ las skills de reqly que falten o estén en una versión anterior: reqly-formalizar, reqly-migrar, reqly-disenar, grill-with-docs y domain-modeling. Muestra la versión instalada de cada una.

Criterios de aceptación:
- Dado un proyecto sin skills de reqly, When el usuario lo selecciona, Entonces reqly copia las cinco skills con su versión y lo indica en pantalla.
- Dada una skill instalada en una versión anterior a la de reqly, When el usuario selecciona el proyecto, Entonces reqly la actualiza y guarda el cambio con un commit.
- Dada una skill instalada con una versión más nueva que la de reqly, When el usuario selecciona el proyecto, Entonces reqly no la sobrescribe y muestra un aviso.

Casos de uso: CU-01
