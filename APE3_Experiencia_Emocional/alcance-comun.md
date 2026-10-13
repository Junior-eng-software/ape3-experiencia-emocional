# APE3 — Alcance común y protocolo de referencia

**Fecha de referencia:** 13 de octubre de 2026. **Asignatura:** Interacción Humano–Computador. **Grupo:** 4 integrantes.
**Tema:** Emoción y experiencia de usuario: de la usabilidad a la satisfacción.
**Aplicación:** Banca Móvil Banco Pichincha (Ecuador), plataforma Android.
**Flujo seleccionado:** transferencia interbancaria a una cuenta de un beneficiario nuevo/no guardado.
**Autorización docente:** según lo confirmado por el grupo, se puede evaluar una aplicación existente.
**Estado:** base de estudio; todavía no hay datos de participantes, puntuaciones medidas ni problemas demostrados.

## 1. Objetivo y pregunta
Analizar percepciones y emociones a lo largo del flujo, detectar momentos de confianza/incertidumbre y justificar propuestas según principios IHC.

**Pregunta:** ¿En qué momentos la comprensión de una transferencia a un beneficiario nuevo influye en la confianza y satisfacción de quien usa la app?

## 2. Persona hipotética y tarea
- **Perfil:** estudiante o joven trabajador en Ecuador, 18–30 años, smartphone Android, habilidades digitales intermedias y posible poca experiencia transfiriendo a nuevos destinatarios.
- **Necesidad:** enviar dinero a una cuenta de otro banco y comprobar que los datos de destino son correctos.
- **Expectativas:** localizar la opción; comprender campos; reconocer al beneficiario; revisar banco, importe y cuenta de origen; corregir datos; distinguir claramente el resultado.
- **Precaución:** es un *perfil de referencia*, no una entrevista, usuario observado ni muestra representativa.

**Escenario común:** «Necesitas enviar dinero a una persona cuya cuenta de otro banco todavía no tienes guardada. Quieres verificar el destinatario y asegurarte de comprender el estado final».

**Límite de prueba:** no ejecutar transferencias reales ni captar credenciales. En ejercicios sin transacción, T07 se evalúa hasta antes de confirmar y T08 mediante material público (no fingir observar un comprobante generado).

## 3. Touchpoints invariables
| ID | Interacción | Aspecto UX a evaluar |
|---|---|---|
| T01 | Acceso/inicio de sesión | Comprensibilidad, control y seguridad percibida |
| T02 | Encontrar «Transferir dinero» | Visibilidad del acceso |
| T03 | Elegir «Nuevo contacto» y «Otros bancos» | Consistencia y opciones |
| T04 | Seleccionar banco e ingresar datos de beneficiario | Campos, errores, esfuerzo |
| T05 | Validar y revisar nombre del beneficiario | Retroalimentación y confianza |
| T06 | Ingresar monto y elegir cuenta de origen | Claridad de importes y origen |
| T07 | Revisar datos y confirmar | Prevención de errores, certeza |
| T08 | Visualizar/compartir comprobante | Evidencia y claridad del estado |

T02–T08 sintetizan operaciones indicadas en la documentación oficial; T01 aporta el contexto de acceso. **No asumir que cada touchpoint equivale a una pantalla distinta.** La versión exacta de la app no se ha verificado; registrar fecha y versión cuando exista observación directa.

## 4. Cualidades y escala
**Usabilidad:** eficacia, eficiencia y claridad en la ejecución. **UX:** respuesta cognitiva y emocional (confianza, tranquilidad, tensión, satisfacción) antes, durante y después.

**Dos cualidades pragmáticas a examinar:** claridad de navegación y prevención/recuperación de errores.
**Dos hedónicas a examinar:** confianza percibida y tranquilidad/satisfacción.
Estas características son *dimensiones a evaluar*, no fortalezas demostradas.

