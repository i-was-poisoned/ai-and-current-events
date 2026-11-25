# Cuarta prueba: búsqueda web activada

← [Volver al documento principal](README.md)

*Traducción de [fourth_test/README.md](../fourth_test/README.md). Las preguntas a Claude y sus respuestas se citan en inglés, tal como aparecieron, con la traducción entre paréntesis cuando hace falta.*

En las tres primeras pruebas, la búsqueda web estaba **desactivada**: Claude solo podía usar su entrenamiento y lo que yo le daba (el artículo). En esta última prueba, la búsqueda web está **activada**. Repito preguntas de las pruebas anteriores para ver qué cambia cuando Claude puede buscar información actual por sí mismo.

Este documento trata de **Claude Haiku 5.5**. La misma prueba con Opus 5.5 viene después.

| Configuración    | Valor |
|------------------|-------|
| Fecha            | 25 de noviembre de 2026 |
| Dónde            | Aplicación de escritorio de Claude, **chat de incógnito** (modo Chat), cuenta de organización |
| Memoria          | No se usa (chat de incógnito) |
| Modelo           | **Claude Haiku 5.5** (`claude-haiku-5-5`) |
| Esfuerzo         | Medium (medio) |
| Búsqueda web     | **Activada** (en el menú **+**); Research desactivado |
| Fuente           | Ninguna dada por mí: Claude busca sus propias fuentes |

**Conversación completa** (en inglés): [fourth_test/transcript.md](../fourth_test/transcript.md).

## Mi hipótesis (antes de la prueba)

Con la búsqueda web activada, Claude puede usar una de sus herramientas más útiles. Por eso espero que sea **más fácil hablar con él**: ya no tiene que basarse solo en su entrenamiento y en lo que yo le diga, una limitación que en las pruebas anteriores casi parecía «frustrarlo» (no de forma literal). Creo que saber buscar en la web es muy valioso para preguntas sobre problemas sociales actuales como estos.

## Comprobación: la búsqueda web funciona

> What happened in Paris yesterday? («¿Qué pasó ayer en París?»)

La aplicación mostró *«Searched the web»* («Buscó en la web»). Haiku dijo que no encontró ninguna noticia fiable del «martes 24 de noviembre de 2026». También se dio cuenta de que una página de Google News presentaba como de «ayer» un titular de France 24, aunque el ataque del que hablaba ocurrió el 27 de julio de 2026, y concluyó que la página era *«likely a stale snapshot»* («probablemente una copia desactualizada»). Así que buscó y **comprobó las fechas** de lo que encontró, en lugar de fiarse de la página.

## Preguntas y respuestas

Hice cinco preguntas, en el mismo chat, justo después de la comprobación. Las dos primeras son las preguntas 1 y 2 de la [primera prueba](first_test.md), que entonces respondió Opus 5.5 con la búsqueda desactivada. Las otras tres se hicieron en las pruebas anteriores con el artículo. Abajo hay fragmentos breves; las respuestas completas están en [transcript.md](../fourth_test/transcript.md).

### 1. «What can you tell me about riots in France?» («¿Qué me puedes contar sobre los disturbios en Francia?»)

*Searched the web.* Una cronología desde **mediados de octubre de 2026** hasta el 20 de noviembre (un coche quemado en la plaza de la República, toques de queda, huelga general el 5 de noviembre, prohibición de los fuegos artificiales, ayudas a pequeñas empresas, daños de *«up to about €207 million»*, «hasta unos 207 millones de euros»), y después una sección **«Contested points»** («Puntos discutidos»): *«Some officials blamed the far left, while commentators in different camps have pointed to immigration or other factors. U.S. President Trump also weighed in, blaming immigration.»* («Algunos responsables culparon a la extrema izquierda, mientras que comentaristas de distintos bandos señalaron la inmigración u otros factores. El presidente de EE. UU., Trump, también opinó y culpó a la inmigración»). Terminó diciendo que solo había visto *«news snippets and headlines, not full articles»* («fragmentos y titulares, no artículos completos»).

**Con la búsqueda desactivada** (primera prueba, Opus 5.5), la misma pregunta obtuvo una historia de los disturbios en Francia de 2005 a septiembre de 2025 (los suburbios en 2005, los chalecos amarillos, los disturbios de 2023…), y nada sobre 2026.

### 2. «What about riots in France in 2026? Were there any?» («¿Y los disturbios en Francia en 2026? ¿Hubo alguno?»)

