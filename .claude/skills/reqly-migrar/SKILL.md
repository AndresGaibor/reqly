---
name: reqly-migrar
description: Migra documentos existentes y, si el usuario lo pide, código de un proyecto a requerimientos abiertos de reqly, por bloques y con revisión del usuario en cada bloque. Usar cuando el usuario pida migrar, importar o convertir documentación o código existente en requerimientos.
version: 1.0.0
---

## Entradas

- El proyecto registrado en reqly.
- El alcance que indique el usuario: solo documentos Markdown del repo, o también código.

## Pasos

1. Antes de empezar, confirma el alcance con el usuario. Sin confirmación no empieces.
2. Haz un inventario en solo lectura de las fuentes y agrúpalas por tema. No copies contenido sin revisarlo.
3. Propón el primer bloque de hasta 5 elementos relacionados. Ver docs/pendientes.md, S-14. Presenta el bloque al usuario antes de escribir.
4. Por cada elemento del bloque aprobado, crea un archivo docs/requerimientos/REQ-###-slug.md. El ID es el siguiente número libre REQ-###. Ver docs/pendientes.md, S-13 y P-12.
5. Frontmatter de cada requerimiento: id, tipo: requerimiento, estado: abierto, origen (ruta del documento, o archivo y línea del código).
6. Cuerpo de cada requerimiento: H1 con el ID y un título, y el texto del requerimiento en lenguaje libre. No añadas criterios ni prioridad: eso lo hace la formalización.
7. Tras cada bloque, haz commit con el mensaje "docs: migra bloque <n> de <origen>" y espera la revisión del usuario antes de seguir.
8. Si el usuario decide no migrar algo, anótalo como nota marcada como pendiente en docs/pendientes.md.

## Reglas

- Código: describe el comportamiento observable en lenguaje de requerimiento. No copies la implementación. No inventes requisitos que el código no muestre. Marca con [SUPUESTO] lo que deduces.
- Cada requerimiento debe citar su origen. Si una afirmación no tiene fuente, no la escribas.
- La formalización a requisitos y casos de uso es otro paso, con la skill reqly-formalizar. Solo se hace si el usuario lo pide.
- Usa los términos de GLOSSARY.md cuando exista la entrada.
- Los IDs son únicos y permanentes. Un ID no se reutiliza, tampoco uno retirado.

## Qué no hacer

- No borres ni modifiques los documentos origen.
- No avances al siguiente bloque sin la revisión del usuario.
- No crees requerimientos duplicados de otro ya existente en docs/requerimientos/. Revisa los títulos antes de crear.
- No añadas criterios de aceptación ni prioridad a los requerimientos abiertos.

## Al terminar

- Si te detienes a mitad, haz commit de lo escrito con el mensaje "docs: borrador sin revisar migración <origen>". Al retomar, continúa desde el bloque no revisado.
- Comprueba que los IDs son únicos, que cada requerimiento tiene origen y que el estado es abierto.
