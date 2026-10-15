# Análisis del usuario, usabilidad y experiencia de usuario

**Responsable:** Juan Carvajal ([@juanjose1234456787654](https://github.com/juanjose1234456787654)) · **Issue:** #1 [APE3][A] · **Rama:** `ape3/analisis-ux`
**Aplicación:** Banca Móvil Banco Pichincha (Ecuador), referencia Android · **Flujo:** transferencia interbancaria a un beneficiario nuevo (T01–T08)
**Fecha de elaboración:** 15 de octubre de 2026

> **Naturaleza del documento.** Es un análisis académico independiente, no afiliado a Banco Pichincha. Se basa en documentación oficial y en evaluación experta. **No contiene entrevistas, pruebas con personas, métricas ni datos bancarios.** Todo lo que no se observó se declara como supuesto.

## 0. Cómo se etiqueta la evidencia

Cada afirmación lleva una de estas etiquetas (según `alcance-comun.md`):

| Etiqueta | Significado |
|---|---|
| **[HD] Hecho documentado** | Sale de la ayuda oficial del banco o de un marco teórico citado. |
| **[OBS] Observación directa** | Alguien inspeccionó la app y lo registró. En este documento no hay observaciones propias (ver sección 7). |
| **[SUP] Supuesto / evaluación experta** | Inferencia razonada, sin atribuirla a usuarios reales. |

---

## 1. Usuario objetivo

### 1.1 Persona hipotética

| Elemento | Descripción |
|---|---|
| **Tipo** | Perfil de referencia **hipotético** [SUP]. No es un participante, una entrevista ni una muestra representativa. |
| **Edad** | 18 a 30 años. |
| **Contexto** | Estudiante o joven trabajador, residente en Ecuador. |
| **Dispositivo** | Smartphone Android. |
| **Habilidades digitales** | Intermedias: usa apps bancarias y de mensajería con soltura. |
| **Experiencia relevante** | Poca práctica transfiriendo a destinatarios nuevos de otro banco. |

### 1.2 Escenario

Necesita enviar dinero a una persona cuya cuenta de otro banco todavía no tiene guardada. Quiere verificar al destinatario y entender cuál fue el resultado final de la operación.

### 1.3 Meta

Enviar dinero a una cuenta de otro banco **sin equivocarse de destinatario** y **comprobar que la operación terminó**.

### 1.4 Expectativas (todas [SUP])

| N.º | Expectativa | Touchpoints |
|---|---|---|
| E1 | Encontrar rápido dónde se inicia una transferencia y cómo agregar un contacto nuevo de otro banco. | T02, T03 |
| E2 | Entender qué datos se piden del beneficiario y para qué sirve cada campo. | T04 |
| E3 | Reconocer al beneficiario antes de enviar (que la app le ayude a confirmar que es la persona correcta). | T05 |
| E4 | Revisar banco, importe y cuenta de origen en un solo lugar antes de confirmar, y poder corregir si algo está mal. | T06, T07 |
| E5 | Distinguir sin dudar cuál fue el resultado (hecho o no) y conservar un comprobante. | T08 |

---

## 2. Usabilidad y experiencia de usuario: diferencia aplicada al flujo

**Marco teórico [HD]:** la usabilidad se define como el grado en que un producto permite lograr objetivos con **eficacia, eficiencia y satisfacción** en un contexto de uso (ISO 9241-11). La experiencia de usuario abarca las **percepciones y respuestas** de la persona antes, durante y después del uso (ISO 9241-210). La distinción entre cualidades **pragmáticas** (utilidad y facilidad para la tarea) y **hedónicas** (sensaciones, estímulo, valor emocional) proviene de Hassenzahl. *(Confirmar la redacción exacta con el material de clase; ver F6.)*

| Aspecto | Usabilidad (¿se pudo hacer bien?) | Experiencia de usuario (¿cómo se vivió?) |
|---|---|---|
| **Pregunta central** | ¿La persona logra transferir sin errores y sin esfuerzo innecesario? | ¿Qué siente y piensa mientras lo hace: confianza, tranquilidad, duda, frustración? |
| **Qué mide** | Eficacia (completar la transferencia), eficiencia (pasos y tiempo), facilidad (aprender y entender). | Percepciones, confianza, tranquilidad y frustración antes, durante y después. |
| **Ejemplo en T03** | Encontrar «Nuevo contacto» y «Otros bancos» en pocos pasos y sin equivocarse de ruta. | La sensación de «voy bien» o de «¿estaré en el lugar correcto?» al elegir esas opciones. |
| **Ejemplo en T05** | Que el sistema muestre un dato del beneficiario para validarlo (un hecho funcional). | La **confianza** de que el destinatario es quien se espera; alivio si coincide, alarma si no. |
| **Ejemplo en T07** | Que la pantalla de revisión liste banco, importe y cuenta de origen (eficacia de la revisión). | La **tranquilidad** o ansiedad al pulsar «Confirmar» una operación económica que no se puede deshacer a la ligera. |
| **Ejemplo en T08** | Que exista un comprobante (resultado verificable). | La **satisfacción** y la certeza de que la operación terminó; la duda si el estado final es ambiguo. |
| **Cómo se evidencia** | Observación de tareas: éxito/fracaso, tiempo, errores, pasos. | Preguntas sobre emoción y confianza, expresiones, valoraciones; **requiere personas reales**. |

**Idea clave:** una pantalla puede ser *usable* (la persona completa la tarea) y aun así dejar una *mala experiencia* (la persona termina con dudas sobre si envió al destinatario correcto). Por eso T05, T07 y T08 se tratan como los momentos donde ambas dimensiones se separan con mayor claridad. En este documento esa separación se plantea como **hipótesis**, no como resultado.

---

## 3. Cualidades evaluadas

Dos **pragmáticas** y dos **hedónicas**, como dimensiones a examinar y **no** como fortalezas demostradas.

| Tipo | Cualidad | Touchpoints vinculados |
|---|---|---|
| Pragmática | **P1. Claridad de navegación** | T02, T03, T04 |
| Pragmática | **P2. Prevención y recuperación de errores** | T04, T05, T07 |
| Hedónica | **H1. Confianza percibida** | T01, T05, T07 |
| Hedónica | **H2. Tranquilidad y satisfacción** | T07, T08 |

### 3.1 Tabla de cualidades

| Cualidad | T-ID | Evidencia | Interpretación | Limitación |
|---|---|---|---|---|
| **P1. Claridad de navegación** | T02 | **[HD]** La guía oficial (F1) describe «Transferir dinero» como inicio del flujo. | **[SUP]** Si la opción es visible desde el inicio, la persona de referencia debería localizarla con poco esfuerzo (E1). | No hay observación propia de la pantalla; no se conoce la versión de la app. |
| | T03 | **[HD]** F1 indica elegir «Nuevo contacto» y luego «Otros bancos». | **[SUP]** Que sean dos decisiones seguidas puede generar duda a quien nunca transfirió a un contacto nuevo (E1). | La guía no prueba dónde busca primero una persona real. No se afirma que haya confusión. |
| | T04 | **[HD]** F1 indica seleccionar el banco de destino e ingresar los datos del beneficiario. | **[SUP]** Si los campos son claros, el recorrido es continuo; si no, la navegación se interrumpe (E2). | No se verificó qué campos exactos ni con qué etiquetas aparecen. |
| **P2. Prevención y recuperación de errores** | T04 | **[HD]** F1 incluye ingresar datos del beneficiario antes de validar. | **[SUP]** Un dato mal digitado es el error más probable de este tramo; conviene que se detecte pronto (E2). | No se probó qué mensajes o bloqueos existen ante un dato inválido. |
| | T05 | **[HD]** F1 indica validar y revisar la identidad del beneficiario antes de seguir. | **[SUP]** La validación funciona como **prevención**: permite detectar un destinatario equivocado antes de enviar (E3). | No se verificó qué dato se muestra ni cómo se corrige si no coincide. |
| | T07 | **[HD]** F1 incluye una revisión antes de confirmar. | **[SUP]** La pantalla de revisión es el último filtro de prevención de errores (E4). | No se verificó si se puede volver atrás para corregir ni si se puede anular lo enviado. |
| **H1. Confianza percibida** | T01 | **[HD]** La página oficial de Banca Móvil (F2) presenta la app como canal bancario. | **[SUP]** Un acceso que se percibe seguro es la base de la confianza del resto del flujo. | F2 es marketing general y no describe el inicio de sesión en detalle. |
| | T05 | **[HD]** F1 incluye la validación del beneficiario. | **[SUP]** Ver al destinatario confirmado puede **subir** la confianza; si no se presenta, puede subir la incertidumbre (E3). | La confianza es subjetiva y no se midió en nadie. |
| | T07 | **[HD]** F1 incluye revisión y confirmación. | **[SUP]** Revisar importe, banco y origen antes de confirmar refuerza la sensación de control (E4). | No se sabe qué datos exactos muestra la pantalla en la versión actual. |
| **H2. Tranquilidad y satisfacción** | T07 | **[HD]** F1 incluye confirmación explícita. | **[SUP]** Tras pulsar «Confirmar» la persona pasa de la duda a la espera del resultado; una respuesta clara ayuda a su tranquilidad. | No se observó la respuesta de la app tras confirmar. |
| | T08 | **[HD]** F1 indica que el flujo termina con un comprobante. | **[SUP]** Un comprobante claro cierra el flujo con certeza (E5); uno ambiguo dejaría incertidumbre. | El comprobante no se evalúa visualmente aquí; no se generó ni se muestra ninguno. |

---

## 4. Análisis de expectativas en T05 y T07

No se afirman resultados: se compara lo que **la persona de referencia esperaría** con lo que **la documentación oficial indica** y con lo que **falta por confirmar**.

### 4.1 T05: validar y revisar al beneficiario

| Expectativa [SUP] | Lo que indica la fuente [HD] | Qué falta confirmar | Riesgo si no se cumple [SUP] |
|---|---|---|---|
| Ver un dato que le permita reconocer a la persona que recibirá el dinero (E3). | F1 contempla validar y revisar la identidad del beneficiario. | Qué dato se muestra exactamente y en qué formato. | Duda sobre si el destinatario es el correcto. Menor confianza. |
| Poder corregir si el dato no coincide (E3, E4). | F1 no detalla la corrección en lo consultado. | Si existe un camino claro para volver y modificar. | Frustración o abandono si se debe reiniciar el flujo. |
| Entender qué significa el resultado de la validación. | F1 la presenta como paso del proceso. | Si el mensaje es comprensible para una persona con poca experiencia. | Se valida «a ciegas» y se pierde el valor preventivo del paso. |

### 4.2 T07: revisar datos y confirmar

| Expectativa [SUP] | Lo que indica la fuente [HD] | Qué falta confirmar | Riesgo si no se cumple [SUP] |
|---|---|---|---|
| Ver en una sola pantalla banco, cuenta de origen, importe y beneficiario (E4). | F1 incluye revisar antes de confirmar. | Qué datos se listan y con qué jerarquía visual. | Se confirma sin revisar bien. Mayor probabilidad de error. |
| Saber que «Confirmar» es el punto de compromiso. | F1 incluye confirmación explícita. | Cómo se diferencia visualmente el botón de confirmar del de cancelar o volver. | Pulsar por inercia o dudar por falta de claridad. |
| Poder retroceder para corregir antes de confirmar (E4). | No detallado en lo consultado. | Si existe «Volver» o «Editar» y conserva lo ya escrito. | Ansiedad y sensación de falta de control. |

> **Límite:** T07 se analiza solo hasta antes de confirmar. No se realizaron transferencias reales (`alcance-comun.md`, sección 2).

---

## 5. Distinción entre hechos oficiales, observaciones y supuestos

### 5.1 Hechos oficiales [HD]

| N.º | Hecho | Fuente |
|---|---|---|
| H-1 | El banco publica una guía para transferir a una cuenta no guardada de otro banco, que va desde «Transferir dinero» hasta un comprobante final. | F1 |
| H-2 | El recorrido documentado incluye elegir «Nuevo contacto» y «Otros bancos», seleccionar el banco de destino e ingresar datos del beneficiario. | F1 |
| H-3 | El recorrido documentado incluye validar/revisar al beneficiario, ingresar el importe, revisar antes de confirmar y visualizar un comprobante. | F1 |
| H-4 | Banco Pichincha ofrece Banca Móvil como canal digital. | F2 |
| H-5 | Definiciones de usabilidad, UX y cualidades pragmáticas/hedónicas. | F4, F5 (marco teórico) |

### 5.2 Observaciones [OBS]

| N.º | Observación | Fuente |
|---|---|---|
| — | **Ninguna.** Este documento no incluye inspección directa de la app ni pruebas con personas. | — |

### 5.3 Supuestos [SUP]

| N.º | Supuesto |
|---|---|
| S-1 | La persona de referencia (18–30 años, Android, Ecuador, habilidades intermedias) existe como perfil de estudio, no como persona real. |
| S-2 | Una persona con poca experiencia transfiriendo a contactos nuevos duda más en T03, T05 y T07. |
| S-3 | La validación del beneficiario (T05) y la revisión (T07) son los momentos de mayor impacto en confianza y tranquilidad. |
| S-4 | Un comprobante claro (T08) refuerza la satisfacción; uno ambiguo la reduce. |
| S-5 | Las expectativas E1 a E5 son razonables para el perfil, pero no se validaron con personas. |

---

## 6. Limitaciones

1. **No hay datos de usuarios.** La persona, las expectativas y las interpretaciones son hipótesis de evaluación experta.
2. **Dependencia de la guía oficial.** Las pantallas pueden cambiar con cada versión de la app; no se verificó la versión instalada ni se mezcló documentación con observaciones de versiones distintas.
3. **Sin observación propia.** No se inspeccionó la app en este documento, por lo que no se afirma nada sobre mensajes de error, textos exactos ni tiempos.
4. **T07 y T08.** Por seguridad no se realizaron transferencias. T07 se analiza antes de confirmar y T08 solo con la descripción pública del comprobante.
5. **Subjetividad.** Confianza, tranquilidad y satisfacción son emociones; sin personas reales no se pueden cuantificar.
6. **Alcance.** No se edita la curva emocional, el prototipo ni el informe de otros integrantes.

---

## 7. Observación directa (opcional, a completar solo si se realizó)

> Si el responsable inspecciona la app hasta **antes de confirmar**, registrar aquí fecha, versión, pantalla y notas **sin datos personales**, etiquetadas **[OBS]**. Si no se hizo, este apartado permanece vacío y no se infieren resultados.

| Fecha | Versión de la app | Touchpoint | Nota anonimizada |
|---|---|---|---|
| | | | |

---

## 8. Fuentes

| Código | Fuente | Tipo | Fecha de consulta |
|---|---|---|---|
| F1 | [Guía oficial: ¿Cómo transfiero a una cuenta no guardada de otro banco?](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco), Centro de Ayuda Banco Pichincha | Hecho documentado | 15/10/2026 |
| F2 | [Banca Móvil Banco Pichincha](https://www.pichincha.com/banca-movil) | Hecho documentado | 15/10/2026 |
| F3 | `APE3_Experiencia_Emocional/alcance-comun.md` (definición del grupo, 13/10/2026) | Alcance del trabajo | 15/10/2026 |
| F4 | ISO 9241-11:2018, *Ergonomics of human-system interaction: Usability: Definitions and concepts* | Marco teórico | Por confirmar |
| F5 | ISO 9241-210:2019, *Human-centred design for interactive systems*; Hassenzahl, M. (2003), «The thing and I: understanding the relationship between user and product» | Marco teórico | Por confirmar |
| F6 | Material del curso de Interacción Humano–Computador, tema «Emoción y experiencia de usuario» | Marco teórico | Por confirmar |