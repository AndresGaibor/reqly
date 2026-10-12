---
id: RF-016
tipo: requisito
prioridad: Debe
estado: formal
casos_de_uso: [CU-01, CU-02]
---

# RF-016 Validar al guardar

Descripción: al guardar, reqly valida los campos obligatorios y el formato. Si fallan, bloquea el guardado con aviso. Las referencias rotas se avisan, pero el guardado se hace.

Criterios de aceptación:
- Dado un requisito sin criterios, Cuando el usuario guarda, Entonces reqly no guarda y muestra el campo que falta.
- Dado un caso de uso que cita un RF que no existe, Cuando el usuario guarda, Entonces reqly guarda y muestra una advertencia con la referencia rota.

Casos de uso: CU-01, CU-02
