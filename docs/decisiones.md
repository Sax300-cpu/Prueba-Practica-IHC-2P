# Decisiones de diseño

## Fidelidad
Wireframes de **baja-media fidelidad**: estructura y jerarquía claras, colores institucionales, textos reales y placeholders de imagen, sin acabado visual final. Suficiente para validar arquitectura, navegación, estados y feedback.

## Herramienta utilizada
**Penpot** (open-source), generando los wireframes y el prototipo de forma programática mediante la API del plugin (MCP).

## Justificación
- Penpot permite crear boards, formas, textos y conectar pantallas con interacciones (prototipo navegable).
- La baja-media fidelidad permite iterar rápido y centrarse en los criterios HCI (estados, feedback, accesibilidad) sin invertir en pulido visual.
- Se incorporó accesibilidad desde el wireframe: foco visible, nombres accesibles y ausencia de "solo color".

## Guía de ejecución del prototipo
1. Abrir el archivo "New File 2" en Penpot.
2. Recorrer las 12 tarjetas (48 pantallas) organizadas por filas.
3. Cada tarjeta tiene 4 pantallas: Inicio → Acción → Error → Confirmación.
4. (Pendiente) Conectar interacciones para el prototipo clicable.
