# IHC-A-08 · Dashboard UX — Docente contrarreloj

**Integrante asignado:** Manolo García

## 1. Diagnóstico

### Persona usuaria
Docente evaluador que prepara sesión contrarreloj.

### Tarea crítica
Completar datos de prueba y checklist.

### Restricción obligatoria
El procedimiento debe quedar claro antes de iniciar.

### Fallo específico
Las casillas parecen guardadas pero se pierden al cambiar de paso.

### Touchpoints (6–8)
1. Ver procedimiento.
2. Completar datos.
3. Marcar checklist.
4. Cambiar paso.
5. Verificar guardado.

### Momentos de verdad (2)
1. Confirmar que el checklist quedó guardado.
2. Ver progreso real.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Casillas no guardadas | Visibilidad del estado | Alta |
| 2 | No distingue guardado/no guardado | Feedback | Alta |
| 3 | Procedimiento poco claro | Reconocimiento vs recuerdo | Media |

### Curva emocional inicial
Frustración al perder datos; alivio al ver el estado "Guardado" explícito.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Completar datos | Campos del formulario |
| R2 | Checklist | Checkboxes |
| R3 | Preservar checklist entre pasos | Persistencia |
| R4 | Distinguir guardado/no guardado | Badge "Guardado"/"Sin guardar" |
| R5 | Mostrar progreso | "X de Y completados" |
| R6 | Procedimiento claro inicial | Pantalla de procedimiento |

## 3. Arquitectura y trazabilidad

### Flujo principal
Instrucciones → completar → guardar → cambiar paso.

### Rama editar/error
Cambiar paso sin guardar → aviso + preservar.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Datos | Campos | 02 Acción |
| R2 | Principal | Checklist | Checkboxes | 02 Acción |
| R3 | Principal | Checklist | Persistencia | 02 Acción |
| R4 | Principal | Checklist | Badge guardado | 02 Acción |
| R5 | Principal | Checklist | Progreso | 04 Confirmación |
| R6 | Principal | Inicio | Procedimiento | 01 Inicio |

## 4. Estados de la interfaz
- **Normal:** formulario con badges de guardado.
- **Procesando:** "Guardando…".
- **Error:** "Tienes cambios sin guardar".
- **Éxito:** "Cambios guardados".

## 5. Incidencia sorpresa (min 100)
Preservar checklist, diferenciar guardado de no guardado y mostrar progreso.

## 6. Pregunta de defensa
¿Qué evidencia muestra una mejora real frente a una mejora inferida?
→ Comparar métricas observadas antes/después (errores, tiempo, pausas), no suposiciones.
