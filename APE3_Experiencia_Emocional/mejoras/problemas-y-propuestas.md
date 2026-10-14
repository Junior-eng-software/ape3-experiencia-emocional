# Inspección Heurística, Problemas HCI y Propuestas de Mejora (Frente C)

**Aplicación evaluada:** Banca Móvil Banco Pichincha (Ecuador) — Plataforma Android  
**Flujo:** Transferencia interbancaria a una cuenta no guardada de otro banco (`T01`–`T08`)  
**Responsable:** Erick López (`@ErickAloy871`) — Rol C  
**Fecha de inspección:** 14 de octubre de 2026  

> **Declaración metodológica y de protección de datos:** En cumplimiento del protocolo común (`alcance-comun.md`), esta inspección no utiliza datos bancarios reales, números de cuenta, saldos ni códigos OTP. Se distingue explícitamente entre **Hecho documentado** (guía oficial de soporte de Banco Pichincha), **Observación directa** (inspección sin ejecutar transacción real) y **Evaluación experta/hipótesis** (riesgos inferidos mediante principios HCI que requieren validación posterior con usuarios).

---

## 1. Inspección preliminar del flujo (`T01`–`T08`)

Antes de seleccionar los tres problemas críticos, se revisó el recorrido completo definido en el alcance común separando los hechos documentados de los riesgos hipotéticos:

| Touchpoint | Interacción | Tipo de evidencia | Observación / Riesgo identificado |
| :--- | :--- | :--- | :--- |
| **T01** | Acceso / inicio de sesión | Observación directa / Evaluación experta | El acceso biométrico o por PIN ofrece seguridad percibida inicial, aunque posibles demoras de carga generan expectativa neutra (`0` a `+1`). |
| **T02** | Encontrar «Transferir dinero» | Hecho documentado / Observación directa | El acceso principal a «Transferir dinero» es visible desde la pantalla de inicio, facilitando la eficacia inicial (`+1`). |
| **T03** | Elegir «Nuevo contacto» y «Otros bancos» | Hecho documentado / Evaluación experta | El usuario debe distinguir entre contactos guardados y un «Nuevo contacto» y verificar que el destino sea interbancario; existe riesgo leve de confusión si no se percibe de inmediato el cambio de flujo (`-1`). |
| **T04** | Seleccionar banco e ingresar datos de beneficiario | Hecho documentado / Evaluación experta | **Punto crítico 1:** Alta demanda de entrada manual (institución financiera, tipo de cuenta, número de cuenta, identificación y correo opcional). Alto riesgo de fatiga y temor a digitar un dígito erróneo (`-2`). |
| **T05** | Validar y revisar nombre del beneficiario | Hecho documentado / Evaluación experta | **Punto crítico 2 (Momento de verdad):** En transferencias interbancarias la validación del titular depende de la disponibilidad de consulta en línea con la otra entidad. Cuando no se muestra o no destaca con claridad el nombre validado antes de avanzar, surge incertidumbre sobre el destinatario (`-2` a `-3`). |
| **T06** | Ingresar monto y elegir cuenta de origen | Hecho documentado / Observación directa | El ingreso de importe y selección de cuenta de origen es directo, pero requiere verificar saldo disponible y posibles comisiones interbancarias (`0` a `-1`). |
| **T07** | Revisar datos y confirmar | Evaluación experta (sin ejecutar transferencia real) | **Punto crítico 3 (Momento de verdad):** Antes de confirmar el envío, la presentación compacta de los datos críticos (banco destino, cuenta, comisión y tipo de envío: inmediato vs. cámara de compensación) puede generar ansiedad financiera y temor a un error irreversible (`-2`). |
| **T08** | Visualizar / compartir comprobante | Hecho documentado (material público) | La generación del comprobante brinda alivio y cierre del flujo (`+2`), siempre que se distinga claramente si la transferencia fue acreditada de inmediato o quedó en procesamiento interbancario. |

---

## 2. Identificación de Tres Problemas / Riesgos Concretos y Relación HCI (1:1)

A continuación se detallan los tres problemas prioritarios detectados en la inspección, vinculados de forma 1 a 1 con un principio de Interacción Humano–Computador (HCI).

