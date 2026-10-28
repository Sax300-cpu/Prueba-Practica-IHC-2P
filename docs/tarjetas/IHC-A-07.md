# IHC-A-07 · Dashboard UX — Investigadora novata

**Integrante asignado:** Manolo García

## 1. Diagnóstico

### Persona usuaria
Investigadora novata que prepara una prueba.

### Tarea crítica
Configurar checklist y avanzar por etapas.

### Restricción obligatoria
Debe identificar en todo momento el paso actual.

### Fallo específico
Stepper permite saltar etapas sin completar requisitos.

### Touchpoints (6–8)
1. Ver stepper.
2. Configurar checklist.
3. Validar requisitos.
4. Avanzar etapa.
5. Ver progreso.

### Momentos de verdad (2)
1. Saber el paso actual.
2. Avanzar solo cuando está completo.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Saltar etapas sin completar | Prevención de errores (Nielsen) | Alta |
| 2 | Paso actual no claro | Visibilidad del estado | Media |
| 3 | Sin feedback de validación | Feedback | Media |

### Curva emocional inicial
Confusión por no saber el paso actual; confianza al ver el Stepper bloqueado correctamente.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Mostrar paso actual | "Paso X de 5" |
| R2 | Completar checklist | Checkboxes |
| R3 | Bloquear avance inválido | "Continuar" deshabilitado |
| R4 | Volver sin perder marcas | Estado preservado |
| R5 | Validar requisitos | Lista de faltantes |
| R6 | Explicar bloqueo | Mensaje de error |

## 3. Arquitectura y trazabilidad

### Flujo principal
Configurar → validar → avanzar.

### Rama editar/error
Avanzar sin completar → bloquear + explicar.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Inicio | Stepper | 01 Inicio |
| R2 | Principal | Checklist | Checkboxes | 02 Acción |
| R3 | Editar/error | Checklist | "Continuar" | 03 Error |
| R4 | Editar/error | Checklist | Estado preservado | 03 Error |
| R5 | Editar/error | Checklist | Lista faltantes | 03 Error |
| R6 | Editar/error | Checklist | Mensaje | 03 Error |

## 4. Estados de la interfaz
- **Normal:** checklist en progreso, "Continuar" deshabilitado.
- **Procesando:** "Guardando…".
- **Error:** avance bloqueado con explicación.
- **Éxito:** "Etapa completada".

## 5. Incidencia sorpresa (min 100)
Bloquear avances inválidos con explicación y permitir volver sin perder marcas.

## 6. Pregunta de defensa
¿Cómo aplica la visibilidad del estado del sistema de Nielsen?
→ Stepper resalta paso actual + mensaje de estado + progreso visible.
