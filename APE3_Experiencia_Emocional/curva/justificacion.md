# APE3 — Evaluación emocional individual: Banca Móvil Banco Pichincha

**Responsable:** Eduardo Chicaiza · **Issue:** [#2](https://github.com/Junior-eng-software/ape3-experiencia-emocional/issues/2) · **Fecha de registro:** 14/10/2026

> **Método y límites:** ocho autorreportes de un único evaluador; no equivalen a pruebas con ocho participantes ni a una medición objetiva. Las valoraciones se transcriben sin corregirlas. No se aportaron capturas, fecha exacta de interacción o versión de app. No se ha confirmado una transferencia nueva durante la evaluación. La observación de T08 corresponde expresamente a un comprobante de una transferencia anterior.

## Contexto
- **Flujo:** transferencia a beneficiario nuevo de otro banco, aplicación Android de Banco Pichincha.
- **Fuente documental que define los pasos:** [Guía oficial de transferencia interbancaria a cuenta nueva](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco). Esta fuente no prueba las emociones del evaluador.
- **Escala:** −3 muy negativa; −2 negativa; −1 ligeramente negativa; 0 neutral; +1 ligeramente positiva; +2 positiva; +3 muy positiva.

## Matriz de valoraciones personales
| ID | Momento | Emoción declarada | Valor | Estado |
|---|---|---|---:|---|
| T01 | Acceso / inicio de sesión | Sensación ligeramente positiva | +1 | Observado (aclaración registrada) |
| T02 | Encontrar Transferir dinero | Confianza | +3 | Observado (justificación aclarada) |
| T03 | Nuevo contacto y Otros Bancos | Confusión | -1 | Observado parcialmente |
| T04 | Banco y datos del beneficiario | Sensación positiva | +2 | Emoción aclarada; detalle de campos del beneficiario no especificado |
| T05 | Validar y revisar beneficiario | Satisfacción | +3 | Valoración de datos propios; validación del beneficiario NO observada |
| T06 | Monto y cuenta de origen | Concentración | +1 | Registrado; anulación no verificada |
| T07 | Revisión y confirmación | Tranquilidad | +2 | Emoción aclarada; envío de transferencia no confirmado |
| T08 | Comprobante de transferencia | Satisfacción | +1 | Observación retrospectiva: comprobante de transferencia anterior |

El [CSV](matriz-emocional.csv) contiene las observaciones literales resumidas, fuentes, justificaciones y limitaciones. El hecho de puntuar un touchpoint no garantiza que todos sus subpasos hayan sido verificados.

## Análisis de los momentos
- **T01 (+1):** ingreso sencillo; sensación ligeramente positiva y agrado por la interfaz inicial (aclaración proporcionada por el propio evaluador).
- **T02 (+3):** confianza elevada por la *facilidad de uso* para acceder a transferencias, sin tiempo medido.
- **T03 (−1):** confusión leve al buscar «Nuevo contacto» en inicio, cuando aparece después de elegir «Transferir dinero». «Otros Bancos» no fue evaluado específicamente.
- **T04 (+2):** aclaró que experimentó una **sensación positiva**, coherente con +2, por la facilidad para navegar y acceder a sus datos. No se detallaron los campos específicos del beneficiario; no debe inventarse su contenido.
- **T05 (+3):** confirmó que verificó **sus propios datos bancarios**, lo que le generó satisfacción y tranquilidad. Esta valoración describe su experiencia real con la información propia, pero **NO es evidencia del touchpoint T05 definido como validación del beneficiario**. Queda pendiente la observación de ese subpaso.
- **T06 (+1):** concentración y facilidad para escribir el monto; según su observación acepta números y punto decimal (no coma). Percibe que no hay anulación posterior al envío y reconoce confirmaciones anteriores. **No está verificado** si existen anulaciones o reversos por otros canales.
- **T07 (+2):** aclaró que predominó la **tranquilidad**, coherente con +2, después de concentración inicial y ligera preocupación. No ha indicado si pulsó Confirmar durante la evaluación; no se afirma envío exitoso.
- **T08 (+1):** reporta satisfacción leve por la claridad visual de un **comprobante de transferencia anterior**. Se registra como observación retrospectiva; no constituye evidencia del resultado de una transferencia nueva durante esta evaluación.

## Momentos de verdad (con alcance explícito)
### T05 — Validación del beneficiario: momento de verdad previsto, aún no observado
En la guía oficial, este paso presenta el nombre del destinatario para que el usuario lo compruebe; por eso **podría** afectar la confianza y es un momento de verdad **hipotético**. Sin embargo, el evaluador aclaró que la satisfacción +3 se refería a **sus propios datos**, no al destinatario. Esa observación no puede usarse como prueba del impacto emocional de validar al beneficiario. **Principio HCI pendiente de evaluar:** visibilidad del estado y retroalimentación.

### T07 — Revisión y confirmación
El paso implica riesgo percibido por una operación económica y una transición de concentración a **tranquilidad (+2)**, tal como aclaró el evaluador. **Principio HCI:** prevención de errores y control del usuario. No se ha corroborado la ejecución de una transferencia durante esta evaluación.

### T08 — Estado/comprobante
La presentación de un comprobante **de una transferencia anterior** produce satisfacción leve (+1). **Principio HCI:** visibilidad del resultado. Este dato permite discutir cómo se comunica el cierre de operaciones bancarias, pero no demuestra el cierre de la transferencia nueva del flujo de estudio.

## Lectura de la curva
Valores originales: **T01 +1 → T02 +3 → T03 −1 → T04 +2 → T05 +3 → T06 +1 → T07 +2 → T08 +1**.

T03 es el punto de mayor fricción emocional declarado. Los máximos T02 y T05 reflejan facilidad de uso y satisfacción al comprobar **datos propios**, respectivamente. Las discrepancias de T04 y T07 fueron **aclaradas por el evaluador**; la curva mantiene sus valores originales. T05 (propios) y T08 (comprobante anterior) se marcan como observaciones reales, pero **no corresponden exactamente a esos pasos del flujo actual**.

## Pendientes para el cierre
- [x] Ocho momentos con autorreportes individuales.
- [x] Matriz emocional con estado y limitaciones.
- [x] Dos momentos de verdad fundamentados provisionalmente.
- [x] Gráfica SVG con escala −3 a +3.
- [x] Aclarar T04 como sensación positiva (+2).
- [x] Aclarar T07 como tranquilidad (+2).
- [x] Precisar T05: datos **propios**, no del beneficiario.
- [ ] Observar la validación real del beneficiario (T05 del flujo), si es posible hacerlo sin exposición de datos privados.
- [x] Precisar T08: comprobante de **transferencia anterior**.
- [ ] Registrar explícitamente que el comprobante del flujo actual no se observó.
- [ ] Confirmar fecha de observación y versión de la app, si están disponibles.
- [ ] Publicar PNG final y preparar PR tras verificación.

**Precaución:** no publicar credenciales, comprobantes privados ni datos bancarios identificables, y no efectuar transferencias para generar evidencias.
