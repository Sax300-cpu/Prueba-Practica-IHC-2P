# IHC-A-11 · Dashboard UX — Monitor pequeño

**Integrante asignado:** Ariel Cholota

## 1. Diagnóstico

### Persona usuaria
Evaluadora que trabaja en un monitor pequeño.

### Tarea crítica
Registrar etapa, errores y observaciones.

### Restricción obligatoria
Mantener jerarquía en un ancho de 360 px.

### Fallo específico
Card UI se superpone al Stepper y oculta campos.

### Touchpoints (6–8)
1. Ver stepper.
2. Registrar etapa.
3. Registrar errores.
4. Registrar observaciones.

### Momentos de verdad (2)
1. Poder ver/completar todos los campos.
2. Mantener orden lógico.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Card superpuesta al Stepper | Jerarquía / Gestalt | Alta |
| 2 | Campos ocultos | Visibilidad del estado | Alta |
| 3 | Jerarquía perdida en 360 px | Carga cognitiva | Media |

### Curva emocional inicial
Frustración al no ver los campos; claridad al apilar el layout sin solaparse.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Registrar etapa | Campo etapa |
| R2 | Registrar errores | Campo errores |
| R3 | Registrar observaciones | Campo observaciones |
| R4 | Layout responsivo 360 px | Sin solapamiento |
| R5 | Orden lógico de foco | Foco sigue orden visual |
| R6 | Jerarquía visual | Tarjetas apiladas |

## 3. Arquitectura y trazabilidad

### Flujo principal
Stepper → card → registrar.

### Rama editar/error
Campos ocultos → reorganizar layout.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Registrar | Campo etapa | 02 Acción |
| R2 | Principal | Registrar | Campo errores | 02 Acción |
| R3 | Principal | Registrar | Campo observaciones | 02 Acción |
| R4 | Principal | Registrar | Layout apilado | 01 Inicio |
| R5 | Principal | Registrar | Orden de foco | 03 Error |
| R6 | Principal | Registrar | Tarjetas | 03 Error |

## 4. Estados de la interfaz
- **Normal:** formulario responsivo a 360 px.
- **Procesando:** "Guardando…".
- **Error:** solapamiento corregido + orden de foco.
- **Éxito:** "Datos guardados".

## 5. Incidencia sorpresa (min 100)
Reorganizar layout responsivo y conservar orden lógico del foco.

## 6. Pregunta de defensa
¿Qué ley Gestalt aplica y qué carga cognitiva se reduce?
→ Proximidad (agrupar campos por etapa) → reduce búsqueda visual y carga de memoria.
