# IHC-A-06 · CaféU — Red móvil inestable

**Integrante asignado:** Luis Miranda

## 1. Diagnóstico

### Persona usuaria
Estudiante con red móvil inestable.

### Tarea crítica
Confirmar pedido desde el teléfono.

### Restricción obligatoria
No se debe afirmar éxito mientras la confirmación está pendiente.

### Fallo específico
Dos pulsaciones generan confirmaciones duplicadas.

### Touchpoints (6–8)
1. Confirmar pedido.
2. Esperar (procesando).
3. Ver estado.
4. Reintentar/volver.

### Momentos de verdad (2)
1. Saber que NO se duplicó el pedido.
2. Ver el estado final inequívoco.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Doble confirmación | Prevención de errores | Alta |
| 2 | Afirma éxito mientras está pendiente | Visibilidad del estado | Alta |
| 3 | No distingue los estados | Reconocimiento vs recuerdo | Media |

### Curva emocional inicial
Incertidumbre y miedo a pagar doble; alivio al ver estados claros (pendiente/confirmado).

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Confirmar pedido | Botón confirmar |
| R2 | Modelar pendiente/confirmado/no confirmado | Tres estados visibles |
| R3 | Evitar duplicados | Botón deshabilitado al procesar |
| R4 | Mostrar estado de red | Indicador "Red: inestable" |
| R5 | Recuperación | Botón "Reintentar" |
| R6 | No afirmar éxito prematuro | Éxito solo tras registro |

## 3. Arquitectura y trazabilidad

### Flujo principal
Confirmar → pendiente → confirmado.

### Rama editar/error
Pulsación repetida → botón deshabilitado + estado "pendiente".

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Revisar | Botón confirmar | 02 Acción |
| R2 | Principal | Estado | 3 estados | 03 Error |
| R3 | Principal | Estado | Botón deshabilitado | 03 Error |
| R4 | Principal | Inicio | Indicador red | 01 Inicio |
| R5 | Editar/error | Estado | "Reintentar" | 03 Error |
| R6 | Principal | Confirmación | Éxito real | 04 Confirmación |

## 4. Estados de la interfaz
- **Normal:** revisión, botón habilitado.
- **Pendiente:** "Confirmando…" deshabilitado.
- **No confirmado:** "No se pudo confirmar" + reintentar.
- **Confirmado:** éxito solo tras registro.

## 5. Incidencia sorpresa (min 100)
Modelar pendiente / confirmado / no confirmado y evitar duplicación.

## 6. Pregunta de defensa
¿Cómo diferencia visualmente y semánticamente los tres estados?
→ Color + ícono + texto + aria-live (no solo color).
