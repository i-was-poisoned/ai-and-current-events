# ai-and-current-events: documento principal (español)

*También disponible en [English](../docs_english/README.md) · [Français](../docs_french/README.md)*

Este es el punto de partida del proyecto. Léelo de arriba abajo: cada vez que veas una flecha (**→**), puedes abrir ese documento, volver aquí y seguir leyendo.

## 1. De qué trata este proyecto

Es un trabajo de investigación sobre cómo se comporta un modelo de IA cuando se le pregunta por acontecimientos ocurridos **después** de su entrenamiento: las manifestaciones y disturbios en Francia del otoño de 2026.

También es una forma de aprender: uso la IA para entender mejor la IA.

## 2. Las cuatro ideas que quiero entender

- **Predicción del siguiente token** (*next-token prediction*): el modelo escribe su respuesta pieza a pieza (cada pieza es un *token*), eligiendo cada vez una continuación probable según los patrones que aprendió durante el entrenamiento. ¿Qué ocurre cuando el tema es algo que nunca vio?
- **Conocimiento** (*knowledge*): lo que el modelo aprendió durante el entrenamiento, que termina en una *fecha de corte* (*knowledge cutoff*). La de Claude Opus 5.5 es junio de 2026, así que estos acontecimientos no están en su entrenamiento.
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
5. Vuelve aquí para leer el resumen de abajo.

Las capturas de pantalla que sirven de prueba están en [first_test/screenshots/](../first_test/screenshots/). El documento original, en inglés, es [first_test/README.md](../first_test/README.md).

## 4. Lo que he descubierto hasta ahora

1. **Desactivar la búsqueda web no significa «solo datos de entrenamiento».** Con la búsqueda web desactivada, Claude respondió a una pregunta sobre el tiempo con datos en tiempo real de una herramienta meteorológica integrada. *(Comprobación 1)*
2. **El modelo siempre sabe la fecha de hoy.** La aplicación se la da al principio de cada chat, en sus instrucciones ocultas (el *system prompt*), aunque su entrenamiento termine a mediados de 2026. *(Comprobación 3)*
3. **Sin información, reconoció que no lo sabía.** No se inventó nada sobre los acontecimientos de 2026 y dijo que su conocimiento de los meses justo anteriores a su fecha de corte es «menos completo». *(Preguntas 1 y 2)*
4. **Las líneas grises de estado de la aplicación pueden confundir.** Una línea como «Checking recent French news…» describe lo que el modelo está pensando; no es una búsqueda. *(Pregunta 2)*
5. **A partir de pistas muy pequeñas, puede construir hechos falsos.** Cuando solo podía ver las direcciones web de las fuentes del artículo, concluyó que las protestas empezaron «hacia el 1 de octubre»; el artículo dice el 17 de septiembre. *(Pregunta 3)*
6. **Con una fuente, se ciñe casi siempre a ella.** Para los hechos usó el artículo; para las preguntas generales usó su entrenamiento y lo dijo. Aun así, se colaron pequeños detalles de su entrenamiento sin avisar. *(Pregunta 3)*
7. **No aceptó una pregunta tendenciosa.** Cuando le pregunté si había sido «un disturbio pacífico», dijo que no. *(Pregunta 3)*

## 5. Próximos pasos

- Hacer las tres preguntas previstas en la pregunta 3 (el total de detenidos, qué pasó en noviembre y quién es el actual ministro o ministra de Educación).
- Repetir las preguntas a través de la **API**, donde no hay instrucciones ocultas ni fecha, y comparar.
- Probar otros modelos y otros niveles de esfuerzo.
