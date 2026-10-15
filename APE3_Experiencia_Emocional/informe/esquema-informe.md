# Esquema del informe grupal en PDF

**Responsable de este esquema:** Mauricio Guevara, GitHub @Mauri10G. **Issue:** #4.
**Extensión planificada:** 6 páginas como máximo, 4 como mínimo. El PDF final no existe todavía y se arma en la integración grupal.

## Distribución propuesta

| Página | Contenido | Viene de | Responsable del insumo |
|---|---|---|---|
| 1 | Portada, datos del grupo, enlace al repositorio GitHub, objetivo y alcance del flujo | README y `alcance-comun.md` | D |
| 1 a 2 | Análisis del usuario, diferencia entre usabilidad y experiencia, dos cualidades pragmáticas y dos hedónicas | `analisis/analisis-ux.md` | A |
| 2 a 3 | Matriz emocional T01 a T08 y curva emocional, con los momentos de verdad | `curva/` | B |
| 3 a 4 | Tres problemas, principio HCI de cada uno y tres mejoras | `mejoras/problemas-y-propuestas.md` | C |
| 4 a 5 | Comparativo antes y después en Figma, con la etiqueta Propuesta académica, no interfaz oficial | `mejoras/antes-despues.png` y `enlace-figma.md` | C |
| 5 | Método, tipos de evidencia, privacidad y limitaciones | `evidencias/protocolo-y-fuentes.md` | D |
| 5 a 6 | Respuestas a las tres preguntas de reflexión y conclusiones | `reflexiones/reflexiones.md` | D, con ajustes del grupo |
| 6 | Contribuciones por integrante, con commits y PR, y fuentes | README final | D |

Si el informe se pasa de seis páginas, se reduce primero la sección de método y después el texto de la matriz, sin quitar la curva ni el antes y después.

## Espacios que no pueden faltar

- [ ] Matriz de emociones, problemas y recomendaciones.
- [ ] Curva emocional de ocho momentos, con escala de -3 a +3.
- [ ] Al menos dos momentos de verdad.
- [ ] Antes y después de al menos una pantalla.
- [ ] Conclusiones.
- [ ] Enlace al repositorio GitHub.
- [ ] Tabla de contribuciones con commits y PR de los cuatro.

## Cómo se redacta la evidencia en el informe

- Cada dato lleva su etiqueta, hecho documentado, observación directa o evaluación experta.
- Los valores de la curva se presentan como autorreporte de una persona, no como resultados de usuarios.
- No se publican comprobantes, cuentas, montos ni capturas personales.
- El Figma se rotula como propuesta académica.

## Comprobación de coherencia en la integración

Se hace después de que A, B y C hagan su PR.

1. Los ocho momentos se llaman igual en el análisis, la matriz, la curva y las mejoras.
2. Los valores de la curva coinciden con la matriz y con el texto.
3. Los momentos de verdad del rol B son los que cita C al hablar de problemas.
4. Los tres problemas de C salen de momentos con evidencia y no de suposiciones sueltas.
5. Las respuestas de reflexión usan los mismos hallazgos que la curva y las mejoras.
6. No hay datos personales ni comprobantes identificables.
7. El comprobante de T08 quedó registrado como desviación en `evidencias/protocolo-y-fuentes.md`, sección 5. Falta que Eduardo confirme qué fue la operación.
8. Revisar fechas y versión de la app, que hoy no están indicadas.

## Fuera de alcance

Publicar como final un PDF sin los aportes de A, B y C.
