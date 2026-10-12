---
id: CU-10
tipo: caso-de-uso
actor: agente de IA y usuario propietario
estado: formal
requisitos: [RF-029, RF-009, RF-007]
---

# CU-10 Diseñar pantallas desde requisitos y casos de uso

Actor: agente de IA y usuario propietario.
Requisitos: RF-029, RF-009, RF-007
Precondición: el caso de uso tiene requisitos formales y Penpot está accesible.

Pasos principales:
1. El usuario pide diseñar un caso de uso.
2. El agente lee el caso de uso, sus requisitos y la skill reqly-disenar (RF-029).
3. El agente crea o reutiliza los fundamentos: tokens y temas claro y oscuro (RF-029).
4. El agente crea los componentes que falten, uno por archivo en docs/diseno/componentes/ (RF-029).
5. El agente diseña las pantallas del caso con todos sus estados y registra cada referencia (RF-029, RF-009).
6. El agente documenta el flujo en docs/diseno/flujos/ y conecta el prototipo en Penpot (RF-029).
7. El agente guarda cada bloque con un commit (RF-007) y espera la revisión del usuario.

Caminos alternos:
A1. Falta un requisito formal para un paso: el agente lo señala y no diseña ese paso.

Errores:
E1. Penpot no responde: el agente registra un pendiente y no crea referencias.
E2. Un par de colores no cumple el contraste: el agente no cierra la pantalla hasta corregirlo.

Resultado: el caso de uso tiene su flujo y sus pantallas en Penpot, documentados en el repo.
