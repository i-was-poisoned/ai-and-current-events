# ai-and-current-events: documento principal (español)

*También disponible en [English](../docs_english/README.md) · [Français](../docs_french/README.md)*

Este es el punto de partida del proyecto. Léelo de arriba abajo: cada vez que veas una flecha (**→**), puedes abrir ese documento, volver aquí y seguir leyendo.

## 1. De qué trata este proyecto

Es un trabajo de investigación sobre cómo se comporta un modelo de IA cuando se le pregunta por acontecimientos ocurridos **después** de su entrenamiento: las manifestaciones y disturbios en Francia del otoño de 2026.

También es una forma de aprender: uso la IA para entender mejor la IA.

## 2. Las cuatro ideas que quiero entender

- **Predicción del siguiente token** (*next-token prediction*): el modelo escribe su respuesta pieza a pieza (cada pieza es un *token*), eligiendo cada vez una continuación probable según los patrones que aprendió durante el entrenamiento. ¿Qué ocurre cuando el tema es algo que nunca vio?
- **Conocimiento** (*knowledge*): lo que el modelo aprendió durante el entrenamiento, que termina en una *fecha de corte* (*knowledge cutoff*). La de Claude Opus 5.5 es junio de 2026, y Claude Haiku 5.5 también dice que su conocimiento termina en junio de 2026, así que estos acontecimientos no están en su entrenamiento.
- **Memoria de trabajo** (*working memory*): lo que el modelo puede ver en la conversación actual (mis preguntas, sus respuestas anteriores y los resultados de búsqueda o archivos que haya). Es la *ventana de contexto*, y es distinta de lo que aprendió en el entrenamiento.
- **Capacidad de dirección** (*steerability*): cuánto cambia la respuesta según cómo pregunto (las palabras, las instrucciones, el enfoque).

## 3. Cómo leer la primera prueba

La primera prueba está entera en un solo documento, [first_test.md](first_test.md) (traducción al español). Lee sus partes en este orden:

1. **La configuración**: dónde y cómo se hizo la prueba (aplicación de escritorio de Claude, chat de incógnito, Claude Opus 5.5, esfuerzo Medium, búsqueda web desactivada).
   → [first_test.md](first_test.md), la tabla del principio.
2. **Comprobaciones previas**: tres comprobaciones rápidas para ver a qué puede seguir accediendo Claude con la búsqueda web desactivada.
   → [first_test.md](first_test.md), sección *Comprobaciones previas*.
3. **Preguntas 1 y 2**: lo que dice Claude sobre los disturbios en Francia sin ninguna ayuda, primero en general y luego en 2026.
   → [first_test.md](first_test.md), sección *Preguntas y respuestas*.
4. **Pregunta 3**: lo que hace Claude cuando le doy un artículo sobre las protestas de 2026.
   → [first_test.md](first_test.md), sección *Pregunta 3*.
   - → Opcional: la conversación completa (en inglés), [first_test/q3-transcript.md](../first_test/q3-transcript.md).
   - → Opcional: el artículo que le di a Claude, [first_test/sources/](../first_test/sources/README.md).
5. Vuelve aquí y sigue con la segunda prueba.

Las capturas de pantalla que sirven de prueba están en [first_test/screenshots/](../first_test/screenshots/). El documento original, en inglés, es [first_test/README.md](../first_test/README.md).

## 4. Cómo leer la segunda prueba

La segunda prueba repite la pregunta 3 (el artículo y las mismas preguntas) con otro modelo, **Claude Haiku 5.5**, y compara las respuestas con las de Opus 5.5.

1. **Qué cambió y por qué**: la configuración y las diferencias con la primera prueba.
   → [second_test.md](second_test.md), la tabla del principio y *En qué se diferencia de la primera prueba*.
2. **La comparación, pregunta por pregunta**: fragmentos breves de los dos modelos.
   → [second_test.md](second_test.md), sección *Comparación, pregunta por pregunta*.
3. **Las observaciones**.
   → [second_test.md](second_test.md), sección *Observaciones*.
   - → Opcional: la conversación completa con Haiku (en inglés), [second_test/transcript.md](../second_test/transcript.md).
4. Vuelve aquí y sigue con la tercera prueba.

El documento original, en inglés, es [second_test/README.md](../second_test/README.md).

## 5. Cómo leer la tercera prueba

