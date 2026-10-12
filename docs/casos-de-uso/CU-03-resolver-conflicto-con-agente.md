---
id: CU-03
tipo: caso-de-uso
actor: usuario propietario y agente de IA
estado: formal
requisitos: [RF-007, RF-008]
---

# CU-03 Resolver un conflicto con un agente

Actor: usuario propietario y agente de IA.

Requisitos: RF-007, RF-008.

Precondición: el usuario tiene un archivo abierto para editar.

Pasos principales:
1. El usuario edita un archivo.
2. Un agente cambia el mismo archivo en disco.
3. El usuario intenta guardar.
4. reqly no guarda y muestra ambas versiones lado a lado.
5. El usuario elige conservar una versión, o combina las dos a mano.
6. reqly guarda la versión elegida y crea un commit (RF-007).

Resultado: nada se sobrescribe sin decisión del usuario.