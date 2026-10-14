# Protocolo de evidencia, validación y fuentes

**Responsable:** Mauricio Guevara, GitHub @Mauri10G. **Issue:** #4. **Rama:** `ape3/evidencias-informe`.
**App:** Banca Móvil Banco Pichincha, Android. **Flujo:** transferencia interbancaria a un beneficiario nuevo.

> Este documento es un plan. Todavía no contiene resultados de pruebas con personas ni métricas. Todo lo que no se probó se declara como hipótesis o evaluación experta.

## 1. Inventario de fuentes

| Código | Fuente | Tipo de evidencia | Fecha de consulta | Se relaciona con |
|---|---|---|---|---|
| F1 | [Guía oficial para transferir a una cuenta no guardada de otro banco](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco) | Hecho documentado | 14/10/2026 | T02 a T08 |
| F2 | [Página oficial de Banca Móvil](https://www.pichincha.com/banca-movil) | Hecho documentado | 14/10/2026 | T01 |
| F3 | `alcance-comun.md` del repositorio | Definición del grupo | 13/10/2026 | T01 a T08 |
| F4 | `curva/matriz-emocional.csv` y `curva/justificacion.md`, del rol B | Autorreporte de un evaluador | 14/10/2026 | T01 a T08 |
| F5 | `curva/evidencias-visuales-externas.md`, imágenes EV-01 a EV-03 de la guía oficial | Hecho documentado | 14/10/2026 | T03, T04 |
| F6 | Material del curso, tema Emoción y experiencia de usuario | Marco teórico | Por confirmar | Reflexiones |

Las pantallas cambian con cada versión. La versión exacta de la app instalada no está verificada, así que se registrará cuando alguien la observe de forma directa.

## 2. Tipos de evidencia

Cada afirmación del informe debe llevar una de estas etiquetas.

1. **Hecho documentado.** Sale de la ayuda oficial, con enlace y fecha.
2. **Observación directa.** Alguien del grupo inspeccionó la app, con pantalla, fecha y versión si se conocen.
3. **Evaluación experta o hipótesis.** Inferencia del grupo, sin atribuirla a usuarios reales.
4. **Prueba con personas.** Solo si hubo consentimiento y notas anónimas.

Hoy el grupo tiene tipos 1 y 3, y un autorreporte individual dentro del tipo 2. No existen pruebas con personas, y no se va a decir que existen.

## 3. Trazabilidad T01 a T08

| ID | Momento | Documento oficial | Estado actual |
|---|---|---|---|
| T01 | Acceso | F2, contexto general | Autorreporte, valor +1 |
| T02 | Encontrar Transferir dinero | F1 | Autorreporte, valor +3 |
| T03 | Nuevo contacto y Otros bancos | F1 pasos 2 y 3, imágenes EV-01 y EV-02 | Autorreporte, valor -1 |
| T04 | Banco y datos del beneficiario | F1 paso 4, imagen EV-03 | Autorreporte, valor +2 |
| T05 | Validar beneficiario | F1, texto | Autorreporte, valor +3 |
| T06 | Monto y cuenta de origen | F1, texto | Autorreporte, valor +1 |
| T07 | Revisar y confirmar | F1, texto | Autorreporte, valor +2 |
| T08 | Comprobante | F1 paso 9, texto | Autorreporte, valor +1 |

Los valores vienen de la matriz del rol B y no se corrigieron aquí.

## 4. Consentimiento y privacidad

Antes de cualquier observación con otra persona se lee y se acepta esto.

- La participación es voluntaria y se puede parar en cualquier momento.
- Es un ejercicio académico de IHC. No se evalúa a la persona, se evalúa la interfaz.
- Se anota solo el código del participante, por ejemplo P1, edad en rango y nivel de experiencia digital.
- No se registran nombres, cédulas, números de cuenta, saldos, contraseñas, códigos OTP ni comprobantes.
- No se toman capturas de la cuenta personal. Si se necesita imagen, se usa material público oficial o el prototipo.
- Las notas se guardan anonimizadas y se pueden borrar si la persona lo pide.

Texto corto de consentimiento para leer en voz alta:

> Voy a pedirte que pruebes un ejercicio de una tarea ficticia, para una clase de la universidad. No hace falta que hagas ninguna transferencia real ni que me muestres datos tuyos. Si algo te incomoda, puedes parar cuando quieras. Anotaré solo tus comentarios sobre la pantalla, sin tu nombre. ¿Aceptas participar?

## 5. Límite previo a la confirmación

- No se hacen transferencias reales por la tarea.
- No se crean cuentas bancarias ficticias.
- En la app real, el recorrido de cualquier observación termina antes de pulsar Confirmar.
- T08 se estudia con material público oficial o con el prototipo, nunca con un comprobante personal.
- No se hacen auditorías de seguridad.

Nota para la integración. La justificación del rol B menciona un comprobante de una transferencia actual hecha durante la evaluación. Eso choca con este límite y con `alcance-comun.md`. El grupo debe decidir cómo lo redacta antes del PDF. Se anota en la sección 9.

## 6. Tarea y preguntas para la observación breve

**Escenario.** Necesitas enviar dinero a una persona cuya cuenta de otro banco todavía no tienes guardada. Quieres verificar el destinatario y entender el estado final.

**Tareas.**
1. Ubicar dónde se empieza una transferencia.
2. Encontrar cómo agregar un contacto nuevo de otro banco.
3. Decir qué datos del beneficiario espera que le pidan.
4. Explicar, con sus palabras, cómo sabe que el nombre del beneficiario es el correcto.
5. Señalar en la pantalla de revisión qué datos mira antes de confirmar.
6. Contar qué espera ver cuando termine la operación.

**Preguntas, en este orden.**
1. ¿Qué esperabas que pasara aquí?
2. ¿Qué parte no te quedó clara?
3. ¿En qué momento sentiste más seguridad o más duda?
4. ¿Qué cambiarías?

**Registro por touchpoint.** Se llena una fila por momento.

| Participante | Touchpoint | Tarea lograda, sí o no | Claridad 1 a 5 | Confianza 1 a 5 | Emoción dicha por la persona | Nota anonimizada |
|---|---|---|---|---|---|---|
| P1 | T03 | | | | | |

La tabla va vacía a propósito. No se llena con datos inventados.

## 7. Plan para comparar la interfaz de referencia con el prototipo

Aplica cuando el rol C tenga el comparativo en Figma.

1. Dos versiones del mismo paso, la de referencia y la propuesta académica, marcada como Propuesta académica, no interfaz oficial.
2. Si hay participantes, cada uno ve primero una versión y luego la otra. Se alterna el orden entre personas para no favorecer a ninguna.
3. Por cada versión se miden tres cosas.
   - **Claridad**, de 1 a 5, con la pregunta ¿qué tan claro te quedó este paso?
   - **Confianza**, de 1 a 5, con la pregunta ¿qué tanta confianza te da enviar dinero con esta pantalla?
   - **Errores de interpretación**, que es cuántas veces la persona entendió mal un dato, por ejemplo confundió el banco, el monto o el nombre.
4. Se comparan promedios y se dice cuántas personas fueron. Con muy pocas personas se habla de tendencia, no de prueba.
5. Si no hay participantes, la comparación se presenta como evaluación experta del grupo con las heurísticas de Nielsen, y se dice así en el informe.

## 8. Criterios para decir que una mejora funcionó

- La claridad o la confianza sube frente a la referencia.
- Bajan los errores de interpretación.
- Las personas explican con sus palabras lo que significa la pantalla.
- Ningún comentario nuevo muestra una confusión que antes no existía.

Si falta alguno, el informe lo escribe como hipótesis pendiente.

## 9. Pendientes

- [ ] Confirmar la fecha de consulta de F1 y F2 abriendo los enlaces.
- [ ] Anotar la versión de la app si alguien la observa.
- [ ] Decidir con el grupo cómo se redacta el comprobante de T08.
- [ ] Enlazar la fuente F6 con el material exacto de la clase.
- [ ] Revisar este protocolo contra los hallazgos de A, B y C en la integración.
