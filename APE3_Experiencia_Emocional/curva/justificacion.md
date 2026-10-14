# APE3 — Evaluación emocional individual: Banca Móvil Banco Pichincha

**Responsable:** Eduardo Chicaiza · **Issue:** [#2](https://github.com/Junior-eng-software/ape3-experiencia-emocional/issues/2) · **Fecha de registro:** 14/10/2026

> **Método y límites:** ocho autorreportes de un único evaluador; no equivalen a pruebas con ocho participantes ni a una medición objetiva. Las valoraciones se transcriben sin corregirlas. No se aportaron capturas, fecha exacta de interacción o versión de app. No hay confirmación de que se ejecutara una transferencia real durante la evaluación.

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
| T04 | Banco y datos del beneficiario | Neutro | +2 | Registrado; discrepancia emocional y objeto de datos pendientes |
| T05 | Validar y revisar beneficiario | Satisfacción | +3 | Registrado; referente de validación pendiente |
| T06 | Monto y cuenta de origen | Concentración | +1 | Registrado; anulación no verificada |
| T07 | Revisión y confirmación | Neutralidad | +2 | Registrado; discrepancia y ejecución por aclarar |
| T08 | Comprobante de transferencia | Satisfacción | +1 | Registrado; origen de comprobante por aclarar |

El [CSV](matriz-emocional.csv) contiene las observaciones literales resumidas, fuentes, justificaciones y limitaciones. El hecho de puntuar un touchpoint no garantiza que todos sus subpasos hayan sido verificados.

## Análisis de los momentos
- **T01 (+1):** ingreso sencillo; sensación ligeramente positiva y agrado por la interfaz inicial (aclaración proporcionada por el propio evaluador).
- **T02 (+3):** confianza elevada por la *facilidad de uso* para acceder a transferencias, sin tiempo medido.
- **T03 (−1):** confusión leve al buscar «Nuevo contacto» en inicio, cuando aparece después de elegir «Transferir dinero». «Otros Bancos» no fue evaluado específicamente.
- **T04 (+2):** describe facilidad para navegar y acceder a «mis datos», pero selecciona «Neutro» con +2. **Se conserva esta discrepancia**: falta precisar el objeto exacto de la pantalla.
- **T05 (+3):** expresa satisfacción y tranquilidad al verificar «mis datos». **No afirmar** que verificó los datos de un beneficiario hasta que especifique cuáles eran.
- **T06 (+1):** concentración y facilidad para escribir el monto; según su observación acepta números y punto decimal (no coma). Percibe que no hay anulación posterior al envío y reconoce confirmaciones anteriores. **No está verificado** si existen anulaciones o reversos por otros canales.
- **T07 (+2):** ligera preocupación, concentración al principio y tranquilidad después. Selecciona «Neutralidad» con +2; **segunda discrepancia** entre etiqueta y escala. No se sabe si pulsó Confirmar.
- **T08 (+1):** satisfacción por entender visualmente que la transferencia fue enviada. **Origen del comprobante por aclarar** (operación actual, anterior u otra referencia); no atribuir envío realizado en la evaluación sin confirmación.

## Momentos de verdad (provisionales)
### T05 — Verificación y confianza
La satisfacción reportada (+3) sugiere que comprobar datos produce tranquilidad. **Principio HCI:** visibilidad del estado y retroalimentación. En la guía, la validación permite revisar el nombre del beneficiario; en el autorreporte se habla de «mis datos», por lo que queda por confirmar su correspondencia con ese paso. No se infiere éxito técnico del proceso de validación.

### T07 — Revisión y confirmación
El paso implica riesgo percibido por una operación económica y una transición de concentración a tranquilidad. **Principio HCI:** prevención de errores y control del usuario. El +2 y «Neutralidad» quedan registrados sin alteración. No se ha corroborado ejecución de transferencia.

### T08 — Estado/comprobante
La presentación del estado produce satisfacción leve (+1). **Principio HCI:** visibilidad del resultado. Su origen y vínculo con una transferencia actual siguen por precisar.

## Lectura de la curva
Valores originales: **T01 +1 → T02 +3 → T03 −1 → T04 +2 → T05 +3 → T06 +1 → T07 +2 → T08 +1**.

T03 es el punto de mayor fricción emocional declarado. Los máximos T02 y T05 reflejan facilidad de uso y tranquilidad por verificación. T04 y T07 se marcan como **etiquetas emocionales por aclarar**, pero sus puntuaciones se trazan tal cual.

## Pendientes para el cierre
- [x] Ocho momentos con autorreportes individuales.
- [x] Matriz emocional con estado y limitaciones.
- [x] Dos momentos de verdad fundamentados provisionalmente.
- [x] Gráfica SVG con escala −3 a +3.
- [ ] Aclarar si en T04 +2 equivale a emoción positiva o mantener «Neutro».
- [ ] Aclarar si en T07 +2 expresa tranquilidad o mantener «Neutralidad».
- [ ] Precisar cuáles datos revisó en T05.
- [ ] Precisar qué comprobante visualizó en T08 y si la operación fue previa, actual o de otro tipo.
- [ ] Confirmar fecha de observación y versión de la app, si están disponibles.
- [ ] Publicar PNG final y preparar PR tras verificación.

**Precaución:** no publicar credenciales, comprobantes privados ni datos bancarios identificables, y no efectuar transferencias para generar evidencias.