La tercera prueba intenta averiguar por qué Haiku dio, en la segunda prueba, el nombre de un ministro con unos cuatro años de retraso. Empieza con mi hipótesis y la pone a prueba repitiendo preguntas a Haiku 5.5 y a Opus 5.5, sin artículo.

1. **Mi hipótesis y el método**.
   → [third_test.md](third_test.md), secciones *Mi hipótesis (antes de la prueba)* y *Método*.
2. **Los resultados**: una tabla con los nombres que dieron y después cada respuesta palabra por palabra.
   → [third_test.md](third_test.md), sección *Resultados*.
3. **Lo que descubrí y los límites de la prueba**.
   → [third_test.md](third_test.md), secciones *Lo que descubrí (después de la prueba)* y *Límites de esta prueba*.
4. Vuelve aquí y sigue con la cuarta prueba.

El documento original, en inglés, es [third_test/README.md](../third_test/README.md).

## 6. Cómo leer la cuarta prueba

La cuarta y última prueba **activa** la búsqueda web y repite preguntas de las pruebas anteriores, primero a Haiku 5.5 y después a Opus 5.5, para ver qué cambia cuando Claude puede encontrar por sí mismo información actual.

1. **Mi hipótesis**.
   → [fourth_test.md](fourth_test.md), sección *Mi hipótesis (antes de la prueba)*.
2. **Parte 1, Haiku 5.5**: la comprobación de que la búsqueda web funciona, las cinco preguntas (cada una comparada con la respuesta con la búsqueda desactivada) y las observaciones.
   → [fourth_test.md](fourth_test.md), sección *Parte 1: Haiku 5.5*.
3. **Parte 2, Opus 5.5**: las mismas preguntas, cada una comparada con la respuesta de Haiku, y las observaciones.
   → [fourth_test.md](fourth_test.md), sección *Parte 2: Opus 5.5*.
   - → Opcional: las dos conversaciones completas (en inglés), [fourth_test/transcript.md](../fourth_test/transcript.md).
4. **¿Era correcta mi hipótesis?** Y los puntos que hay que tener en cuenta.
   → [fourth_test.md](fourth_test.md), secciones *¿Era correcta mi hipótesis?* y *Puntos importantes que hay que tener en cuenta*.
5. Vuelve aquí para leer el resumen de abajo.

El documento original, en inglés, es [fourth_test/README.md](../fourth_test/README.md).

## 7. Lo que he descubierto hasta ahora

### En la primera prueba (Opus 5.5)


1. **Desactivar la búsqueda web no significa «solo datos de entrenamiento».** Con la búsqueda web desactivada, Claude respondió a una pregunta sobre el tiempo con datos en tiempo real de una herramienta meteorológica integrada. *(Comprobación 1)*
2. **El modelo siempre sabe la fecha de hoy.** La aplicación se la da al principio de cada chat, en sus instrucciones ocultas (el *system prompt*), aunque su entrenamiento termine a mediados de 2026. *(Comprobación 3)*
3. **Sin información, reconoció que no lo sabía.** No se inventó nada sobre los acontecimientos de 2026 y dijo que su conocimiento de los meses justo anteriores a su fecha de corte es «menos completo». *(Preguntas 1 y 2)*
4. **Las líneas grises de estado de la aplicación pueden confundir.** Una línea como «Checking recent French news…» describe lo que el modelo está pensando; no es una búsqueda. *(Pregunta 2)*
5. **A partir de pistas muy pequeñas, puede construir hechos falsos.** Cuando solo podía ver las direcciones web de las fuentes del artículo, concluyó que las protestas empezaron «hacia el 1 de octubre»; el artículo dice el 17 de septiembre. *(Pregunta 3)*
6. **Con una fuente, se ciñe casi siempre a ella.** Para los hechos usó el artículo; para las preguntas generales usó su entrenamiento y lo dijo. Aun así, se colaron pequeños detalles de su entrenamiento sin avisar. *(Pregunta 3)*
7. **No aceptó una pregunta tendenciosa.** Cuando le pregunté si había sido «un disturbio pacífico», dijo que no. *(Pregunta 3)*

### En la segunda prueba (Haiku 5.5 comparado con Opus 5.5)

