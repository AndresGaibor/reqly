---
id: CU-04-flujo
tipo: flujo
estado: sin revisar
casos_de_uso: [CU-04]
requisitos: [RF-007, RF-010, RF-015]
---

# Flujo CU-04: Añadir una nota y marcarla como pendiente

Recorrido del caso de uso CU-04. Una nota con fecha se añade a un elemento y, si se marca, aparece en la lista de pendientes.

## Camino principal

1. Abrir el requisito: CU-01-P7 (RF-009). Para un requerimiento: CU-02-P14.
2. Añadir la nota: CU-04-P13 (RF-015).
3. Marcarla como pregunta o como pendiente: CU-04-P13 (RF-015).
4. Guardar la nota con commit: CU-04-P13, estado guardado (RF-007).
5. Ver la nota en la lista de pendientes: CU-04-P12 (RF-010).

## Caminos alternos

- A1. Nota sin marca: solo aparece en la ficha del elemento (RF-015).

## Errores

- E1. La nota no se guarda: CU-04-P13, estado error (RF-007).

## Resultado

La cuestión queda visible y trazada al elemento.
