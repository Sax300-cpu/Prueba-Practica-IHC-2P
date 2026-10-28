# IHC-A-04 · CaféU — Alergia alimentaria declarada

**Integrante asignado:** Luis Miranda

## 1. Diagnóstico

### Persona usuaria
Estudiante con alergia alimentaria declarada.

### Tarea crítica
Consultar un producto y corregir el pedido.

### Restricción obligatoria
La advertencia de alérgenos debe ser perceptible antes de confirmar.

### Fallo específico
Se permite confirmar sin leer la advertencia de ingredientes.

### Touchpoints (6–8)
1. Ver producto.
2. Leer advertencia de alérgenos.
3. Agregar producto.
4. Revisar pedido.
5. Corregir pedido.
6. Confirmar pedido.

### Momentos de verdad (2)
1. Percibir la advertencia antes de confirmar.
2. Poder corregir sin perder el pedido.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Confirma sin leer advertencia | Prevención de errores (Nielsen) | Alta |
| 2 | Advertencia no perceptible/accesible | Accesibilidad (WCAG) | Alta |
| 3 | No permite corregir sin perder pedido | Flexibilidad (Nielsen) | Media |

### Curva emocional inicial
Tensión por el riesgo de alérgenos; seguridad al ver la advertencia clara y poder corregir.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Consultar producto | Pantalla de detalle |
| R2 | Mostrar alérgenos perceptibles | Sección "Ingredientes y alérgenos" |
| R3 | Confirmación explícita de lectura | Checkbox obligatorio |
| R4 | Corregir pedido | Botón "Editar pedido" |
| R5 | Mantener pedido al volver | Carrito preservado |
| R6 | Advertencia accesible | role="alert" + ícono |

## 3. Arquitectura y trazabilidad

### Flujo principal
Detalle → advertencia → agregar → confirmar.

### Rama editar/error
Confirmar sin leer → bloquear + obligar a reconocer la advertencia.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Detalle | Tarjeta producto | 02 Acción |
| R2 | Principal | Detalle | Panel alérgenos | 02 Acción |
| R3 | Principal | Detalle | Checkbox | 03 Error |
| R4 | Editar/error | Revisar | Botón editar | 04 Confirmación |
| R5 | Editar/error | Revisar | Carrito preservado | 04 Confirmación |
| R6 | Principal | Detalle | role="alert" | 02 Acción |

## 4. Estados de la interfaz
- **Normal:** detalle con advertencia visible.
- **Procesando:** "Confirmando…".
- **Error:** advertencia no reconocida (botón bloqueado).
- **Éxito:** confirmación tras reconocer la advertencia.

## 5. Incidencia sorpresa (min 100)
Incorporar aviso accesible y opción de volver a editar sin perder pedido.

## 6. Pregunta de defensa
¿Cómo prueba que el usuario comprende y puede corregir su elección?
→ Prueba cognitiva: observa si lee la advertencia y si vuelve atrás sin perder ítems.
