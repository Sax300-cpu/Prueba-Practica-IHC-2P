# IHC-A-10 · Dashboard UX — Lector de pantalla

**Integrante asignado:** Ariel Cholota

## 1. Diagnóstico

### Persona usuaria
Evaluador que utiliza lector de pantalla.

### Tarea crítica
Navegar Stepper y checklist.

### Restricción obligatoria
Toda acción y resultado debe estar anunciado semánticamente.

### Fallo específico
El paso activo depende solo de color.

### Touchpoints (6–8)
1. Anunciar paso.
2. Navegar stepper.
3. Marcar checklist.
4. Anunciar resultado.

### Momentos de verdad (2)
1. Conocer el paso actual sin color.
2. Recibir anuncio de cada acción.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Paso activo solo por color | Accesibilidad (no color-only) | Alta |
| 2 | Sin anuncio semántico | Accesibilidad (aria-live) | Alta |
| 3 | Foco no visible | Accesibilidad (foco) | Media |

### Curva emocional inicial
Desorientación al no saber el paso actual; claridad al oír el estado anunciado.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Navegar stepper | Controles enfocables |
| R2 | Checklist | Checkboxes con nombre |
| R3 | Anunciar acciones | aria-live / role=status |
| R4 | Estado accesible del paso | aria-current="step" + texto |
| R5 | Foco visible | Anillo de foco |
| R6 | No depender del color | Número + texto + ícono |

## 3. Arquitectura y trazabilidad

### Flujo principal
Stepper → checklist.

### Rama editar/error
Paso ambiguo → texto accesible del paso activo.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Inicio | Stepper | 01 Inicio |
| R2 | Principal | Checklist | Checkboxes | 02 Acción |
| R3 | Principal | Checklist | aria-live | 02 Acción |
| R4 | Principal | Inicio | aria-current | 01 Inicio |
| R5 | Principal | Inicio | Anillo de foco | 01 Inicio |
| R6 | Principal | Inicio | Número + texto | 03 Error |

## 4. Estados de la interfaz
- **Normal:** paso actual por texto + semántica.
- **Procesando:** "Guardando…" anunciado.
- **Error:** paso ambiguo corregido + errores anunciados.
- **Éxito:** "Etapa completada" anunciado.

## 5. Incidencia sorpresa (min 100)
Añadir texto/estado accesible del paso activo y foco visible.

## 6. Pregunta de defensa
Demuestre cómo conoce el paso actual sin depender del color.
→ Mostrar texto/aria-current leído por el lector de pantalla.
