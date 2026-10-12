# Visión de reqly

## Problema

Los documentos de ingeniería de cada proyecto (requerimientos, requisitos, casos de uso, glosario, decisiones, tickets) son archivos Markdown separados en el repo. Leerlos uno por uno en un editor es lento. No hay forma de ver de un vistazo qué requisitos no tienen caso de uso, qué falta para terminar el proyecto ni cuál es el avance.

## Objetivo

reqly muestra y edita esos documentos en una interfaz web, en un solo lugar, y hace visible la trazabilidad entre requerimiento, requisito, caso de uso, diseño en Penpot, ticket y prueba. El repositorio es la única fuente de verdad: reqly no tiene base de datos propia ni formato propio.

## Métrica de éxito

Cero huecos de trazabilidad en los requisitos funcionales "debe" antes de declarar un proyecto terminado. Un hueco es un requisito funcional "debe" no retirado sin caso de uso o sin criterios verificables. Los requisitos no funcionales se verifican con criterios y no requieren caso de uso.

## Alcance de v1

Dentro de v1:

- Cargar una carpeta de proyecto y sus documentos Markdown.
- Ver el avance y los huecos, la vista de documento con índice lateral, las tablas desde el frontmatter y la matriz de trazabilidad.
- Editar Markdown con vista previa, con commit automático por guardado y detección de conflictos con agentes.
- Ver el diseño de Penpot en solo lectura: vista gráfica o referencia.
- Diseño en Penpot guiado por la skill reqly-disenar, documentado en docs/diseno/.
- Capturar requerimientos, notas, pendientes, glosario y ADR.
- Skills del proyecto para formalizar, migrar, diseñar y aplicar las reglas de ingeniería, instaladas al seleccionar el proyecto.
- Historial por elemento desde git.

## Fuera de alcance

- Editar diseños en Penpot desde la interfaz de reqly. El agente sí diseña en Penpot, guiado por la skill reqly-disenar (RF-029).
- Diagramas Mermaid y HTML animado. Después de v1.
- Exportar a Word o PDF. Después de v1.
- Grafo visual de tickets con dependencias. [SUPUESTO] Fuera de v1.
- Varios usuarios, login propio y roles.
- Importación automática de documentos desde Notion, Word u otros repos.
- Tracker externo para specs y tickets. Todo vive en el repo.

## Restricciones

- Presupuesto: ninguno adicional. Se usan los recursos ya instalados en la VM y los servicios que ya se pagan.
- Plazo: ninguno fijo. El objetivo es una versión útil cuanto antes para el proyecto actual.
- Tecnología obligatoria: Bun como entorno de ejecución y React para la interfaz.
- Despliegue: stack Docker Compose detrás de Traefik, con Sablier para escalar a cero. Dokploy queda descartado.
- Acceso: solo por Tailscale, sin login propio en v1.
- Normativa: no aplica en v1 por ser uso personal. [SUPUESTO] Se revisa al definir exportaciones para clientes.

## Actores

- Usuario propietario: administra el proyecto y tiene control total sobre sus archivos.
- Agente de IA: lee y escribe archivos del repo y hace commits.