| Valor emocional | Interpretación orientativa |
|---|---|
| -3 | Muy negativa: frustración o desconfianza intensa |
| -2 | Negativa: preocupación o confusión marcada |
| -1 | Algo negativa: duda o molestia leve |
| 0 | Neutral |
| +1 | Algo positiva: alivio o comodidad |
| +2 | Positiva: confianza o satisfacción |
| +3 | Muy positiva: tranquilidad y satisfacción intensa |

Usar únicamente **números enteros de -3 a +3**. En cada touchpoint anotar emoción, valoración, justificación, fuente y tipo de evidencia. Identificar al menos **dos momentos de verdad**; candidatos: T05 (beneficiario), T07 (confirmación), T08 (comprobante). Su influencia real no se da por demostrada.

## 5. Etiquetado obligatorio de evidencia
1. **Hecho documentado:** información de ayuda oficial; enlazar URL y fecha de consulta.
2. **Observación directa:** interacción inspeccionada por integrante; registrar versión/fecha si se conocen, pantalla y notas anonimizadas.
3. **Evaluación experta/hipótesis:** inferencia fundada, sin atribuirla a participantes reales.
4. **Prueba con personas:** consentimiento, notas anónimas y cita de condiciones; no inventar testimonios ni métricas.

En resultados distinguir inequívocamente lo documentado, observado y supuesto. No atribuir valoraciones a participantes inexistentes.

## 6. Alcance de entregables
- Análisis del usuario objetivo; diferencia usabilidad/UX; 2 cualidades pragmáticas y 2 hedónicas.
- Matriz y **curva de 6–8 momentos** (aquí: T01–T08), con escala -3 a +3 y justificaciones.
- **Al menos 2 momentos de verdad**.
- **3 problemas/riesgos sustentados**, asociados cada uno con un principio HCI, y **3 mejoras concretas**.
- **Antes/después en Figma** de al menos una pantalla, mostrando qué es original, recreación o rediseño académico.
- Protocolo de validación; respuestas a las tres preguntas de reflexión.
- **Informe grupal PDF de 4–6 páginas**, con enlace al repositorio, y aportes individuales rastreables mediante commits/PR.

## 7. Trabajo paralelo y archivos
Los cuatro frentes parten de este mismo alcance y de fuentes oficiales, no de resultados de otras tareas. Cada quien escribe en su carpeta:
- A: `analisis/analisis-ux.md`, rama `ape3/analisis-ux`.
- B: `curva/matriz-emocional.csv`, `curva/curva-emocional.png`, `curva/justificacion.md`, rama `ape3/curva-emocional`.
- C: `mejoras/problemas-y-propuestas.md`, `mejoras/enlace-figma.md`, `mejoras/antes-despues.png`, rama `ape3/mejoras-figma`.
- D: `evidencias/protocolo-y-fuentes.md`, `reflexiones/reflexiones.md`, `informe/esquema-informe.md`, `informe/propuesta-readme.md`, rama `ape3/evidencias-informe`.

Estados Kanban: **Pendiente → En proceso → En revisión → Finalizado**. El README principal y el PDF definitivo se integrarán en una revisión conjunta posterior; esto **no bloquea** ninguna de las cuatro investigaciones iniciales.

## 8. Seguridad, integridad y límites
No publicar datos de clientes, cuentas, montos reales, saldos, cédulas, OTP ni credenciales. No crear cuentas bancarias ficticias ni presionar a realizar transferencias. Si no hay acceso a la app, usar imágenes públicas oficiales, citarlas y declarar el límite. No realizar auditorías de seguridad. Marcar el Figma propuesto como **«Propuesta académica, no interfaz oficial»**.

## 9. Fuentes principales
- [Guía de transferencia interbancaria a contacto nuevo](https://soporte.pichincha.com/hc/es-419/articles/39805280403355--C%C3%B3mo-transfiero-a-una-cuenta-no-guardada-de-otro-banco).
- [Banca Móvil Banco Pichincha](https://www.pichincha.com/banca-movil).

**Nota:** las pantallas cambian por versión. No mezclar sin aviso documentación publicada con observación de versiones distintas.
