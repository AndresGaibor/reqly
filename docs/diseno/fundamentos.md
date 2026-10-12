---
id: fundamentos
tipo: documento
nivel: sistema
estado: sin revisar
---

# Fundamentos de diseño de reqly

Tokens de la interfaz de reqly: color, tipografía, espaciado, radios y accesibilidad. Son la fuente de los componentes y de las pantallas. Se importarán a Penpot desde docs/diseno/tokens.json (S-16), que se creará al diseñar en Penpot.

## Colores primitivos

| Nombre | Valor |
| --- | --- |
| gray.50 | #F9FAFB |
| gray.100 | #F3F4F6 |
| gray.200 | #E5E7EB |
| gray.400 | #9CA3AF |
| gray.600 | #4B5563 |
| gray.700 | #374151 |
| gray.800 | #1F2937 |
| gray.900 | #111827 |
| blue.400 | #60A5FA |
| blue.600 | #2563EB |
| blue.700 | #1D4ED8 |
| green.600 | #16A34A |
| green.700 | #15803D |
| amber.600 | #D97706 |
| amber.800 | #92400E |
| red.600 | #DC2626 |
| red.700 | #B91C1C |
| white | #FFFFFF |

## Colores semánticos, modo claro

| Token | Valor | Uso | Contraste aproximado |
| --- | --- | --- | --- |
| color.background.default | #F9FAFB (gray.50) | fondo de la aplicación | base |
| color.surface.raised | #FFFFFF | tarjetas, paneles y tablas | base |
| color.text.primary | #111827 (gray.900) | títulos y texto principal | 17:1 |
| color.text.secondary | #4B5563 (gray.600) | metadatos y ayudas | 7.6:1 |
| color.border.default | #E5E7EB (gray.200) | separadores; no es texto | decorativo |
| color.interactive.default | #2563EB (blue.600) | botón primario, enlaces y foco | 5.2:1 con texto blanco |
| color.interactive.hover | #1D4ED8 (blue.700) | botón primario al pasar el cursor | no aplica |
| color.text.on-interactive | #FFFFFF | texto sobre color interactivo | 5.2:1 sobre blue.600 |
| color.feedback.success.text | #15803D (green.700) | texto de éxito, como "revisado" | 5.0:1 |
| color.feedback.success.fill | #16A34A (green.600) | iconos y barras de éxito | componente, 3:1 o más |
| color.feedback.warning.text | #92400E (amber.800) | texto de aviso | 7.1:1 |
| color.feedback.warning.fill | #D97706 (amber.600) | iconos y bordes de aviso | componente, 3:1 o más |
| color.feedback.error | #DC2626 (red.600) | texto de error y hueco | 4.8:1 |
| color.feedback.error.hover | #B91C1C (red.700) | error al pasar el cursor | no aplica |
| color.feedback.info | #2563EB (blue.600) | información | 5.2:1 |

Los contrastes son cálculos de luminancia. Se verifican en Penpot antes de cerrar cada pantalla.

## Colores semánticos, modo oscuro

| Token | Valor | Uso |
| --- | --- | --- |
| color.background.default | #111827 (gray.900) | fondo de la aplicación |
| color.surface.raised | #1F2937 (gray.800) | tarjetas, paneles y tablas |
| color.text.primary | #F9FAFB (gray.50) | texto principal |
| color.text.secondary | #9CA3AF (gray.400) | metadatos y ayudas |
| color.border.default | #374151 (gray.700) | separadores |
| color.interactive.default | #60A5FA (blue.400) | enlaces, foco y acciones |

Los colores de estado en modo oscuro se fijan al crear el tema en Penpot, y deben cumplir los mismos mínimos de contraste.

## Tipografía

- Fuente de interfaz: Inter.
- Fuente de identificadores, rutas y commits: JetBrains Mono.
- Escala de tamaños en píxeles: 12, 14, 16, 20, 24, 30 y 36.
- Pesos: 400, 500 y 600.
- Altura de línea: 1.5 en texto de cuerpo y 1.2 en títulos.
- Ancho máximo de lectura: 72 caracteres.

## Espaciado y radios

- Espaciado en píxeles: 4, 8, 12, 16, 24, 32, 48 y 64.
- Radios: 4 para campos e insignias; 8 para botones y tarjetas; 12 para diálogos; completo para píldoras.

## Accesibilidad

- Contraste mínimo: texto normal 4.5:1; texto grande y componentes de interfaz 3:1.
- Ningún estado se comunica solo con color: siempre con icono o texto.
- Foco visible: anillo azul de 2 px con separación de 2 px.
- Objetivos táctiles de al menos 44 px en móvil.
