# IHC-A-02 · CaféU — Teclado por lesión temporal

**Integrante asignado:** Kevin Velasco

## 1. Diagnóstico

### Persona usuaria
Estudiante que utiliza teclado por una lesión temporal.

### Tarea crítica
Editar un pedido y finalizar sin ratón.

### Restricción obligatoria
Tabulación, Enter y Escape como medios de interacción.

### Fallo específico
El botón "Quitar" no tiene nombre accesible ni confirmación.

### Touchpoints (6–8)
1. Enfocar botón.
2. Tabular al control.
3. Activar "Quitar".
4. Confirmar eliminación.
5. Ver carrito actualizado.
6. Finalizar pedido.

### Momentos de verdad (2)
1. Poder quitar un ítem solo con teclado.
2. Confirmación visible tras eliminar.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | "Quitar" sin nombre accesible | Accesibilidad (WCAG nombre) | Alta |
| 2 | Sin confirmación al eliminar | Prevención de errores (Nielsen) | Alta |
| 3 | Foco no visible / orden de tabulación | Visibilidad del estado | Media |

### Curva emocional inicial
Frustración al no poder operar sin ratón y al perder un ítem por accidente; mejora al poder confirmar cada acción.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Navegable por Tab | Orden lógico de foco |
| R2 | Activar por Enter/Escape | Acciones con teclado |
| R3 | Nombre accesible en "Quitar" | aria-label "Quitar producto" |
| R4 | Confirmar eliminación | Diálogo de confirmación |
| R5 | Restaurar foco tras quitar | Foco vuelve al carrito |
| R6 | Finalizar sin ratón | Botón "Finalizar pedido" con Enter |

## 3. Arquitectura y trazabilidad

### Flujo principal
Carrito → editar → finalizar.

### Rama editar/error
Eliminar → confirmar (sí/no) → restaurar foco al carrito.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Mi pedido | Orden de tabulación | 01 Inicio |
| R2 | Principal | Mi pedido | Controles por teclado | 02 Acción |
| R3 | Editar/error | Mi pedido | Botón "Quitar" | 02 Acción |
| R4 | Editar/error | Diálogo | Confirmar/Cancelar | 03 Error |
| R5 | Editar/error | Mi pedido | Foco restaurado | 03 Error |
| R6 | Principal | Finalizar | Botón final | 04 Confirmación |

## 4. Estados de la interfaz
- **Normal:** controles habilitados, foco visible.
- **Procesando:** "Finalizando…" deshabilitado.
- **Error:** diálogo de confirmación de eliminación.
- **Éxito:** "¡Pedido finalizado!" con resumen.

## 5. Incidencia sorpresa (min 100)
Hacer identificables y operables los controles; restaurar foco después de quitar.

## 6. Pregunta de defensa
Demuestre edición, eliminación y confirmación sin usar el ratón.