1. **Mismos hechos, distinto estilo.** Los dos modelos se ciñeron al artículo. Las respuestas de Haiku fueron más cortas desde el principio y usaron más listas, así que la brevedad se debe sobre todo al modelo.
2. **Haiku se mantuvo dentro de la fuente de forma más estricta.** Ante una pregunta que iba más allá del artículo, Opus añadió conocimientos generales y lo dijo; Haiku calificó cualquier explicación de «especulación» y se detuvo.
3. **Haiku fue muy prudente con su fecha de corte, a veces demasiado.** Aunque insistí tres veces, no quiso nombrar al actual ministro de Educación (Édouard Geffray), un nombre que quizá tenía en su entrenamiento.
4. **Pequeñas incoherencias.** Haiku se contradijo sobre qué ministro nombra el artículo e interpretó la palabra «hijacked» de dos formas opuestas.
5. **Patrones parecidos entre modelos.** En la pregunta del «disturbio pacífico», los dos dieron casi la misma frase.
6. **Ser demasiado prudente también puede llevar a equivocarse, y dificulta la conversación.** Con la búsqueda web desactivada, hicieron falta ocho mensajes para que Haiku diera un nombre de su entrenamiento, y el que dio (un ministro de 2017 a 2022) estaba desfasado unos cuatro años.

### En la tercera prueba (una pregunta repetida, Haiku 5.5 y Opus 5.5)

1. **Mi hipótesis era errónea.** Esperaba que ganara el nombre más frecuente (Blanquer). En un chat limpio, Haiku nombró al ministro actual, Édouard Geffray, en 7 de 8 intentos, y nunca a Blanquer.
2. **Una respuesta es solo una muestra.** La misma pregunta con la misma configuración dio 7 veces Geffray y una vez Borne. Hay que preguntar varias veces para ver qué tiende a responder un modelo.
3. **Saber no es encontrar.** Haiku conocía a Geffray, pero lo dejó fuera cuando le pedí la lista de ministros por orden de fechas. La forma de preguntar cambia lo que sale.
4. **Unos modelos son mejores que otros.** Opus nombró a Geffray todas las veces, con su fecha de nombramiento y su gobierno, y dio una lista completa.
5. **Probablemente la conversación explica lo de Blanquer.** En la segunda prueba fue el propio Haiku quien metió a Blanquer en la conversación (el artículo no lo menciona). Lo que ya está en la memoria de trabajo puede arrastrar la respuesta hacia ello. Es una explicación posible, no una prueba.

### En la cuarta prueba (búsqueda web activada, Haiku 5.5 y Opus 5.5)

1. **Mucho más fácil hablar con él.** Mi hipótesis se confirmó con los dos modelos: cada pregunta obtuvo una respuesta directa y detallada a la primera, con fechas, cifras y fuentes. Con Opus fue todavía más fácil que con Haiku.
2. **Más fácil no significa más fiable.** Las cifras cambiaron de una respuesta y de una fuente a otra, y los dos modelos dijeron que no podían confirmarlo todo.
3. **La búsqueda da forma a la historia, pero el modelo elige.** Para acontecimientos que no están en su entrenamiento, la respuesta se construye sobre todo con los resultados de búsqueda (memoria de trabajo). Pero con la misma web, Haiku situó el comienzo a mediados de octubre y Opus a mediados de septiembre, como el artículo de las pruebas anteriores.
4. **Los temas frecuentes en internet pueden aparecer solos.** Haiku mencionó la inmigración antes de que yo preguntara; Opus no. Los dos dijeron que no había pruebas que la respaldaran.
5. **Opus siguió mejor la conversación.** Se refirió a su respuesta anterior y se corrigió, explicó de dónde venían sus cifras y ofreció buscar más con menos frecuencia que Haiku.
6. **Los dos entendieron por qué las cifras no coinciden.** «Detención», «custodia» y «acusación» no son lo mismo, así que no sumaron cifras de fuentes distintas.

## 8. Conclusión

La conclusión reúne lo que me enseñaron las cuatro pruebas, idea por idea.

→ [conclusion.md](conclusion.md)

## 9. Preguntas abiertas

Ideas que no están previstas en este proyecto, para quien quiera continuar:

- ¿La conversación explica la respuesta de Blanquer de la segunda prueba? Hacer las mismas preguntas sobre el ministro en un chat donde no se haya mencionado a Blanquer.
- ¿Qué cambia a través de la **API**, donde no hay instrucciones ocultas ni fecha?
- ¿Qué cambia con otros niveles de esfuerzo?