### Problema 1 (Asociado a `T04`): Sobrecarga en la captura manual de datos del beneficiario interbancario
* **Touchpoint asociado:** `T04` — Seleccionar banco e ingresar datos de beneficiario.
* **Tipo de evidencia y fuente:** **Hecho documentado** en la [Guía oficial de Banco Pichincha para transferir a una cuenta no guardada de otro banco](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco) (consulta: 14/10/2026) combinado con **Evaluación experta/hipótesis**.
* **Descripción del problema/riesgo:** Para transferir a otro banco sin registro previo, el usuario debe seleccionar la entidad bancaria en un listado extenso y digitar manualmente múltiples campos secuenciales (tipo de cuenta, número de cuenta, tipo y número de documento de identidad, nombre/alias y correo electrónico). No existe agrupación visual progresiva ni formato asistido (máscaras de entrada por bloques de dígitos), lo que obliga al usuario a alternar repetidamente entre la app bancaria y la fuente externa donde tiene anotados los datos (ej. WhatsApp o nota).
* **Posible impacto emocional:** **Preocupación, tensión y fatiga (`-2`)**. El temor a equivocarse en un solo dígito del número de cuenta o cédula disminuye la sensación de control.
* **Nivel de certeza:** **Medio-Alto** (la cantidad de campos requeridos es un hecho documentado; la carga emocional asociada se formula como hipótesis experta sujeta a prueba con usuarios).
* **Principio HCI vulnerado (Relación 1:1):** **Reducción de la Carga Cognitiva (Memoria de Trabajo) y Heurística #5 de Nielsen (Prevención de errores)**. Exigir la retención y transcripción continua de cadenas numéricas largas sin segmentación visual ni validación en tiempo real incrementa la carga cognitiva extrínseca y la probabilidad de error de captura (*slips*).

---

### Problema 2 (Asociado a `T05`): Incertidumbre en la retroalimentación de validación del titular de otro banco
* **Touchpoint asociado:** `T05` — Validar y revisar nombre del beneficiario (Momento de verdad).
* **Tipo de evidencia y fuente:** **Hecho documentado** (guía oficial de soporte de Banca Móvil) y **Evaluación experta/hipótesis**.
* **Descripción del problema/riesgo:** Al tratarse de una transferencia a otro banco, el usuario necesita certeza de que el número de cuenta e identificación ingresados corresponden efectivamente a la persona correcta. Si el sistema no diferencia visualmente de forma prominente entre un **«Titular verificado en línea con el banco destino»** y un **«Nombre ingresado manualmente sin verificación externa»**, el usuario avanza hacia el pago con incertidumbre sobre si el dinero llegará al destinatario esperado o será rechazado posteriormente.
* **Posible impacto emocional:** **Desconfianza e incertidumbre marcada (`-2` a `-3`)**. Impacta directamente en la cualidad hedónica de *confianza percibida*.
* **Nivel de certeza:** **Medio** (evaluación experta basada en heurísticas sobre el momento de verdad `T05`; requiere verificación empírica en pruebas de usabilidad).
* **Principio HCI vulnerado (Relación 1:1):** **Retroalimentación (Feedback inmediato) y Heurística #1 de Nielsen (Visibilidad del estado del sistema)**. El sistema debe informar de manera inmediata, inequívoca y con codificación visual clara qué datos han sido validados automáticamente por la red interbancaria y cuáles dependen exclusivamente de la digitación del usuario.

---

### Problema 3 (Asociado a `T07`): Jerarquía visual homogénea y falta de claridad sobre el tiempo de acreditación antes de confirmar
* **Touchpoint asociado:** `T07` — Revisar datos y confirmar (Momento de verdad previo al envío).
* **Tipo de evidencia y fuente:** **Evaluación experta/hipótesis** sobre el paso de revisión previa (respetando el límite de prueba de no ejecutar transferencias reales).
* **Descripción del problema/riesgo:** En el resumen previo a la confirmación (`T07`), los datos críticos para la decisión final (nombre del beneficiario, banco de destino, número de cuenta, monto total, comisión interbancaria y tiempo estimado de acreditación: inmediato vs. diferido/SPI) suelen presentarse como una lista de texto plano con peso visual similar. Además, modificar un dato específico desde este punto puede percibirse como un retroceso que obliga a repetir pasos previos.
* **Posible impacto emocional:** **Duda, ansiedad de confirmación y temor al error irreversible (`-2`)**. Afecta la cualidad pragmática de *prevención/recuperación de errores* y la cualidad hedónica de *tranquilidad*.
* **Nivel de certeza:** **Medio** (hipótesis derivada de inspección heurística experta).
* **Principio HCI vulnerado (Relación 1:1):** **Heurística #3 de Nielsen (Control y libertad del usuario) y Heurística #8 (Diseño estético y minimalista / Jerarquía visual)**. En un momento de verdad financiero, la interfaz debe destacar con mayor jerarquía los atributos críticos de verificación y ofrecer micro-controles de edición directa («Editar cuenta», «Editar monto») sin perder el progreso del formulario.

---

## 3. Tres Propuestas de Mejora Concretas (Relación 1:1)

> **Nota de alcance:** Los efectos emocionales descritos a continuación representan el **efecto esperado (hipótesis de diseño)** y **no un resultado demostrado** hasta ejecutar el protocolo de validación con usuarios.

