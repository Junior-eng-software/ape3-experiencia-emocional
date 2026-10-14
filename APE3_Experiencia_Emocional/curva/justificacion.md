# APE3 — Evaluación emocional individual: Banca Móvil Banco Pichincha

**Responsable:** Eduardo Chicaiza · **Issue:** [#2](https://github.com/Junior-eng-software/ape3-experiencia-emocional/issues/2) · **Fecha de registro:** 14/10/2026

> **Método y límites:** ocho autorreportes de un único evaluador; no equivalen a pruebas con ocho participantes ni a una medición objetiva. Las valoraciones se transcriben sin corregirlas. No se aportaron capturas, fecha exacta de interacción o versión de app. El evaluador aclaró posteriormente que T08 corresponde al comprobante de una **transferencia actual realizada durante la evaluación**. Esto es un **autorreporte**, sin comprobante adjunto ni verificación independiente de la operación.

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
| T05 | Validar y revisar beneficiario | Satisfacción | +3 | Autorreporte: verificó datos propios y del beneficiario; sin evidencia visual adjunta |
| T06 | Monto y cuenta de origen | Concentración | +1 | Registrado; anulación no verificada |
| T07 | Revisión y confirmación | Tranquilidad | +2 | Emoción aclarada; comprobante actual declarado posteriormente en T08 |
| T08 | Comprobante de transferencia | Satisfacción | +1 | Autorreporte: comprobante de transferencia actual, sin verificación externa |

El [CSV](matriz-emocional.csv) contiene las observaciones literales resumidas, fuentes, justificaciones y limitaciones. El hecho de puntuar un touchpoint no garantiza que todos sus subpasos hayan sido verificados.

## Análisis de los momentos
- **T01 (+1):** ingreso sencillo; sensación ligeramente positiva y agrado por la interfaz inicial (aclaración proporcionada por el propio evaluador).
- **T02 (+3):** confianza elevada por la *facilidad de uso* para acceder a transferencias, sin tiempo medido.
- **T03 (−1):** confusión leve al buscar «Nuevo contacto» en inicio, cuando aparece después de elegir «Transferir dinero». «Otros Bancos» no fue evaluado específicamente.
- **T04 (+2):** aclaró que experimentó una **sensación positiva**, coherente con +2, por la facilidad para navegar y acceder a sus datos. No se detallaron los campos específicos del beneficiario; no debe inventarse su contenido.
- **T05 (+3):** mediante una nueva aclaración, afirmó que verificó **tanto sus propios datos como los del beneficiario**, y que experimentó satisfacción y tranquilidad. Su explicación anterior se limitaba a datos propios. Se trata de una observación individual **declarada por el evaluador**, sin captura ni comprobación independiente del funcionamiento de la validación.
- **T06 (+1):** concentración y facilidad para escribir el monto; según su observación acepta números y punto decimal (no coma). Percibe que no hay anulación posterior al envío y reconoce confirmaciones anteriores. **No está verificado** si existen anulaciones o reversos por otros canales.
- **T07 (+2):** aclaró que predominó la **tranquilidad**, coherente con +2, después de concentración inicial y ligera preocupación. No describió si pulsó específicamente «Confirmar»; posteriormente aclaró que el comprobante de T08 correspondía a la transferencia actual. **No se dispone de evidencia técnica independiente** del envío.
- **T08 (+1):** corrigió su respuesta anterior e indicó que el comprobante provenía de una **transferencia actual realizada durante la evaluación**. Declaró satisfacción leve por su claridad visual. **Procedencia:** autorreporte; no se adjuntó captura ni prueba independiente. No se publicarán datos bancarios.

## Momentos de verdad (con alcance explícito)
### T05 — Validación de datos y confianza
En la guía oficial, la validación permite revisar la información del beneficiario antes de transferir. El evaluador aclaró finalmente que revisó **datos propios y del beneficiario**, y reportó satisfacción (+3) y tranquilidad. Se interpreta como **momento de verdad observado por autorreporte individual**, no como prueba técnica del funcionamiento del banco ni como resultado de participantes independientes. **Principio HCI:** visibilidad del estado y retroalimentación.

### T07 — Revisión y confirmación
El paso implica riesgo percibido por una operación económica y una transición de concentración a **tranquilidad (+2)**, tal como aclaró el evaluador. **Principio HCI:** prevención de errores y control del usuario. El evaluador después indicó que visualizó un comprobante de la transferencia actual; ese hecho es autorreportado, sin corroboración técnica externa.

### T08 — Estado/comprobante
La presentación de un comprobante **de la transferencia actual, según nueva aclaración del evaluador**, produce satisfacción leve (+1). **Principio HCI:** visibilidad del resultado. El reporte permite discutir la claridad del cierre, pero no se dispone de comprobante adjunto ni de validación independiente.

## Lectura de la curva
Valores originales: **T01 +1 → T02 +3 → T03 −1 → T04 +2 → T05 +3 → T06 +1 → T07 +2 → T08 +1**.

T03 es el punto de mayor fricción emocional declarado. Los máximos T02 y T05 reflejan facilidad de uso y satisfacción al comprobar **datos propios y del beneficiario**, respectivamente. T04 y T07 se aclararon y las puntuaciones originales permanecen intactas. T05 y T08 se reportan como parte del flujo actual, **según la última aclaración del evaluador**; no se han corroborado con capturas ni registros técnicos.

## Pendientes para el cierre
- [x] Ocho momentos con autorreportes individuales.
- [x] Matriz emocional con estado y limitaciones.
- [x] Dos momentos de verdad fundamentados provisionalmente.
- [x] Gráfica SVG con escala −3 a +3.
- [x] Aclarar T04 como sensación positiva (+2).
- [x] Aclarar T07 como tranquilidad (+2).
- [x] Precisar T05: el evaluador declara haber verificado datos **propios y del beneficiario**.
- [ ] Complementar con evidencia no sensible de los componentes visuales de validación, si está disponible.
- [x] Precisar T08: el evaluador declara haber visto un comprobante de la **transferencia actual**, corrigiendo la aclaración anterior.
- [ ] Anotar si existe alguna evidencia visual no sensible o documentar únicamente el autorreporte.
- [ ] Confirmar fecha de observación y versión de la app, si están disponibles.
- [ ] Publicar PNG final y preparar PR tras verificación.

**Precaución:** no publicar credenciales, comprobantes privados ni datos bancarios identificables, y no efectuar transferencias para generar evidencias.

## Historial de aclaraciones (trazabilidad)

**14/10/2026 — Corrección de respuestas declaradas por el evaluador:**
- **T04:** sensación positiva (+2), sin modificación de la puntuación.
- **T05:** la aclaración anterior indicaba «propios»; la nueva declaración indica «**ambos: datos propios y del beneficiario**». Se usa la última respuesta, conservando aquí el antecedente.
- **T07:** tranquilidad (+2), sin modificación de la puntuación.
- **T08:** la aclaración anterior indicaba «anterior»; la nueva declaración indica «**actual: comprobante de la transferencia de esta evaluación**». Se usa la última respuesta, conservando aquí el antecedente.

La fuente de todas estas precisiones es **el relato del evaluador en la conversación**, no una captura de pantalla, una auditoría de la app ni una prueba con usuarios externos. Las puntuaciones T01–T08 no cambiaron.
