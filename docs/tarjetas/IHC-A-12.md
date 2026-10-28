# IHC-A-12 · Dashboard UX — Prueba interrumpida

**Integrante asignado:** Ariel Cholota

## 1. Diagnóstico

### Persona usuaria
Investigadora que retoma una prueba interrumpida.

### Tarea crítica
Recuperar checklist y cerrar sesión.

### Restricción obligatoria
No perder los pasos previamente finalizados.

### Fallo específico
El estado final aparece sin comprobar checklist obligatorio.

### Touchpoints (6–8)
1. Reanudar.
2. Ver checklist recuperado.
3. Revisar pasos.
4. Cerrar sesión.
5. Ver estado final.

### Momentos de verdad (2)
1. Recuperar el checklist sin perder pasos.
2. Comprobar el estado final.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Estado final sin comprobar checklist | Prevención de errores | Alta |
| 2 | Pérdida de pasos | Visibilidad del estado | Alta |
| 3 | Éxito falso | Feedback honesto | Media |

### Curva emocional inicial
Miedo a perder el trabajo; alivio al recuperar los pasos y verificar antes de cerrar.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Recuperar checklist | Estado persistido |
| R2 | Preservar pasos finalizados | Pasos marcados |
| R3 | Comprobar checklist obligatorio | Validación previa |
| R4 | Revisión previa | Pantalla de resumen |
| R5 | Resumen comprobable | "X de Y completados" |
| R6 | Cerrar sin éxito falso | "Finalizar" bloqueado hasta verificar |

## 3. Arquitectura y trazabilidad

### Flujo principal
Reanudar → ver checklist → cerrar.

### Rama editar/error
Checklist incompleto → bloquear cierre.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Inicio | Botón reanudar | 01 Inicio |
| R2 | Principal | Checklist | Pasos marcados | 02 Acción |
| R3 | Editar/error | Cierre | Validación | 03 Error |
| R4 | Principal | Revisión | Resumen | 04 Confirmación |
| R5 | Principal | Revisión | "X de Y" | 04 Confirmación |
| R6 | Principal | Cierre | Botón finalizar | 03 Error |

## 4. Estados de la interfaz
- **Normal:** checklist recuperado con progreso.
- **Procesando:** "Guardando…".
- **Error:** cierre bloqueado (checklist incompleto).
- **Éxito:** "Sesión finalizada" solo tras verificar.

## 5. Incidencia sorpresa (min 100)
Añadir revisión previa y resumen comprobable; evitar éxito falso.

## 6. Pregunta de defensa
¿Cómo muestra el momento de verdad y comprueba el estado final?
→ Resumen comprobable + bloqueo de éxito falso (validar antes de confirmar).
