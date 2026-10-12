---
id: RF-017
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-02]
---

# RF-017 Identificadores únicos

Descripción: los IDs RF-### y RNF-### son únicos y permanentes. Al formalizar, el agente usa el siguiente número libre. reqly verifica que no haya duplicados.

Criterios de aceptación:
- Dado que existe RF-004, Cuando el agente formaliza un nuevo requisito, Entonces el requisito recibe el siguiente número libre, sin reutilizar IDs retirados.
- Dado dos archivos con el mismo ID, Cuando reqly carga el proyecto, Entonces muestra un error de ID duplicado que identifica ambos archivos.

Casos de uso: CU-02
