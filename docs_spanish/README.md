# El proyecto (español)

Este es un trabajo de investigación sobre cómo se comporta un modelo de IA cuando se le pregunta por acontecimientos ocurridos **después** de su entrenamiento: las manifestaciones y disturbios en Francia del otoño de 2026.

También es una forma de aprender: uso la IA para entender mejor la IA.

## Qué quiero entender

- **Predicción del siguiente token** (*next-token prediction*): el modelo escribe su respuesta pieza a pieza (cada pieza es un *token*), eligiendo cada vez una continuación probable según los patrones que aprendió durante el entrenamiento. ¿Qué ocurre cuando el tema es algo que nunca vio?
- **Conocimiento** (*knowledge*): lo que el modelo aprendió durante el entrenamiento, que termina en una *fecha de corte* (*knowledge cutoff*). La de Claude Opus 5.5 es junio de 2026, así que estos acontecimientos no están en su entrenamiento.
- **Memoria de trabajo** (*working memory*): lo que el modelo puede ver en la conversación actual (mis preguntas, sus respuestas anteriores y los resultados de búsqueda o archivos que haya). Es la *ventana de contexto*, y es distinta de lo que aprendió en el entrenamiento.
- **Capacidad de dirección** (*steerability*): cuánto cambia la respuesta según cómo pregunto (las palabras, las instrucciones, el enfoque).

## La primera prueba

En la aplicación de escritorio de Claude, en un **chat de incógnito** (modo Chat, sin memoria de otras conversaciones), con el modelo **Claude Opus 5.5** (id del modelo `claude-opus-5-5`), esfuerzo **Medium** y la **búsqueda web desactivada**, haré preguntas sobre las manifestaciones en Francia. Sin búsqueda, Claude solo puede responder con lo que aprendió en el entrenamiento.

Las preguntas, las respuestas y lo que observe quedarán registrados en la carpeta [first_test](../first_test/).

## Primer hallazgo: "búsqueda web desactivada" no significa "solo datos de entrenamiento"

Antes de la prueba, comprobé la configuración preguntando por el tiempo de hoy en París, con la búsqueda web desactivada. Aun así, Claude respondió con datos meteorológicos en tiempo real ("Weather data from Google"), usando una herramienta del tiempo integrada en la app que el interruptor de Web search no controla.

Es decir, desactivar la búsqueda web no impide que Claude use otras herramientas que le traen información que no está en sus datos de entrenamiento. Hay que revisar cada respuesta en busca de señales de una herramienta (widgets, tarjetas, fuentes, enlaces). Detalles y captura en [first_test](../first_test/README.md#checks-before-the-test).
