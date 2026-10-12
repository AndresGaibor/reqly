---
id: CU-02
tipo: caso-de-uso
actor: usuario propietario y agente de IA
estado: formal
requisitos: [RF-007, RF-012, RF-013, RF-014, RF-015, RF-016, RF-017, RF-018, RF-019, RF-020]
---

# CU-02 Capturar y formalizar un requerimiento (opcional)

Actor: usuario propietario y agente de IA.

Requisitos: RF-007, RF-012, RF-013, RF-014, RF-015, RF-016, RF-017, RF-018, RF-019, RF-020.

Precondición: existe un requerimiento abierto.

Pasos principales:
1. El usuario escribe el requerimiento en texto libre (RF-012).
2. El usuario añade notas si hace falta (RF-015).
3. El usuario pide al agente formalizarlo (RF-013).
4. El agente aplica la skill del proyecto y crea requisitos con ID y criterios, y los casos de uso. Los deja en estado formal (RF-013, RF-017).
5. El agente marca el requerimiento como formalizado y lo enlaza a los requisitos creados (RF-013).
6. El usuario revisa los requisitos y marca cada uno como revisado (RF-014).

Caminos alternos:
A1. El usuario retira un requisito en lugar de revisarlo (RF-018, RF-019).
A2. El agente se detiene a mitad: lo escrito queda en un commit marcado sin revisar. Al retomar, continúa por bloques (RF-013, RF-007).

Errores:
E1. Un requisito no tiene criterios: reqly no guarda y muestra el campo que falta (RF-016).
E2. Un caso de uso cita un RF que no existe: reqly guarda y muestra una advertencia (RF-016).
E3. Dos archivos tienen el mismo ID: reqly muestra un error de ID duplicado (RF-017).

Resultado: el requerimiento queda trazado a requisitos formales y casos de uso, listos para revisión.