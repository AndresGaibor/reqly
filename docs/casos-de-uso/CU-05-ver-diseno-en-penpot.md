---
id: CU-05
tipo: caso-de-uso
actor: usuario propietario
estado: formal
requisitos: [RF-009, RNF-002]
---

# CU-05 Ver el diseño de un requisito en Penpot

Actor: usuario propietario.

Requisitos: RF-009, RNF-002.

Precondición: el requisito tiene una referencia de diseño.

Pasos principales:
1. El usuario abre el requisito.
2. reqly intenta mostrar el frame de Penpot.
3. El usuario ve la vista gráfica del frame.

Caminos alternos:
A1. Penpot no responde: reqly muestra la referencia en texto (RF-009).
A2. El requisito no tiene referencia: reqly no muestra la sección de diseño.

Errores:
E1. La referencia apunta a un frame que no existe: reqly muestra la referencia y un aviso de referencia rota. [SUPUESTO] Ver docs/pendientes.md, S-03.

Resultado: el usuario ve el diseño o la referencia para abrirlo en Penpot.