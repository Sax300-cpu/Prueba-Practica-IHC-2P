# Prueba-Practica-IHC-2P

Prueba Práctica Integradora — **Interacción Humano-Computador (IHC)** · Paralelo A · Quinto nivel.

Diagnóstico, diseño, prototipado, prueba y corrección de interfaces mediante evidencias nuevas y **colaboración verificable en GitHub**. El proyecto cubre **12 tarjetas privadas** (6 de CaféU y 6 de Dashboard UX).

## Integrantes y asignación

| Integrante | Tarjetas | Dominio |
|---|---|---|
| **Kevin Andrés Velasco Huayamave** | IHC-A-01, 02, 03 | CaféU |
| **Luis Sebastián Miranda Tarupi** | IHC-A-04, 05, 06 | CaféU |
| **Manolo José García Amores** | IHC-A-07, 08, 09 | Dashboard UX |
| **Ariel Isai Cholota Bastidas** | IHC-A-10, 11, 12 | Dashboard UX |

## Las 12 tarjetas

| Tarjeta | Tema | Fallo específico corregido |
|---|---|---|
| IHC-A-01 | CaféU · Compra entre clases | El total no cambia al variar cantidades |
| IHC-A-02 | CaféU · Teclado por lesión temporal | "Quitar" sin nombre accesible ni confirmación |
| IHC-A-03 | CaféU · Dispositivo compartido | "Listo" sin número ni resumen |
| IHC-A-04 | CaféU · Alergia alimentaria | Confirma sin leer la advertencia de alérgenos |
| IHC-A-05 | CaféU · Presupuesto USD 4,25 | Una edición genera sobrecosto sin feedback |
| IHC-A-06 | CaféU · Red móvil inestable | Dos pulsaciones generan confirmaciones duplicadas |
| IHC-A-07 | Dashboard · Investigadora novata | El Stepper permite saltar etapas |
| IHC-A-08 | Dashboard · Docente contrarreloj | Las casillas se pierden al cambiar de paso |
| IHC-A-09 | Dashboard · Participantes anónimos | El formulario exige nombre real |
| IHC-A-10 | Dashboard · Lector de pantalla | El paso activo depende solo de color |
| IHC-A-11 | Dashboard · Monitor pequeño | Card UI se superpone al Stepper |
| IHC-A-12 | Dashboard · Prueba interrumpida | Estado final sin comprobar el checklist |

## Prototipo

- **Penpot** (archivo "New File 2"): 48 wireframes (12 tarjetas × 4 pantallas: inicio, acción, error, confirmación).
- Enlace al archivo: `[pendiente de agregar]`

## Estructura del repositorio

```
├── docs/
│   ├── diagnostico.md      # plantilla de diagnóstico emocional
│   ├── requisitos.md       # plantilla de requisitos
│   ├── trazabilidad.md     # plantilla de trazabilidad
│   ├── decisiones.md       # fidelidad y herramienta (Penpot)
│   ├── defensa.md          # estructura de defensa y contribución
│   └── tarjetas/           # documentación completa de las 12 tarjetas
│       ├── IHC-A-01.md … IHC-A-12.md
├── wireframes/
│   ├── IHC-1-2-3/          # Kevin (12 capturas)
│   ├── IHC-4-5-6/          # Luis
│   ├── IHC-7-8-9/          # Manolo
│   └── IHC-10-11-12/       # Ariel
├── pruebas/
│   └── sesion.md           # prueba cognitiva
├── prototipo/
│   ├── v1/
│   └── v2/
├── diagramas/
└── evidencias/
```

## Estado del proyecto

- [x] Documentación de las 12 tarjetas (`docs/tarjetas/`).
- [x] Wireframes de Kevin (`wireframes/IHC-1-2-3/`).
- [ ] Wireframes de Luis, Manolo y Ariel.
- [ ] Prueba cognitiva con datos reales (`pruebas/sesion.md`).
- [ ] Issues de hallazgo (mínimo 3).
- [ ] Incidencia sorpresa (minuto 100) y defensa individual.

## Colaboración en GitHub

- Cada integrante trabaja en **su propia rama** con **commits sustantivos**.
- Mínimo **1 Issue asignado** por persona y **1 PR revisado** (revisión cruzada).
- Flujo: `Issue → rama → commit → PR → revisión → merge`.
