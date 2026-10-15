# Enlace al Prototipo Comparativo en Figma (Frente C)

**Aplicación evaluada:** Banca Móvil Banco Pichincha (Ecuador) — Plataforma Android  
**Flujo:** Transferencia interbancaria a una cuenta no guardada de otro banco (`T01`–`T08`)  
**Responsable:** Erick López (`@ErickAloy871`) — Rol C  
**Rama:** `ape3/mejoras-figma`  
**Evidencia visual exportada en el repositorio:** [`antes-despues.png`](./antes-despues.png)

---

## 1. Enlace de Acceso Público y Verificable a Figma

* **Lienzo en Figma (acceso público de lectura habilitado — *Anyone with the link can view*):**  
  [Abrir Comparativo Antes / Después en Figma (Propuesta Académica)]https://www.figma.com/design/N9GTdrhdlkHe68FZRKCuPS/Untitled?node-id=0-1&t=VQ8A5s0pwI6FGAoQ-1  
  URL directa: `https://www.figma.com/design/N9GTdrhdlkHe68FZRKCuPS/Untitled?node-id=0-1&t=VQ8A5s0pwI6FGAoQ-1`

---

## 2. Estructura del Comparativo: Interfaz de Referencia vs. Rediseño Académico

En cumplimiento de los criterios de aceptación del Issue #3 y del documento `alcance-comun.md`, tanto el archivo en Figma como la imagen exportada [`antes-despues.png`](./antes-despues.png) presentan claramente diferenciadas las dos vistas lado a lado:

| Columna en el Lienzo | Categoría Declarada | Touchpoints Representados | Elementos Clave Visibles |
| :--- | :--- | :--- | :--- |
| **Izquierda (`ANTES`)** | **Recreación declarada de la interfaz de referencia** (elaborada a partir de la guía oficial de soporte de Banco Pichincha, sin capturas de sesiones bancarias reales). | `T04`, `T05` y `T07` | • Campos de cuenta e identificación en formato continuo sin segmentación visual (`T04`).<br>• Ausencia de indicador explícito que diferencie un titular validado en línea de uno digitado manualmente (`T05`).<br>• Resumen previo a confirmación con jerarquía visual plana, sin detalle de tiempo de acreditación ni botones de edición directa (`T07`). |
| **Derecha (`DESPUÉS`)** | **«Propuesta académica, no interfaz oficial»** (rediseño fundamentado en principios HCI). | `T04`, `T05` y `T07` | • **Mejora M1 (`T04`):** Número de cuenta segmentado en bloques de 4 dígitos (`0022 0098 7654 32`) para reducir la carga cognitiva y prevenir errores.<br>• **Mejora M2 (`T05`):** Tarjeta semántica en verde de *«Titular verificado en línea con Banco Guayaquil»* aplicando la Heurística #1 de Nielsen (Visibilidad del estado del sistema).<br>• **Mejora M3 (`T07`):** Resumen jerarquizado con monto destacado, desglose de comisión, etiqueta de tiempo de acreditación (*Pago Directo < 1 min*) y botones `Editar` por sección (Heurísticas #3 y #8). |

---

## 3. Declaración de Protección de Datos y Límites del Prototipo

1. **Datos 100% ficticios y anonimizados:** Ninguna de las pantallas en Figma ni en `antes-despues.png` incluye números de cuenta reales, números de cédula verdaderos, saldos personales, códigos OTP ni comprobantes identificables. Se emplean únicamente datos ficticios de prueba (*Carlos Méndez*, CI `1800***000`, cuenta `0022 0098 7654 32`, monto `$45.00`).
2. **Etiquetado académico obligatorio:** La propuesta de mejora incluye de forma visible dentro del propio diseño la leyenda explícita **«Propuesta académica, no interfaz oficial»**.
3. **Alcance del impacto emocional:** La variación emocional proyectada en la vista `DESPUÉS` (de `-2`/`-3` a `+1`/`+2` en confianza y tranquilidad) se declara como **efecto esperado (hipótesis de diseño)** sujeta al protocolo de validación A/B descrito en [`problemas-y-propuestas.md`](./problemas-y-propuestas.md).