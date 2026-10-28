# IHC-A-03 · CaféU — Dispositivo compartido

**Integrante asignado:** Kevin Velasco

## 1. Diagnóstico

### Persona usuaria
Estudiante que comparte dispositivo y debe salir rápido.

### Tarea crítica
Confirmar pedido y comprobar que se recibió.

### Restricción obligatoria
No puede exponerse un número personal ni guardar datos sensibles.

### Fallo específico
La pantalla dice "Listo" pero no muestra número ni resumen.

### Touchpoints (6–8)
1. Confirmar pedido.
2. Ver estado.
3. Ver número de pedido.
4. Ver resumen.
5. Salir rápido.

### Momentos de verdad (2)
1. Ver un identificador de pedido.
2. Ver el estado inequívoco "recibido".

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | "Listo" sin número ni resumen | Visibilidad del estado | Alta |
| 2 | Sin desglose | Reconocimiento vs recuerdo | Media |
| 3 | Riesgo de exponer datos personales | Privacidad | Media |

### Curva emocional inicial
Confusión al no poder verificar el pedido; alivio al ver número y resumen.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Confirmar pedido | Botón "Confirmar pedido" |
| R2 | Mostrar identificador simulado | Código #CU-104 |
| R3 | Mostrar desglose | Lista de ítems y precios |
| R4 | Estado inequívoco "recibido" | Mensaje + checkmark |
| R5 | No almacenar datos sensibles | Nota de privacidad |
| R6 | Permitir salir rápido | Botón "Cerrar" |

## 3. Arquitectura y trazabilidad

### Flujo principal
Carrito → confirmar → confirmación con número.

### Rama editar/error
Clic sin confirmar → botón deshabilitado + estado explícito.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Revisar | Botón confirmar | 02 Acción |
| R2 | Principal | Confirmación | Código de retiro | 04 Confirmación |
| R3 | Principal | Confirmación | Desglose | 04 Confirmación |
| R4 | Principal | Confirmación | Mensaje "recibido" | 04 Confirmación |
| R5 | Principal | Revisar | Nota privacidad | 01 Inicio |
| R6 | Principal | Confirmación | Botón "Cerrar" | 04 Confirmación |

## 4. Estados de la interfaz
- **Normal:** revisión con controles.
- **Procesando:** "Confirmando…" deshabilitado.
- **Error:** "No se pudo confirmar" con reintentar.
- **Éxito:** "¡Pedido recibido!" con #CU-104 y resumen.

## 5. Incidencia sorpresa (min 100)
Mostrar un identificador simulado, desglose y estado inequívoco de pedido recibido.

## 6. Pregunta de defensa
¿Cómo evita confundir clic efectuado con pedido confirmado?
→ Estado explícito + botón deshabilitado tras confirmar + mensaje de éxito.
