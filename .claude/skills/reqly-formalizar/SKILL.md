---
name: reqly-formalizar
description: Formaliza un requerimiento abierto de reqly en requisitos formales (RF o RNF) y casos de uso (CU) como archivos Markdown del repo. Usar cuando el usuario pida formalizar, convertir o pasar a requisitos un requerimiento de docs/requerimientos/.
version: 1.0.0
---

# Formalizar un requerimiento de reqly

## Entradas

Un archivo `docs/requerimientos/REQ-###-*.md` con estado abierto.

Si el archivo no existe o no está abierto, detente y pide al usuario el archivo correcto. No formalices nada por suposición.

## Pasos

1. Lee `GLOSSARY.md`, `docs/reglas-de-negocio.md` y los IDs existentes en `docs/requisitos/` y `docs/casos-de-uso/`. Usa solo los términos del glosario.
2. Propón los requisitos por bloques de hasta 5 elementos relacionados. Ver `docs/pendientes.md`, S-14.
3. Para cada requisito, crea un archivo `docs/requisitos/RF-###-slug.md` o `docs/requisitos/RNF-###-slug.md`. El ID es el siguiente número libre de su tipo.
4. Para cada caso de uso necesario, crea `docs/casos-de-uso/CU-##-slug.md` con el siguiente número libre.
5. Verifica la simetría: cada requisito lista sus casos de uso y cada caso de uso lista sus requisitos.
6. Cambia el requerimiento de abierto a formalizado y añade la lista de requisitos y casos de uso creados.
7. Tras cada bloque, haz commit con el mensaje `docs: formaliza <REQ-id> bloque <n>` y espera la revisión del usuario antes de seguir.

## Reglas

- Frontmatter de requisito: `id`, `tipo` (`requisito` o `requisito-no-funcional`), `prioridad` (`Debe`, `Debería`, `Podría` o `No por ahora`), `estado: formal`, `casos_de_uso` (lista, o `[]`).
- Cuerpo de requisito: título H1 con ID y título; `Descripción:` en una frase; `Criterios de aceptación:` en formato Dado / Cuando / Entonces, uno por línea; `Casos de uso:` con la lista o `ninguno`.
- Frontmatter de caso de uso: `id`, `tipo: caso-de-uso`, `actor`, `estado: formal`, `requisitos` (lista).
- Cuerpo de caso de uso: `Actor`, `Requisitos`, `Precondición`, `Pasos principales` numerados, `Caminos alternos` (A1, A2, ...), `Errores` (E1, E2, ...), `Resultado`. Omite las secciones vacías.
- Solo los RF `debe` necesitan caso de uso. Los RNF se verifican con criterios. Si un RF `debe` no tiene caso de uso, di por qué.
- Un criterio debe ser verificable. No uses `rápido`, `fácil` o `adecuado` sin una medida.
- Todo lo que escribes queda en estado `formal`. No lo marques como `revisado`: eso lo hace el usuario.
- Un ID retirado no se reutiliza, aunque el archivo ya no esté.
- Si un término del requerimiento no está en `GLOSSARY.md`, no lo inventes. Añade una nota marcada como pendiente en el requerimiento y `[PENDIENTE]` en `docs/pendientes.md`.

## Qué no hacer

- No borres archivos. Retirar un elemento es cambiar su estado a `retirado`, y solo si el usuario lo pide.
- No modifiques requisitos ya revisados sin que el usuario lo pida.
- No avances al siguiente bloque sin la revisión del usuario.

## Al terminar

- Comprueba que los IDs son únicos, que la simetría se cumple, que el frontmatter está completo y que cada criterio está en Dado / Cuando / Entonces.
- Si te detienes a mitad, haz commit de lo escrito con el mensaje `docs: borrador sin revisar <REQ-id>`. Al retomar, continúa desde el bloque no revisado.