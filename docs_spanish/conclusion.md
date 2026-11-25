# Conclusión

← [Volver al documento principal](README.md)

*Traducción de [conclusion.md](../conclusion.md).*

A lo largo de cuatro pruebas, pregunté a Claude (Opus 5.5 y Haiku 5.5) por las manifestaciones y los disturbios en Francia del otoño de 2026, acontecimientos ocurridos **después** de su entrenamiento. Primero con la búsqueda web desactivada, después con un artículo de prensa, luego con preguntas repetidas y, por último, con la búsqueda web activada. Esto es lo que aprendí.

## 1. Cuando no lo sabía, lo decía

Con la búsqueda web desactivada, Claude no sabía nada de los acontecimientos de 2026, y lo **dijo** en lugar de inventarse algo. No intentó «rellenar los huecos» con información que no tenía. En términos de predicción del siguiente token, la continuación más probable que aprendió en el entrenamiento fue «no lo sé», y no una respuesta inventada.

Esto también muestra un límite: no puedo «enseñar» algo nuevo al modelo en una conversación. Lo que sí puedo hacer es darle información (un artículo) o dejar que busque. En ambos casos, la información nueva solo vive en la conversación, no en el modelo.

## 2. Las herramientas forman parte del contexto

Con la búsqueda web desactivada, Claude me pedía a menudo que la activara, sobre todo Haiku. Trataba todo lo que decía sobre la actualidad como una suposición, y decía que sería **más fiable** con la búsqueda web activada. Incluso cuando intenté llevarlo en otra dirección y le dije que no quería activarla, siguió proponiéndolo. Probablemente es un comportamiento aprendido en el ajuste fino (*fine-tuning*): el modelo es consciente de los límites de su conocimiento y sabe qué herramienta los cubre.

Para mí es uno de los hallazgos más importantes: **el contexto (la memoria de trabajo) no se construye solo con lo que escribo, sino también con las herramientas que dejo usar al modelo.** Activar o desactivar la búsqueda web cambia lo que el modelo puede saber en una conversación. De todas sus herramientas, la búsqueda web es una de las más importantes para la actualidad.

## 3. Lo que está en el contexto influye mucho en los siguientes tokens

Varias veces, lo que ya estaba en la conversación determinó la respuesta:

- En la segunda prueba, Haiku metió por error a Jean-Michel Blanquer en la conversación y, más tarde, dio su nombre como el ministro más reciente que conocía, con unos cuatro años de retraso. En un chat limpio (tercera prueba), nombró al ministro correcto 7 veces de 8.
- Con la búsqueda web activada, las respuestas se construyeron sobre todo con lo que encontraba la búsqueda. Temas frecuentes en internet, como la inmigración, podían aparecer antes de que yo preguntara por ellos.

El modelo no solo responde a mi pregunta: continúa todo lo que puede ver.

## 4. Puede haber errores incluso con una fuente

Cuando di a Claude un artículo de prensa, la mayoría de sus respuestas se ciñeron a él, pero algunos detalles se **inventaron o se añadieron** de todos modos. Cuando solo podía ver las direcciones web de las fuentes del artículo, concluyó que las protestas empezaron «hacia el 1 de octubre» (el artículo dice el 17 de septiembre), y se colaron algunos detalles de su entrenamiento sin avisar.

No estoy del todo seguro de por qué ocurre, pero creo que es lo que pasa cuando **la predicción del siguiente token se encuentra con un hueco en el conocimiento**: cuando el modelo solo ve parte de la información, rellena el hueco con lo que le parece más probable, y el resultado puede parecer plausible y aun así ser falso.

## 5. Sin búsqueda, las preguntas que cambian con el tiempo eran difíciles

Con la búsqueda web desactivada, Claude a veces se negaba a responder preguntas cuya respuesta cambia con el tiempo, como quién es el ministro de Educación de Francia. En la segunda prueba hicieron falta ocho mensajes para obtener un nombre, y ese nombre estaba desfasado. En la tercera prueba bastó una sola pregunta clara: la forma de preguntar importa (capacidad de dirección).

## 6. Los dos modelos son claramente distintos

Haiku 5.5 dio respuestas más cortas, con otro estilo de escritura y más listas. También se contradijo más a menudo, fue menos constante de un intento a otro y, con la búsqueda web activada, contó una historia menos completa. En estas pruebas, **Haiku pareció menos fiable que Opus** para preguntas sobre la actualidad social. Opus dio respuestas más largas y cuidadosas, siguió mejor la conversación y dijo con más claridad de dónde venía su información. Estas conclusiones se basan en un número pequeño de preguntas e intentos.

## 7. Con todas sus herramientas, trabajar con IA es mucho más fácil, pero no está libre de errores

Con la búsqueda web activada, casi todas las preguntas obtuvieron una respuesta directa y detallada a la primera. Las respuestas venían **sobre todo de la búsqueda, no del entrenamiento**, aunque el entrenamiento seguramente sirvió para estructurar las frases y entender la información, por ejemplo, que «detención» y «custodia» no son lo mismo.

Pero hubo errores en todas las pruebas: fechas equivocadas, contradicciones, nombres desfasados y cifras que cambiaban de una fuente a otra. Así que los modelos no siempre tienen razón. La mejor forma de trabajar con la IA es **aprovechar sus puntos fuertes y gestionar sus puntos débiles**:

- activar las herramientas que necesita (para la actualidad, la búsqueda web);
- darle un buen contexto, y recordar que todo lo que hay en la conversación influye en la respuesta;
- hacer preguntas claras, y preguntar más de una vez cuando sea importante;
- comprobar uno mismo los datos importantes en las fuentes.

## Las cuatro ideas, en una frase cada una

- **Predicción del siguiente token:** el modelo siempre escribe la continuación más probable; cuando falta información, esa continuación puede ser «no lo sé», o un detalle plausible pero falso.
- **Conocimiento:** el entrenamiento se detiene en una fecha de corte; después, el modelo solo puede saber lo que le dan la conversación o sus herramientas.
- **Memoria de trabajo:** todo lo que hay en la conversación (mis palabras, sus respuestas anteriores, los documentos y los resultados de búsqueda) determina lo que viene después, a veces más que su entrenamiento.
- **Capacidad de dirección:** la forma de preguntar y las herramientas que permito cambian mucho la respuesta, pero insistir más no siempre lleva a una respuesta mejor.
