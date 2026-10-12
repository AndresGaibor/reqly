---
id: CU-08
tipo: caso-de-uso
actor: usuario propietario y agente de IA
estado: formal
requisitos: [RF-011, RF-023]
---

# CU-08 Consultar glosario y decisiones

Actor: usuario propietario y agente de IA.
Requisitos: RF-011, RF-023
Precondición: el proyecto tiene GLOSSARY.md y, si hay decisiones, registros en docs/adr/.

Pasos principales:
1. El usuario abre el glosario (RF-011).
2. reqly muestra cada término con su definición y sus sinónimos rechazados (RF-011).
3. El usuario abre la vista de decisiones (RF-023).
4. reqly lista los ADR en orden numérico, con título y estado (RF-023).

Resultado: los términos y las decisiones del proyecto se consultan en un solo lugar.