# IHC-A-05 · CaféU — Presupuesto USD 4,25

**Integrante asignado:** Luis Miranda

## 1. Diagnóstico

### Persona usuaria
Estudiante con presupuesto de USD 4,25.

### Tarea crítica
Añadir productos, ajustar cantidades y revisar total.

### Restricción obligatoria
No exceder el presupuesto sin aviso claro.

### Fallo específico
Una edición genera sobrecosto sin feedback.

### Touchpoints (6–8)
1. Ver productos.
2. Añadir producto.
3. Ajustar cantidad.
4. Ver total.
5. Ver aviso de presupuesto.
6. Revisar pedido.

### Momentos de verdad (2)
1. El aviso de sobrecosto (el total vs. presupuesto pasa a ser momento de verdad).
2. La decisión de ajustar o confirmar.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Sobrecosto sin feedback | Visibilidad del estado | Alta |
| 2 | No avisa antes de confirmar | Prevención de errores | Alta |
| 3 | No permite ajustar manteniendo carrito | Flexibilidad | Media |

### Curva emocional inicial
Frustración al superar el presupuesto sin aviso; alivio al poder ajustar sin perder el pedido.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Añadir producto | Botón agregar |
| R2 | Ajustar cantidades | Stepper +/− |
| R3 | Calcular total | Total en vivo |
| R4 | Avisar si excede presupuesto | Banner de sobrecosto |
| R5 | Ajustar manteniendo carrito | Botón "Ajustar pedido" |
| R6 | Avisar antes de confirmar | Confirmación con aviso |

## 3. Arquitectura y trazabilidad

### Flujo principal
Menú → añadir → ajustar → revisar total.

### Rama editar/error
Edición con sobrecosto → aviso + opción de ajustar sin vaciar carrito.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Menú | Tarjeta producto | 02 Acción |
| R2 | Principal | Detalle | Stepper | 02 Acción |
| R3 | Principal | Detalle | Total en vivo | 02 Acción |
| R4 | Editar/error | Detalle | Banner sobrecosto | 03 Error |
| R5 | Editar/error | Revisar | "Ajustar pedido" | 03 Error |
| R6 | Principal | Revisar | Confirmación | 04 Confirmación |

## 4. Estados de la interfaz
- **Normal:** total dentro del presupuesto.
- **Procesando:** "Confirmando…".
- **Error:** sobrecosto (confirmación bloqueada).
- **Éxito:** confirmación dentro del presupuesto.

## 5. Incidencia sorpresa (min 100)
Avisar antes de confirmar y ofrecer ajustar el pedido manteniendo el carrito.

## 6. Pregunta de defensa
¿Qué touchpoint pasa a ser momento de verdad y por qué?
→ "Ver total vs. presupuesto" → genera confianza/frustración que define la experiencia.
