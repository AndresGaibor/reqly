# Diseño de reqly

Documentación de diseño de la interfaz de reqly, lista para diseñarla en Penpot. Todo está en estado sin revisar y con Penpot pendiente. Ningún valor de color, espacio o radio se escribe suelto: sale de fundamentos.md.

## Orden de trabajo

1. Fundamentos (fundamentos.md).
2. Componentes de átomo a organismo (componentes/).
3. Plantillas (plantillas/).
4. Pantallas con sus estados (pantallas/).
5. Flujos, uniendo pantallas (flujos/).
6. Prototipo en Penpot, una vez revisados los flujos.

## Índice

### Fundamentos

- [fundamentos.md](fundamentos.md): tokens de color, espacio, radio y tipografía, y sus reglas de uso.

### Componentes

- [atomo-banner.md](componentes/atomo-banner.md): banner de aviso para mensajes y errores.
- [atomo-boton.md](componentes/atomo-boton.md): botón con sus variantes y estados.
- [atomo-campo.md](componentes/atomo-campo.md): campo de formulario con etiqueta y validación.
- [atomo-insignia.md](componentes/atomo-insignia.md): insignia de estado.
- [molecula-celda-trazabilidad.md](componentes/molecula-celda-trazabilidad.md): celda de la matriz de trazabilidad.
- [molecula-elemento-lista.md](componentes/molecula-elemento-lista.md): elemento de lista para glosario, decisiones, pendientes y requerimientos.
- [molecula-pestanas.md](componentes/molecula-pestanas.md): grupo de pestañas.
- [molecula-tarjeta-metrica.md](componentes/molecula-tarjeta-metrica.md): tarjeta de métrica.
- [organismo-barra-lateral.md](componentes/organismo-barra-lateral.md): barra lateral de navegación.
- [organismo-cabecera.md](componentes/organismo-cabecera.md): cabecera de la aplicación.
- [organismo-dialogo.md](componentes/organismo-dialogo.md): diálogo modal.
- [organismo-tabla.md](componentes/organismo-tabla.md): tabla de datos con cabecera, filas y orden.

### Plantillas

- [plantilla-app-shell.md](plantillas/plantilla-app-shell.md): plantilla base de una pantalla de reqly.

### Pantallas

- [CU-01-P1-seleccionar-proyecto.md](pantallas/CU-01-P1-seleccionar-proyecto.md): selección de la carpeta o repositorio, con aviso de ID duplicado.
- [CU-01-P2-avance.md](pantallas/CU-01-P2-avance.md): avance, huecos, pendientes y supuestos.
- [CU-01-P3-matriz-trazabilidad.md](pantallas/CU-01-P3-matriz-trazabilidad.md): matriz de trazabilidad.
- [CU-01-P4-documento.md](pantallas/CU-01-P4-documento.md): documento continuo del proyecto.
- [CU-01-P5-editor-vista-previa.md](pantallas/CU-01-P5-editor-vista-previa.md): editor con vista previa, validaciones y guardado por commit.
- [CU-01-P6-conflicto-agente.md](pantallas/CU-01-P6-conflicto-agente.md): conflicto con lo que propone el agente y guardado por commit.
- [CU-01-P7-ficha-requisito.md](pantallas/CU-01-P7-ficha-requisito.md): ficha del requisito, con diseño en solo lectura y marcado como revisado.
- [CU-01-P8-historial.md](pantallas/CU-01-P8-historial.md): historial de commits.
- [CU-01-P9-tabla-elementos.md](pantallas/CU-01-P9-tabla-elementos.md): tabla de elementos del proyecto.
- [CU-02-P14-captura-requerimiento.md](pantallas/CU-02-P14-captura-requerimiento.md): captura de un requerimiento, con estado formalizado.
- [CU-02-P15-revision.md](pantallas/CU-02-P15-revision.md): revisión de lo capturado, con marcado como revisado y advertencias.
- [CU-04-P12-pendientes.md](pantallas/CU-04-P12-pendientes.md): lista de pendientes y supuestos.
- [CU-04-P13-nota.md](pantallas/CU-04-P13-nota.md): nota con su marca y guardado por commit.
- [CU-05-P20-diseno.md](pantallas/CU-05-P20-diseno.md): diseño del requisito en solo lectura.
- [CU-06-P18-migracion.md](pantallas/CU-06-P18-migracion.md): migración por bloques, con notas y guardado por commit.
- [CU-07-P16-tickets.md](pantallas/CU-07-P16-tickets.md): tickets por estado y sus transiciones, con guardado por commit.
- [CU-07-P19-retirar.md](pantallas/CU-07-P19-retirar.md): retirar un ticket sin borrarlo.
- [CU-08-P10-glosario.md](pantallas/CU-08-P10-glosario.md): glosario.
- [CU-08-P11-decisiones.md](pantallas/CU-08-P11-decisiones.md): decisiones (ADR), con guardado por commit.
- [CU-09-P17-skills.md](pantallas/CU-09-P17-skills.md): versión de las skills instaladas.

### Flujos

- [CU-01-revisar-estado.md](flujos/CU-01-revisar-estado.md): recorrido principal para revisar el estado de un requisito.
- [CU-02-capturar-formalizar.md](flujos/CU-02-capturar-formalizar.md): captura de un requerimiento y su formalización.
- [CU-03-conflicto-agente.md](flujos/CU-03-conflicto-agente.md): resolución de un conflicto con el agente.
- [CU-04-nota-pendiente.md](flujos/CU-04-nota-pendiente.md): alta de una nota y de un pendiente.
- [CU-05-ver-diseno.md](flujos/CU-05-ver-diseno.md): consulta del diseño de un requisito.
- [CU-06-migracion-bloques.md](flujos/CU-06-migracion-bloques.md): migración de contenido por bloques.
- [CU-07-estado-ticket.md](flujos/CU-07-estado-ticket.md): cambio de estado y retirada de un ticket.
- [CU-08-glosario-decisiones.md](flujos/CU-08-glosario-decisiones.md): consulta del glosario y de las decisiones.
- [CU-09-mantener-skills.md](flujos/CU-09-mantener-skills.md): mantenimiento de las skills del proyecto.

### Cobertura

- [cobertura.md](cobertura.md): qué requisito y qué caso de uso tienen pantalla o flujo.

## Decisiones confirmadas

- Los tokens viven en docs/diseno/tokens.json y Penpot los importa; el repo es la fuente (S-16).
- El diseño va en el archivo de Penpot conectado, en páginas nuevas; las páginas existentes no se tocan (S-17, P-17).
- El primer caso de uso es CU-01 (P-18).
- Los ADR se leen y se crean desde reqly; un ADR aceptado se reemplaza (S-07).

## Pendientes antes de diseñar en Penpot

- Confirmar que la versión de Penpot importa tokens.json sin errores (P-15).
- Confirmar que el acceso de reqly a Penpot cubre las vistas previas (P-01).
- Definir el formato de los tickets y pruebas (P-06), que no afecta a las pantallas de CU-01.

## Cómo usar esta documentación

La skill reqly-disenar guía al agente para llevar cada caso de uso a Penpot, documentando cada elemento aquí. El diseñador usa cobertura.md para comprobar que cada requisito tiene pantalla.