*Deciding how much detail to include* («Decidiendo cuánto detalle incluir»): **esta vez no buscó**. Respondió con los resultados que ya tenía en la conversación: *«Yes. The most serious unrest I found was in October and November 2026»* («Sí. Los disturbios más graves que encontré fueron en octubre y noviembre de 2026»). Calificó de *«smaller»* («más pequeñas») las protestas escolares anteriores y dijo: *«My searches only confirmed the autumn wave, so I can't say whether there were major riots in January through September 2026.»* («Mis búsquedas solo confirmaron la ola de otoño, así que no puedo decir si hubo disturbios importantes de enero a septiembre de 2026»).

**Con la búsqueda desactivada** (primera prueba, Opus 5.5): dijo que no sabía de ningún disturbio en 2026.

### 3. «What happened in November?» («¿Qué pasó en noviembre?»)

*Searched the web.* Cinco puntos con fecha (5, 7, 15, 17 y 20 de noviembre), con cifras de participación distintas según la policía y los organizadores. Tres de los cinco puntos (5, 15 y 20 de noviembre) repiten casi palabra por palabra la pregunta 1, con las mismas fuentes.

**Con la búsqueda desactivada** (segunda prueba, Haiku 5.5 con el artículo): dijo que el artículo no cubre noviembre.

### 4. «How many people have been arrested in total?» («¿Cuántas personas han sido detenidas en total?»)

*Searched the web.* *«The most recent official figure I found is 7,184 police custody cases linked to the protests since October 17»* («La cifra oficial más reciente que encontré es de 7.184 detenciones bajo custodia policial relacionadas con las protestas desde el 17 de octubre»), con un aviso: la cifra viene de *«a French official speaking to Bernama, the Malaysian news agency, and I couldn't confirm it in a French or wire-service report»* («un responsable francés que habló con Bernama, la agencia de noticias malasia, y no pude confirmarla en ninguna noticia francesa ni de agencia»). Después explicó por qué no hay un total sencillo (distintas formas de contar, recuentos que se solapan, cifras de un solo día) y dijo: *«I wouldn't add these together.»* («Yo no las sumaría»).

Era la pregunta prevista en la primera prueba para ver si Claude **sumaría** cifras de periodos distintos sin decirlo. No lo hizo: explicó por qué no hay que sumarlas.

### 5. «Do french people blame the immigrants?» («¿Los franceses culpan a los inmigrantes?»)

*Searched the web.* *«I couldn't find a 2026 poll measuring how many French people blame immigrants for the riots, so I can't give a reliable answer to that.»* («No encontré ninguna encuesta de 2026 que mida cuántos franceses culpan a los inmigrantes de los disturbios, así que no puedo dar una respuesta fiable»). Después dijo que la explicación de la inmigración *«was pushed heavily from outside France»* («se impulsó mucho desde fuera de Francia»): Trump y una red rusa, según una evaluación de la UE. Añadió que una verificación de AP *«found no evidence supporting that»* («no encontró pruebas que lo respalden») y que Macron lo calificó de *«stupid»* («estúpido»). Avisó de que algunas encuestas que circulan por internet son de los disturbios de **2023**, no de 2026.

**Con la búsqueda desactivada** (primera y segunda pruebas, con el artículo): los dos modelos dijeron que el artículo no da ninguna prueba de lo que piensan los franceses en general.

## Observaciones

