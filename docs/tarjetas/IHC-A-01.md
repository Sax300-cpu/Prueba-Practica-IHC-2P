# IHC-A-01 · CaféU — Compra entre clases

**Integrante asignado:** Kevin Velasco

## 1. Diagnóstico

### Persona usuaria
Estudiante de primer nivel que compra entre clases, con prisa (3 minutos).

### Tarea crítica
Agregar café y sánduche; confirmar un pedido.

### Restricción obligatoria
Solo dispone de 3 minutos y utiliza pantalla de 360 px.

### Fallo específico
El total no cambia al variar cantidades.

### Touchpoints (6–8)
1. Ver menú.
2. Ver café.
3. Ver sánduche.
4. Ajustar cantidad.
5. Ver subtotal.
6. Revisar carrito.
7. Confirmar pedido.
8. Ver confirmación.

### Momentos de verdad (2)
1. El total se actualiza al variar cantidad (confianza).
2. La confirmación visible al final (cierre de la compra).

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Total no recalcula al variar cantidad | Visibilidad del estado del sistema (Nielsen) | Alta |
| 2 | Tap targets pequeños en 360 px | Ley de Fitts | Media |
| 3 | Sin feedback al cambiar cantidad | Feedback / carga cognitiva | Media |

### Curva emocional inicial
Sube al elegir productos, baja (frustración) al ver el total desactualizado y al no poder confirmar; recupera al final con la confirmación.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Agregar producto | Botón "Agregar al pedido" añade el ítem |
| R2 | Ajustar cantidad | Stepper +/− cambia la cantidad |
| R3 | Recalcular total en tiempo real | El total se actualiza al variar cantidad |
| R4 | Confirmar pedido | Botón "Confirmar pedido" finaliza |
| R5 | Mostrar confirmación con resumen | Pantalla con número y desglose |
| R6 | Operar en viewport 360 px | Sin scroll horizontal, targets ≥ 44 px |

## 3. Arquitectura y trazabilidad

### Flujo principal
Menú → agregar café → agregar sánduche → carrito → confirmar → confirmación.

### Rama editar/error
Cambiar cantidad → (total obsoleto) → recalcular/avisar → no confirmar importe viejo.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Menú | Tarjeta de producto | 02 Acción |
| R2 | Principal | Detalle | Stepper +/− | 02 Acción |
| R3 | Editar/error | Detalle | Subtotal en vivo | 02 Acción |
| R4 | Principal | Mi pedido | Botón confirmar | 03 Error |
| R5 | Principal | Confirmación | Número + resumen | 04 Confirmación |
| R6 | Todos | Todas | Layout 360 px | 01 Inicio |

## 4. Estados de la interfaz
- **Normal:** carrito con controles disponibles.
- **Procesando:** "Confirmando…" con botón deshabilitado.
- **Error:** total desactualizado (confirmación bloqueada).
- **Éxito:** confirmación con número #CU-104.

## 5. Incidencia sorpresa (min 100)
Recalcular el total y anunciar cada cambio; impedir confirmar un importe obsoleto.

## 6. Pregunta de defensa
¿Qué parte de la rama de editar del user flow se modifica?
→ El nodo "cambiar cantidad → actualizar subtotal" (se añade recálculo + bloqueo de confirmación obsoleta).
