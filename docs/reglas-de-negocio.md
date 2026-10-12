# Reglas de negocio de reqly

### Estados
- Requisito: formal, revisado o retirado. De formal a revisado cuando el usuario lo revisa. Retirado es final.
- Ticket: pendiente, en curso, hecho o retirado. Retirado es final.
- Requerimiento: abierto o formalizado. De abierto a formalizado cuando la formalización termina.

### Identificadores
- RF-### y RNF-###, con tres dígitos. El agente usa el siguiente número libre al formalizar.
- Los IDs son únicos y permanentes. Un ID retirado no se reutiliza. reqly verifica que no haya duplicados.

### Huecos y avance
- Hueco de trazabilidad: RF "debe" no retirado sin caso de uso o sin criterios verificables.
- Los RNF no requieren caso de uso, solo criterios verificables.
- Avance: proporción de requisitos "debe" (RF y RNF) no retirados que tienen un ticket en estado hecho. Los "debería", los "podría", los pendientes y los supuestos no cuentan; se muestran aparte.

### Validaciones
- Campos obligatorios y formato: bloquean el guardado con aviso.
- Referencias rotas: se avisan y el guardado se hace.

Los supuestos y pendientes están en docs/pendientes.md.