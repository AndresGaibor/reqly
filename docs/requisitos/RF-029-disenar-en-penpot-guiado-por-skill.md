---
id: RF-029
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-10]
---

# RF-029 Diseñar en Penpot guiado por la skill

Descripción: el proyecto incluye la skill reqly-disenar, que guía al agente para diseñar en Penpot a partir de requisitos y casos de uso, por capas, y documenta cada elemento en docs/diseno/. reqly solo lee el diseño.

Criterios de aceptación:
- Dado un caso de uso con requisitos formales, Cuando el agente aplica la skill, Entonces crea una pantalla por cada paso con interfaz y registra su referencia de diseño (archivo, página y frame) en docs/diseno/.
- Dado un caso de uso con caminos alternos o errores, Cuando el agente diseña sus pantallas, Entonces existe un frame por cada estado de error o alterno descrito en el caso.
- Dado un componente de una pantalla, Cuando se revisa, Entonces sus colores, espacios y radios salen de tokens, sin valores sueltos.
- Dado un par de texto y fondo, Cuando se mide el contraste, Entonces cumple al menos 4.5:1 para texto normal y 3:1 para texto grande y componentes.

Casos de uso: CU-10