| ID | Problema que resuelve | Principio HCI aplicado | Propuesta de mejora concreta (Cambio de diseño) | Efecto emocional esperado (No demostrado) |
| :--- | :--- | :--- | :--- | :--- |
| **M1** | **Problema 1 (`T04`):** Sobrecarga en captura manual de datos del beneficiario. | **Reducción de Carga Cognitiva y Prevención de Errores (Heurística #5)** | **1. Entrada asistida y segmentada con pegado inteligente:** Agrupar visualmente el formulario de `T04` en dos bloques claros (*Datos del banco* y *Datos del titular*), aplicar formato automático en bloques de 4 dígitos al número de cuenta para facilitar la lectura visual (ej. `2200 1234 56`) e incorporar validación en línea del formato de cédula/RUC antes de habilitar el botón «Continuar». | Reducir la tensión de captura de `-2` hacia un estado neutral o cómodo (`0` a `+1`), disminuyendo la fatiga cognitiva y el temor a errores de digitación. |
| **M2** | **Problema 2 (`T05`):** Incertidumbre sobre la validación del titular en otro banco. | **Retroalimentación inmediata y Visibilidad del Estado del Sistema (Heurística #1)** | **2. Tarjeta de estado de verificación del beneficiario (`T05`):** Mostrar inmediatamente después de ingresar cuenta e identificación un bloque destacado con insignia semántica: **Verde («Titular verificado con [Banco Destino]»)** mostrando el nombre oficial recuperado, o **Ámbar («Verificación en línea no disponible: confirma que el nombre y cédula coincidan con tu destinatario»)**. | Transformar la incertidumbre de `T05` (`-2`/`-3`) en **confianza percibida y alivio (`+1` a `+2`)**, eliminando la ambigüedad sobre quién recibirá los fondos. |
| **M3** | **Problema 3 (`T07`):** Baja jerarquía visual y fricción para corregir datos en la pantalla de confirmación. | **Jerarquía Visual (Heurística #8) y Control y Libertad del Usuario (Heurística #3)** | **3. Resumen de confirmación jerarquizado con edición rápida y aviso de acreditación (`T07`):** Rediseñar la tarjeta de revisión destacando en nivel primario el **Monto, Banco Destino y Beneficiario**, añadir una etiqueta explícita del **Tiempo de acreditación y comisión** (*«Acreditación inmediata · Comisión $0.41»*), e incluir enlaces de acción directa (`Editar`) junto a cada bloque para corregir sin reiniciar el flujo. | Elevar la experiencia en el momento de verdad `T07` de ansiedad (`-2`) a **tranquilidad y seguridad (`+2`)**, fortaleciendo la motivación para completar la tarea. |

---

## 4. Impacto Conjunto en Confianza, Motivación y Experiencia de Usuario (UX)

1. **Favorecimiento de la Confianza:** Al incorporar la tarjeta de verificación explícita en `T05` (**M2**) y el desglose transparente de tiempo de acreditación y comisión en `T07` (**M3**), la interfaz pasa de ser una «caja negra» a un sistema transparente. El usuario comprende exactamente qué validó el banco y bajo qué condiciones viajará su dinero.
2. **Favorecimiento de la Motivación y Control:** La reducción del esfuerzo de lectura mediante máscaras numéricas en `T04` (**M1**) y los botones de edición directa en `T07` (**M3**) reducen la fricción pragmática. El usuario siente que puede corregir cualquier error sin castigo (sin perder los datos ya ingresados), manteniendo la fluidez hacia la meta.
3. **De la Usabilidad a la Satisfacción (UX):** Mientras la usabilidad básica garantiza que el usuario *pueda* enviar la transferencia, estas tres mejoras atienden la dimensión hedónica: mitigan los picos de estrés financiero en los momentos de verdad (`T05` y `T07`), propiciando una transición emocional positiva hacia el cierre en `T08`.

---

## 5. Propuesta de Validación de las Mejoras

Dado que las mejoras **M1, M2 y M3** se formulan desde una inspección heurística, para demostrar empíricamente su efectividad se propone el siguiente protocolo de validación con el prototipo de Figma (sin usar datos bancarios reales):

1. **Diseño de prueba A/B moderada (Prototipo en Figma):**
   * **Grupo/Condición A (Línea base):** Recorrido interactivo por la recreación fiel del flujo actual (`T04`, `T05`, `T07`) con datos ficticios estandarizados.
   * **Grupo/Condición B (Propuesta académica):** Recorrido por el prototipo rediseñado con las mejoras **M1, M2 y M3**.
2. **Métricas pragmáticas (Usabilidad):**
   * **Tasa de detección de errores inducidos:** Entregar al participante un número de cuenta de prueba con un dígito alterado en el resumen y medir cuántos participantes lo detectan y corrigen en `T05`/`T07` usando el botón `Editar`.
   * **Tiempo en tarea (Time on Task):** Tiempo empleado en revisar y confirmar los datos en `T04`–`T07`.
3. **Métricas hedónicas y emocionales (UX):**
   * **Autoreporte emocional por touchpoint:** Al finalizar `T04`, `T05` y `T07`, solicitar al participante que valore su nivel de tranquilidad/confianza en la misma escala entera del estudio (`-3` a `+3`) y comparar si la curva emocional en `T05` y `T07` sube respecto a la línea base.
   * **Pregunta de comprensión de estado:** Preguntar al usuario antes de pulsar *Confirmar*: *«¿El banco verificó el nombre del destinatario y cuánto tardará en llegar el dinero?»* para comprobar si **M2** y **M3** eliminan la incertidumbre.