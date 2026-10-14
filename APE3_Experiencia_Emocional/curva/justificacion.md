# APE3 — Curva emocional UX (autorreporte parcial + evaluación experta preliminar)

**Responsable:** Eduardo Chicaiza · **Issue:** [#2](https://github.com/Junior-eng-software/ape3-experiencia-emocional/issues/2) · **Fecha de elaboración:** 2026-10-14

> **ESTADO DE EVIDENCIA MIXTO.** **T01–T03** proceden del autorreporte de observaciones individuales del evaluador (registradas el 14 de octubre de 2026; fecha de interacción no especificada). **T04–T08** siguen siendo hipótesis de inspección experta, **no resultados reales**. No hubo participantes externos, medición controlada ni transacción bancaria efectuada. La versión de la app no fue informada.

## 1. Contexto y fuente

- Aplicación de referencia: Banca Móvil Banco Pichincha, Ecuador (Android; **versión instalada no comprobada**).
- Tarea de usuario hipotético: transferir a una cuenta no guardada de otro banco, verificando el beneficiario antes de confirmar.
- Fuente documental consultada el **14 de octubre de 2026**: [guía oficial «¿Cómo transfiero a una cuenta no guardada de otro banco?»](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco).
- Los pasos T02–T08 derivan de la guía. **T01 es contexto de acceso** y no está descrito en esa guía.
- El evaluador indicó tener instalada la app y describió personalmente T01–T03, sin compartir capturas ni datos privados. No declaró haber efectuado ninguna transacción en esta evaluación. No se recogieron respuestas de participantes adicionales.
- **Diferenciar registro de observación de prueba controlada:** las declaraciones corresponden a una experiencia individual no supervisada y no generalizable.

## 2. Escala emocional

| Valor | Interpretación |
|---|---|
| −3 | Muy negativa: frustración o desconfianza intensa |
| −2 | Negativa: preocupación marcada |
| −1 | Algo negativa: duda, cautela o tensión leve |
| 0 | Neutral: atención o concentración sin emoción dominante |
| +1 | Algo positiva: sensación de orientación o comodidad |
| +2 | Positiva: alivio, confianza o tranquilidad |
| +3 | Muy positiva: satisfacción o tranquilidad intensa |

Se asignan enteros entre −3 y +3. **T01–T03 conservan exactamente las emociones y valores declarados por el evaluador**. T04–T08 corresponden a reacciones posibles sin verificar.

## 3. Matriz de resultados y trazabilidad

**Avance:** 3 de 8 momentos con observaciones individuales autorreportadas. T03 es parcial porque no hay información de «Otros Bancos». Los otros cinco son hipótesis aún sin observación.

| ID | Momento | Emoción | Valor | Estado y fundamento |
|---|---|---|---:|---|
| T01 | Acceso / inicio de sesión | Sensación ligeramente positiva | +1 | Observación individual; aclaración de emoción y valoración consistente |
| T02 | Encontrar Transferir dinero | Confianza | +3 | Observación individual; motivo declarado: facilidad de uso |
| T03 | Nuevo contacto (Otros Bancos pendiente) | Confusión | -1 | Observación parcial; expectativa de ubicación distinta |
| T04 | Banco y datos del beneficiario | Inquietud | -1 | Hipótesis; observación pendiente |
| T05 | Validar y revisar beneficiario | Alivio | +2 | Hipótesis; observación pendiente |
| T06 | Monto y cuenta de origen | Concentración | 0 | Hipótesis; observación pendiente |
| T07 | Revisión y confirmación | Tensión | -1 | Hipótesis; observación pendiente |
| T08 | Comprobante de transferencia | Tranquilidad | +2 | Hipótesis; observación pendiente |

El detalle exacto de fuente, tipo de evidencia, justificación y limitaciones se registra en [matriz-emocional.csv](matriz-emocional.csv).

### Análisis de los tres autorreportes

- **T01 (+1, «Sensación ligeramente positiva»):** el evaluador confirmó expresamente que su sensación fue ligeramente positiva (+1); indicó que el inicio de sesión fue sencillo y que le agrada la interfaz inicial. La inconsistencia anterior entre «Neutralidad» y +1 queda aclarada por el propio evaluador.
- **T02 (+3, «Confianza»):** el evaluador respondió «Sí» a si encontró rápidamente la opción de transferir y precisó que su confianza (+3) se debe a la **facilidad de uso**. Es una percepción subjetiva, sin medición de tiempo ni descripción de elementos particulares de la pantalla.
- **T03 (−1, «Confusión»):** no encontró «Nuevo contacto» directamente en el inicio; la opción apareció al ingresar a «Transferir dinero». Interpretación: diferencia entre su expectativa y la estructura de navegación. No constituye automáticamente un error de diseño; es un **punto de fricción emocional observado**. No se ha confirmado la interacción con «Otros Bancos».

## 4. Momentos de verdad (*moments of truth*)

### T05 — Validación del beneficiario (momento de confianza)

**Hecho documentado:** después de usar «Validar», la guía indica que se visualiza el nombre completo del beneficiario y se debe revisar que corresponda a la persona correcta.

**Hipótesis emocional:** reconocer claramente al beneficiario podría disminuir la inquietud generada al introducir datos (T04) y elevar la confianza (**+2 provisional**). Si el nombre no coincide o la retroalimentación es ambigua, podría darse el efecto contrario.

**Verificación pendiente:** inspeccionar qué se muestra realmente, si el resultado es legible y cómo se comunica un error; registrar fecha, versión y evidencia no sensible.

### T07 — Revisión y confirmación (momento de seguridad percibida)

**Hecho documentado:** antes de «Confirmar transferencia» se pide verificar todos los datos.

**Hipótesis emocional:** la relevancia económica de confirmar un importe podría provocar tensión leve (**−1 provisional**) incluso ante un diseño funcional. La presentación clara del banco, beneficiario, cuenta e importe podría reducir esa tensión.

**Verificación pendiente:** observar la pantalla de revisión y comprobar si permite comparar y corregir datos antes de la confirmación. **No pulsar Confirmar** para generar evidencia académica.

### T08 — Comprobante (momento de cierre potencial)

La guía documenta la aparición de un comprobante una vez finalizada la operación y una opción de compartirlo. **+2** es una expectativa de tranquilidad **condicionada** a que una transferencia válida termine correctamente; no se observó un comprobante propio.

## 5. Lectura preliminar de la curva

**Tramo observado por autorreporte:** T01 (+1) → T02 (+3) → T03 (−1). Se aprecia una subida de confianza al encontrar la función y una caída al buscar «Nuevo contacto». La curva **no debe interpretarse como resultado completo** hasta completar T04–T08.

**Tramo aún hipotético:** T04 (−1), T05 (+2), T06 (0), T07 (−1), T08 (+2). Son escenarios de referencia, no emociones declaradas por el evaluador. La visualización diferencia ambos tramos.

**Relación HCI:** T03 puede motivar una inspección de **arquitectura de información y correspondencia entre el sistema y expectativas**. T05 invita a examinar **retroalimentación y visibilidad del estado**, y T07 **prevención de errores y control del usuario**, sin declarar deficiencias antes de observarlas.

## 6. Cómo contrastar la hipótesis sin usar dinero real

1. Inspeccionar material oficial, registrando URL, fecha y correspondencia T-ID. No usar pantallas de terceros sin acreditar.
2. Si hay acceso legítimo, recorrer el flujo sin divulgar credenciales, destinatarios reales, cifras ni datos de cuentas; detenerse **antes** de confirmar la transferencia.
3. Solicitar a una persona voluntaria (si se realiza prueba) que describa emociones y califique cada momento de −3 a +3, con consentimiento. No pedir que transfiera dinero ni que comparta datos bancarios.
4. Registrar por cada momento si la evidencia es documental, observación directa o reporte de participante. Si cambia una puntuación, explicar el cambio en el CSV y regenerar la curva.
5. Documentar la limitación de T08: sin transferencia real solo es posible evaluar el comprobante como elemento descrito por el banco o visualizar material público, **no** afirmar éxito observado.

## 7. Criterios de cierre del issue

- [x] Se definieron T01–T08 y una valoración preliminar **hipotética** por momento.
- [x] Se justificaron T05 y T07 como momentos de verdad **potenciales**.
- [x] Se identificó la procedencia de cada paso y sus limitaciones.
- [x] Registrar autorreportes de observación individual de T01–T03 (no equivalen a prueba controlada).
- [x] Aclarar T01 como sensación ligeramente positiva (+1) y documentar «facilidad de uso» como motivo declarado de T02 (+3).
- [ ] Observar T04–T07 sin confirmar transferencia; T08 solo documentado, si no se ejecuta ninguna.
- [ ] Exportar la curva en `curva-emocional.png` con escala completa.
- [ ] Abrir PR con commits verificables y revisar consistencia con evidencia antes del informe.

**Estado:** evaluación individual parcial (T01–T03) + hipótesis para T04–T08. Pendiente de completar observaciones y de entregar PNG final.
