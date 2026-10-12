---
name: reqly-disenar
description: Diseña pantallas, componentes, plantillas y flujos en Penpot a partir de requisitos y casos de uso de reqly, por capas, y documenta cada elemento en docs/diseno/. Usar cuando el usuario pida diseñar, prototipar o llevar un caso de uso a Penpot.
version: 1.0.0
---

## Entradas

- Un caso de uso CU-## de docs/casos-de-uso/ con sus requisitos formales (RF o RNF) de docs/requisitos/. Si el caso no tiene requisitos formales, detente: el diseño sale de los requisitos, no al revés.
- Penpot accesible. Si no responde, registra un pendiente en docs/pendientes.md y no crees referencias.

## Pasos

1. Lee el caso de uso, sus requisitos, GLOSSARY.md y docs/reglas-de-negocio.md. Define objetivo, actor, entrada y salida.
2. Fundamentos: tokens como fuente en docs/diseno/tokens.json en formato DTCG. Un set core con primitivos (paletas de grises, azules, verdes, ámbar y rojos; espaciado; radios) y dos sets semánticos, semantic/light y semantic/dark, con los mismos nombres. Dos temas en Penpot: Modo/Claro y Modo/Oscuro. Crea solo los tokens que falten. [SUPUESTO] Ver docs/pendientes.md, S-16 y S-17.
3. Verifica el contraste de cada par texto-fondo y borde-superficie, en claro y en oscuro. Registra la tabla en docs/diseno/fundamentos.md.
4. Componentes, de átomos a organismos: antes de crear uno, revisa docs/diseno/componentes/ para reutilizarlo. Cada componente va en docs/diseno/componentes/<nivel>-<nombre>.md (nivel: atomo, molecula u organismo), con: propósito, cuándo no usarlo, anatomía, variantes, estados (por defecto, hover, foco, deshabilitado y los que apliquen), propiedades, tokens que usa, accesibilidad y reglas de uso. Construye con auto layout y solo tokens.
5. Plantillas: una por tipo de pantalla del caso (listado, detalle, formulario, autenticación, estructura de aplicación), en docs/diseno/plantillas/.
6. Pantallas: primero baja fidelidad (estructura), después alta fidelidad con contenido realista. Un frame por cada paso con interfaz y uno por cada estado: principal, cargando, vacío, error, éxito y cada camino alterno o error del caso de uso. Cada pantalla va en docs/diseno/pantallas/<CU>-<paso>-<estado>.md.
7. Flujo: documenta el camino feliz y las ramas de error en docs/diseno/flujos/CU-##.md, con cada paso enlazado a su pantalla.
8. Prototipo: conecta en Penpot las pantallas según el flujo. Hazlo solo después de tener el flujo documentado.
9. Trazabilidad: cada archivo de pantalla tiene frontmatter con id, tipo: pantalla, estado: sin revisar, requisitos (lista), casos_de_uso (lista) y penpot con archivo, pagina y frame. Usa nombres de archivo y frame sin espacios raros para que sean estables.
10. Tras cada bloque, haz commit con el mensaje "diseno: <CU-##> bloque <n>" y espera la revisión del usuario antes de seguir.

## Reglas

- Ningún color, espacio o radio suelto: todos salen de tokens.
- Contraste mínimo: texto normal 4.5:1; texto grande y componentes de interfaz 3:1. Comprueba en claro y en oscuro.
- No dependas solo del color para indicar un estado: añade icono o texto.
- Los estados de error y vacío vienen del caso de uso. Si el caso no los describe, pregunta; no los inventes.
- Diseña con textos largos, para comprobar que los componentes no se rompen.
- Penpot: lee primero la visión general de Penpot disponible en el entorno y usa sus herramientas. No cambies diseños ya revisados sin que el usuario lo pida.
- Un cambio de componente que afecte a varias pantallas se documenta en el archivo del componente.

## Qué no hacer

- No diseñes pantallas de un caso sin requisitos formales.
- No borres componentes ni pantallas. Para retirar, cambia su estado a retirado, y solo si el usuario lo pide.
- No crees referencias a frames que no existen.
- No envíes el diseño a ningún servicio externo.

## Al terminar

- Comprueba que cada pantalla tiene su referencia, que los RF y CU citados existen, que no hay valores sueltos y que el contraste está registrado.