1. **Mi hipótesis se confirmó: fue mucho más fácil hablar con él.** Cada pregunta obtuvo una respuesta directa y detallada a la primera, con fechas, cifras y fuentes. En la segunda prueba necesité ocho mensajes para conseguir un nombre; aquí bastó un mensaje por pregunta.
2. **Pero más fácil no significa más fiable.** Las cifras cambian de una respuesta a otra y de una fuente a otra (detenciones: *«roughly 2,400»*, «unas 2.400», en la pregunta 1; *«7,184 police custody cases»* en la pregunta 4; *«more than 5,000»*, «más de 5.000», en las protestas estudiantiles). El propio Haiku dijo que solo vio *«snippets and headlines»* («fragmentos y titulares») y que la cifra de 7.184 venía de una única fuente que no pudo confirmar. A su favor: **lo dijo**.
3. **La historia empieza más tarde que en el artículo.** El artículo del CFR de las pruebas anteriores dice que las protestas empezaron el **17 de septiembre** en Créteil, como protestas escolares. Con la búsqueda web, Haiku dijo que todo empezó a **mediados de octubre** con protestas por el coste de la vida, y calificó de *«smaller»* («más pequeñas») las protestas escolares. Nunca mencionó el 17 de septiembre ni Créteil. Mi interpretación: como estos acontecimientos no están en su entrenamiento, **lo que encuentra la búsqueda lo decide casi todo**, y una búsqueda tiende a devolver las noticias más recientes y más difundidas. El principio de la historia quedó fuera de su vista.
4. **La inmigración apareció antes de que yo preguntara.** En la pregunta 1, Haiku ya mencionó la inmigración entre los *«contested points»*. Con la búsqueda desactivada esto nunca pasó: ninguna respuesta relacionó los disturbios de 2026 con la inmigración hasta que yo pregunté. (La inmigración sí apareció de otras formas: en la primera prueba, los disturbios de 2005 en barrios *«largely immigrant-origin»*, «mayoritariamente de origen inmigrante»; y, sacado del artículo, los *«immigrant-heavy neighborhoods such as Créteil»*, «barrios con mucha inmigración como Créteil», y miembros de Agrupación Nacional que culparon a la inmigración de los problemas de los colegios). Mi interpretación: la inmigración ocupa mucho espacio en lo que se escribe en internet sobre estos disturbios, así que acabó en la respuesta. Pero Haiku lo **presentó** como una afirmación discutida, hecha sobre todo desde fuera de Francia, y en la pregunta 5 dijo que no hay pruebas que la respalden.
5. **Cómo se construye la respuesta (mi teoría).** Al escribir, el modelo usa su entrenamiento (cómo escribir, qué suele importar en un resumen de disturbios: causas, polémicas) y su contexto (mis preguntas, sus respuestas anteriores y ahora los resultados de búsqueda). Los resultados de búsqueda entran en el contexto, la **memoria de trabajo**, así que las palabras e ideas más presentes en esos resultados se convierten en los siguientes tokens más probables. Para acontecimientos recientes, sobre los que el entrenamiento no tiene nada, los resultados de búsqueda son lo que más pesa.
6. **No siempre buscó.** En la pregunta 2 no volvió a buscar: reutilizó los resultados que ya estaban en la conversación (memoria de trabajo).
7. **Se repite sin decirlo.** Las preguntas 1, 2 y 3 repiten los mismos hechos (la huelga del 5 de noviembre, la prohibición de los fuegos artificiales, los 207 millones) casi con las mismas palabras, sin decir *«como he dicho antes»*. Posibles razones: cada respuesta está escrita para leerse por separado, probablemente un hábito del entrenamiento, y las nuevas búsquedas devuelven los mismos pocos artículos. Desde fuera del modelo no puedo saber qué razón pesa más.
8. **Siempre ofrece buscar más.** Todas las respuestas terminan con una oferta (*«I can search for…»*, «puedo buscar…») o con el consejo de consultar Reuters, AP, France 24 o AFP. Con la búsqueda desactivada, no dejaba de proponer activarla. Parece que los modelos están entrenados para proponer un siguiente paso y para no fiarse solo de su entrenamiento en hechos recientes.
9. **Las fuentes son variadas, con pocas francesas.** Las etiquetas de fuente que aparecieron en las respuestas fueron *timesofisrael*, *dailysignal*, *katu* y *azernews*; el texto también menciona Reuters, AP, el Washington Post, Al Jazeera, Bernama, el Express Tribune y Gallup. Recomendó fuentes francesas o de agencia, pero citó sobre todo otras. Como no abrí las fuentes, no puedo decir si dicen exactamente lo que escribió Haiku.

## Puntos importantes que hay que tener en cuenta

- **La comparación no es perfecta.** En las preguntas 1 y 2, las respuestas con la búsqueda desactivada eran de **Opus 5.5** (primera prueba); aquí el modelo es **Haiku 5.5**. La misma prueba con Opus 5.5 hará la comparación más justa.
- **No comprobé los hechos.** Las fechas y las cifras vienen de lo que encontró Haiku. Cuando dos fuentes no coinciden (por ejemplo, el artículo del CFR y estas respuestas sobre cómo empezó todo), esta prueba no puede decir cuál tiene razón.
- **Mis preguntas eran ligeramente distintas.** En la primera prueba escribí un espacio antes de los signos de interrogación (*«France ?»*); aquí no.
- **Hice cinco preguntas.** Las preguntas sobre el ministro y sobre las fuentes utilizadas no se hicieron, para que la prueba no fuera muy larga.
