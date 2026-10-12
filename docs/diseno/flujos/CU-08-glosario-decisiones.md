---
id: CU-08-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-08]
requisitos: [RF-011, RF-023]
---

# Flujo CU-08: Consultar glosario y decisiones

Recorrido del caso de uso CU-08. Consulta de términos y de decisiones del proyecto.

## Camino principal

1. Abrir el glosario: CU-08-P10 (RF-011).
2. Buscar un término: CU-08-P10 (RF-011).
3. Abrir la vista de decisiones: CU-08-P11 (RF-023).
4. Leer una decisión en su detalle: CU-08-P11 (RF-023).

## Caminos alternos

- A1. Reemplazar una decisión aceptada por otra: CU-08-P11, estado reemplazando (RF-023).

## Errores

- E1. El proyecto no tiene glosario: CU-08-P10, estado vacío (RF-011).
- E2. No hay decisiones registradas: CU-08-P11, estado vacío (RF-023).

## Resultado

El usuario encuentra la definición de un término o la decisión del proyecto con su contexto.
