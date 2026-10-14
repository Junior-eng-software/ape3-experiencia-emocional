# APE3 — Curva emocional UX (evaluación experta preliminar)

**Responsable:** Eduardo Chicaiza · **Issue:** [#2](https://github.com/Junior-eng-software/ape3-experiencia-emocional/issues/2) · **Fecha de elaboración:** 2026-10-14

> **IMPORTANTE — NO ES UNA PRUEBA DE USUARIOS.** Los valores de la matriz son **hipótesis ilustrativas de una inspección experta**, no puntuaciones expresadas por clientes, ni emociones observadas ni resultados estadísticos. Antes de presentarlos como hallazgos deben contrastarse con la interfaz o con pruebas breves correctamente documentadas.

## 1. Contexto y fuente

- Aplicación de referencia: Banca Móvil Banco Pichincha, Ecuador (Android; **versión instalada no comprobada**).
- Tarea de usuario hipotético: transferir a una cuenta no guardada de otro banco, verificando el beneficiario antes de confirmar.
- Fuente documental consultada el **14 de octubre de 2026**: [guía oficial «¿Cómo transfiero a una cuenta no guardada de otro banco?»](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco).
- Los pasos T02–T08 derivan de la guía. **T01 es contexto de acceso** y no está descrito en esa guía.
- No se ha interactuado con una cuenta real, no se ha confirmado una transacción y no se han recogido respuestas de participantes.

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

Se asignan enteros entre −3 y +3. La valoración representa **una reacción posible** de la persona objetivo; no prueba que ocurra.

## 3. Matriz preliminar y trazabilidad

| ID | Momento | Emoción posible | Valor hipotético | Interpretación y evidencia |
|---|---|---|---:|---|
| T01 | Acceso / inicio de sesión | Neutralidad | 0 | Sin observar el acceso no es justificable atribuir satisfacción ni frustración. |
| T02 | Encontrar Transferir dinero | Orientación | +1 | Como hipótesis, disponer de dos vías documentadas puede facilitar encontrar la operación. |
| T03 | Nuevo contacto y Otros Bancos | Atención | 0 | La selección de dos opciones puede exigir atención sin implicar emoción negativa. |
| T04 | Banco y datos del beneficiario | Inquietud | -1 | Posible precaución por el riesgo de escribir datos erróneos al mover dinero. |
| T05 | Validar y revisar beneficiario | Alivio | +2 | La posibilidad documentada de comprobar la identidad podría reforzar la confianza. |
| T06 | Monto y cuenta de origen | Concentración | 0 | El usuario debe contrastar el importe y origen, sin evidencia suficiente para asignar emoción positiva o negativa. |
| T07 | Revisión y confirmación | Tensión | -1 | La confirmación de una operación financiera puede generar incertidumbre anticipatoria incluso si el flujo funciona. |
| T08 | Comprobante de transferencia | Tranquilidad | +2 | Si la transferencia concluye correctamente, un comprobante visible podría aportar cierre y certeza. |

El detalle completo, la referencia por momento y sus limitaciones están en [matriz-emocional.csv](matriz-emocional.csv). La curva prevista deberá representar estos ocho valores en el mismo orden, con eje X T01–T08, eje Y de −3 a +3 y línea neutra en 0.

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

En el escenario hipotético, la mayor caída se ubicaría en T04 (introducir datos: −1) y T07 (confirmar: −1), y las recuperaciones en T05 (beneficiario verificado: +2) y T08 (comprobante: +2). **No afirmar que la aplicación presenta un defecto por esas oscilaciones**: pueden obedecer también a la responsabilidad propia de una transferencia bancaria.

**Conexión con HCI:** T05 invita a examinar **retroalimentación y visibilidad del estado**; T07, **prevención de errores y control del usuario**. Esto sirve de insumo independiente para contrastar luego las propuestas del integrante C, sin suponer que ya están justificadas.

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
- [ ] Incorporar observaciones verificadas de la interfaz o pruebas breves, si están disponibles.
- [ ] Exportar la curva en `curva-emocional.png` con escala completa.
- [ ] Abrir PR con commits verificables y revisar consistencia con evidencia antes del informe.

**Estado:** borrador de evaluación experta, pendiente de validación y de gráfica final.
