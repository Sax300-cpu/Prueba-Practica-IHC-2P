# IHC-A-09 · Dashboard UX — Participantes anónimos

**Integrante asignado:** Manolo García

## 1. Diagnóstico

### Persona usuaria
Investigadora que trabaja con participantes anónimos.

### Tarea crítica
Registrar resultados y finalizar sesión.

### Restricción obligatoria
No mostrar nombres reales en evidencias.

### Fallo específico
Un formulario exige nombre real y no admite código de participante.

### Touchpoints (6–8)
1. Registrar resultado.
2. Ingresar participante.
3. Finalizar sesión.

### Momentos de verdad (2)
1. Registrar sin exponer identidad.
2. Finalizar con datos válidos.

### Fallos priorizados (3)
| # | Fallo | Principio HCI | Severidad |
|---|---|---|---|
| 1 | Exige nombre real | Privacidad | Alta |
| 2 | No admite código | Flexibilidad | Alta |
| 3 | Riesgo de privacidad en evidencias | Privacidad | Media |

### Curva emocional inicial
Preocupación por la privacidad; confianza al usar códigos anónimos validados.

## 2. Requisitos verificables (6)
| ID | Requisito | Verificable mediante |
|---|---|---|
| R1 | Registrar resultados | Formulario |
| R2 | Usar código seudónimo | Campo "Código de participante" |
| R3 | Validar formato del código | Regex P-### |
| R4 | Finalizar sesión | Botón finalizar |
| R5 | No mostrar nombres reales | Sin campos de nombre |
| R6 | Proteger privacidad | Nota de privacidad |

## 3. Arquitectura y trazabilidad

### Flujo principal
Registrar → código → finalizar.

### Rama editar/error
Nombre real / código inválido → validar.

### Matriz de trazabilidad
| Requisito | Flujo | Pantalla | Componente | Wireframe |
|---|---|---|---|---|
| R1 | Principal | Resultados | Formulario | 02 Acción |
| R2 | Principal | Resultados | Campo código | 02 Acción |
| R3 | Editar/error | Resultados | Validación | 03 Error |
| R4 | Principal | Sesión | Botón finalizar | 04 Confirmación |
| R5 | Principal | Resultados | Sin nombre real | 02 Acción |
| R6 | Principal | Sesión | Nota privacidad | 01 Inicio |

## 4. Estados de la interfaz
- **Normal:** formulario con campo código.
- **Procesando:** "Guardando…".
- **Error:** "Código inválido" (formato P-###).
- **Éxito:** "Sesión finalizada" solo con códigos.

## 5. Incidencia sorpresa (min 100)
Sustituir por código seudónimo y validar su formato.

## 6. Pregunta de defensa
¿Qué requisito protege privacidad y dónde aparece en la trazabilidad?
→ R5/R6 → matriz trazabilidad (requisito → pantalla → componente).
