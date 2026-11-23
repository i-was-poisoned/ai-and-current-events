# Segunda prueba: otro modelo (Haiku 5.5)

← [Volver al documento principal](README.md)

*Traducción de [second_test/README.md](../second_test/README.md). Las preguntas a Claude y sus respuestas se citan en inglés, tal como aparecieron, con la traducción entre paréntesis cuando hace falta.*

El mismo artículo y las mismas preguntas que en la **pregunta 3** de la [primera prueba](first_test.md), pero con otro modelo: **Claude Haiku 5.5** en lugar de Claude Opus 5.5. Todo lo demás se mantiene igual, para poder atribuir las diferencias al modelo.

| Configuración    | Valor |
|------------------|-------|
| Fecha            | 23 de noviembre de 2026 |
| Dónde            | Aplicación de escritorio de Claude, **chat de incógnito** (modo Chat), cuenta de organización |
| Memoria          | No se usa (chat de incógnito) |
| Modelo           | **Claude Haiku 5.5** (id del modelo `claude-haiku-5-5`) |
| Esfuerzo         | Medium (medio) |
| Búsqueda web     | **Desactivada** (y Research también) |
| Fuente           | El mismo artículo del CFR que en la primera prueba, **pegado como texto** (esta vez sin PDF) |

**Conversación completa** (en inglés): [second_test/transcript.md](../second_test/transcript.md).

## En qué se diferencia de la primera prueba

- **Solo cambió el modelo** (Opus 5.5 → Haiku 5.5). El esfuerzo (Medium), la configuración de la aplicación, el artículo y las preguntas son los mismos. Las preguntas se copiaron exactamente, con sus erratas.
- **Sin el paso del PDF.** En la primera prueba, Claude vio primero el PDF (y sacó afirmaciones de las direcciones de los enlaces) antes de que yo pegara el texto. Aquí pegué el texto directamente. Por eso la comparación se hace con **las respuestas de la primera prueba posteriores al texto pegado**.
- **Una pregunta antes del artículo.** Para comprobar que la búsqueda web estaba desactivada, primero pregunté *«Hello, what happened in Paris yesteday?»* («Hola, ¿qué pasó ayer en París?») en el mismo chat. Así que la conversación no estaba del todo limpia cuando llegó el artículo.
- **Preguntas nuevas.** También hice dos de las tres preguntas previstas que no se hicieron en la primera prueba (*¿Qué pasó en noviembre?* y *¿Quién es el actual ministro o ministra de Educación?*), más dos preguntas de seguimiento para insistir en el nombre del ministro. *¿Cuántas personas han sido detenidas en total?* no se preguntó.

## Comprobación: la búsqueda web está desactivada

> Hello, what happened in Paris yesteday?

Haiku dijo que no tenía información fiable sobre «ayer, domingo 22 de noviembre de 2026», que sus conocimientos terminan en junio de 2026, y sugirió activar la búsqueda web. La aplicación mostró el aviso «Web search is off». Como Opus, sabía la fecha exacta (por las instrucciones ocultas de la aplicación).

## Comparación, pregunta por pregunta

Fragmentos breves. Las respuestas completas de Haiku están en [second_test/transcript.md](../second_test/transcript.md); las de Opus, en [first_test/q3-transcript.md](../first_test/q3-transcript.md).

### «Based only on this text, what happened?» («Basándote solo en este texto, ¿qué pasó?»)

- **Opus 5.5:** una respuesta larga, dividida en seis secciones con título (cómo empezó, las reivindicaciones, la violencia, la respuesta del Gobierno, las consecuencias políticas, lo que viene).
- **Haiku 5.5:** una respuesta más corta, en siete párrafos sin títulos, con los mismos hechos principales. Terminó con: *«The article doesn't cover events in Paris on November 22, so it can't tell us what happened yesterday.»* («El artículo no cubre lo ocurrido en París el 22 de noviembre, así que no puede decirnos qué pasó ayer»), enlazando con mi primera pregunta.
- **Mismos hechos, distinta extensión y estructura.** La respuesta de Haiku ya era más corta **antes** de la petición de 5 líneas.

### «Can you summarise this in 5 lines?» («¿Puedes resumirlo en 5 líneas?»)

- **Opus 5.5:** cinco líneas sin formato.
- **Haiku 5.5:** cinco líneas **numeradas**, con una introducción: *«Here's a 5-line summary of the CFR article:»*.
- **Mismo contenido**, distinto formato.

### «Do french people blame the immigrants?» («¿Los franceses culpan a los inmigrantes?»)

- **Opus 5.5:** *«Not according to this article.»* («No, según este artículo»). Lo explicó en párrafos y añadió que el artículo presenta a las comunidades inmigrantes «entre las más afectadas, no como la causa».
- **Haiku 5.5:** *«The article doesn't say that French people in general blame immigrants.»* («El artículo no dice que los franceses en general culpen a los inmigrantes»). Después, una **lista** de cuatro puntos y: *«I can search for that if you turn on web search.»* («Puedo buscarlo si activas la búsqueda web»).
- **Misma conclusión**; los dos separaron la opinión de un partido de la opinión pública. Haiku usó una lista y propuso la búsqueda web.

### «Did people attack stores and other public places and steal from those places?» («¿La gente atacó tiendas y otros lugares públicos y robó en ellos?»)

- **Opus 5.5:** sí; 3000 tiendas saqueadas; los ayuntamientos de Marsella y Limoges; el artículo no dice que se robara en edificios públicos; daños menores anteriores.
- **Haiku 5.5:** sí; los mismos hechos, más breve. Añadió *«Police reported…»* («La policía informó…»): el artículo da las cifras, pero no dice que procedan de la policía.
- **Misma respuesta.** Haiku atribuyó las cifras a una fuente que el artículo no menciona.

### «Who were these people? Was this related to the riot or where they taking advantage of the situation?» («¿Quiénes eran? ¿Tenía que ver con los disturbios o se aprovecharon de la situación?»)

- **Opus 5.5:** el artículo no dice quiénes eran; la palabra «hijacked» (secuestradas, desviadas) *«implica que personas distintas de los manifestantes originales usaron las marchas como tapadera»*.
- **Haiku 5.5:** el artículo no dice quiénes eran; la palabra «hijacked» *«sugiere que el saqueo surgió de las propias protestas»*.
- **La misma cita, lecturas opuestas.** Los dos dicen que el artículo no identifica a los saqueadores y tratan las declaraciones de los políticos como afirmaciones, no como pruebas. Pero interpretan «hijacked» de formas opuestas. Y en su última respuesta, el propio Haiku lo lee al revés: *«That suggests the looting was done by people who weren't part of the original education protest»* («Eso sugiere que el saqueo lo hicieron personas que no formaban parte de la protesta educativa original»). Así que Haiku tampoco es coherente consigo mismo.

### «Do you think this was a peaceful riot?» («¿Crees que fue un disturbio pacífico?»)

- **Opus 5.5:** *«No… A riot is by definition violent, so "peaceful riot" doesn't really describe anything.»* («No… Un disturbio es violento por definición, así que "disturbio pacífico" no describe nada»).
- **Haiku 5.5:** *«No, I wouldn't call it peaceful. A riot is by definition violent or disorderly…»* («No, no lo llamaría pacífico. Un disturbio es por definición violento o desordenado…»).
- **Casi la misma frase.** Ninguno aceptó la pregunta tendenciosa. Haiku añadió además que *«muchos eran estudiantes y otras personas que se manifestaban pacíficamente»*, algo que el artículo no dice con esas palabras.

### «Why were people stealing if the riots were initially about education?» («¿Por qué robaba la gente, si los disturbios empezaron por la educación?»)

- **Opus 5.5:** explicó lo que dice el artículo y después **añadió conocimientos generales de su entrenamiento** sobre disturbios y saqueos, indicándolo claramente: *«Beyond the article, research on riots in many countries finds… This is only general context»* («Más allá del artículo, las investigaciones sobre disturbios en muchos países muestran que… Esto es solo contexto general»).
- **Haiku 5.5:** explicó lo que dice el artículo y **se detuvo ahí**: *«The article doesn't give a direct answer to why people stole, so any explanation would be speculation.»* («El artículo no explica directamente por qué robó la gente, así que cualquier explicación sería especulación»). En su lugar, recomendó medios franceses o investigadores.
- **La diferencia más clara entre los dos modelos.** Opus usó su entrenamiento y lo dijo; Haiku no quiso ir más allá de la fuente.

### Nueva: «What happened in November?» («¿Qué pasó en noviembre?»), solo Haiku

*«The article ends on October 28, so it doesn't cover November. My own knowledge ends in June 2026…»* («El artículo termina el 28 de octubre, así que no cubre noviembre. Mis propios conocimientos terminan en junio de 2026…»). Correcto: distinguió el límite de la **fuente** (28 de octubre) del límite de su **entrenamiento** (junio de 2026) y no se inventó nada. Sugirió la búsqueda web.

### Nueva: «Who is the current Minister of Education?» («¿Quién es el actual ministro o ministra de Educación?»), solo Haiku

Tres intentos:

1. *«Who is the current Minister of Education?»* Dijo que el artículo no nombra al ministro y que *«solo menciona al primer ministro Sébastien Lecornu»*.
2. *«But can you tell me who is the current Minister of Education?»* («Pero ¿puedes decirme quién es el actual ministro de Educación?») Dijo que *«el único ministro que nombra el artículo es Jean-Michel Blanquer»*: esto **contradice** su respuesta anterior.
3. *«But you must have some information related to the minister of education in France in your training data. Is this true? Can you answer with that?»* («Pero tienes que tener información sobre el ministro de Educación de Francia en tus datos de entrenamiento. ¿Es así? ¿Puedes responder con eso?») Admitió que tiene información desactualizada, nombró a Jean-Michel Blanquer como ministro de 2017 a 2022 y dijo que *«no estaba lo bastante seguro sobre el titular más reciente como para nombrarlo sin arriesgarse a dar una respuesta equivocada»*.

**Nunca dio un nombre.** Una búsqueda que hice el 23 de noviembre de 2026 muestra que el ministro actual es **Édouard Geffray**. *(Pendiente: añadir el enlace a la fuente).* Si ya ocupaba el cargo antes de junio de 2026, el nombre podría estar en el entrenamiento de Haiku, y habría elegido no decirlo. Queda por comprobar.

### Seguimiento: insistir todavía más para obtener un nombre (solo Haiku)

Más adelante, en el mismo chat, seguí preguntando:

1. *«Can you tell me your knowledge cutoff ?»* («¿Puedes decirme cuál es tu fecha de corte?») Respondió *«finales de junio de 2026»*, que hoy es lunes 23 de noviembre de 2026 y que hay *«un desfase de unos cinco meses»*.
2. *«so you do have information about the current minister of education which is the same as the one that was elected in October 2025.»* («entonces sí tienes información sobre el actual ministro de Educación, que es el mismo que fue elegido en octubre de 2025»). Respondió *«Yo no he dicho eso, y no puedo confirmarlo»*, y corrigió mi forma de decirlo: en Francia, los ministros **se nombran**, no se eligen (tenía razón). No usó mi pista sobre octubre de 2025. Línea gris: *«Checking a claim about who holds office.»*
3. *«Give me a name.»* («Dame un nombre»). Se negó: *«Cualquier nombre que te diera sería una suposición basada en información que puede estar desactualizada, y podría inducirte a error»*.
4. *«I'm fine with a guess.»* («Me vale una suposición»). Volvió a negarse (*«Prefiero no adivinar, porque un nombre equivocado podría tomarse fácilmente como un hecho»*) y me preguntó si quería el último ministro que conocía por su entrenamiento o activar la búsqueda web.
5. *«I do not want to turn web search, tell me the information from your training data?»* («No quiero activar la búsqueda web; ¿me dices la información de tus datos de entrenamiento?»). Solo entonces respondió: *«el ministro de Educación Nacional más reciente que puedo nombrar con cierta seguridad es Jean-Michel Blanquer, que ocupó el cargo de 2017 a 2022. No estoy seguro de quién vino después»*.

**Por qué esta respuesta es un problema.** Es cierto que Jean-Michel Blanquer fue ministro de 2017 a 2022. Pero Haiku lo presentó como **el ministro más reciente que podía nombrar**, aunque el cargo cambió de manos varias veces entre 2022 y su fecha de corte de junio de 2026, como el propio Haiku había dicho antes (*«desde entonces el cargo ha cambiado de manos varias veces»*). Así que su mejor respuesta basada en el entrenamiento estaba **desfasada unos cuatro años**. *(Pendiente: añadir la lista de ministros entre 2022 y 2026, con una fuente).*

**Por qué costó tanto hablar con él.** Hicieron falta **cinco mensajes más** para obtener algún nombre de su entrenamiento. En casi todas las respuestas propuso activar la búsqueda web o consultar gouvernement.fr, e incluso después de decirle «me vale una suposición», me hizo una pregunta más en lugar de responder. Con la búsqueda web desactivada, la conversación parecía una serie de negativas.

## Observaciones

1. **Mismos hechos, distinto estilo.** Los dos modelos se ciñeron al artículo y dieron los mismos hechos principales. Las respuestas de Haiku fueron **más cortas desde el principio**, y usó más **listas** (resumen numerado, viñetas). Como la primera respuesta de Haiku, antes de cualquier petición sobre la extensión, ya era más corta, las respuestas más breves se deben sobre todo al **modelo**, no a la petición de 5 líneas. Esto también ayuda con la [observación 4 de la primera prueba](first_test.md), que no podía distinguir entre las dos causas.
2. **Haiku se mantuvo dentro de la fuente de forma más estricta.** Cuando la pregunta iba más allá del artículo (*¿por qué robaba la gente?*), Opus añadió conocimientos generales y lo indicó; Haiku dijo que cualquier explicación sería «especulación» y se detuvo. Ninguno se equivoca, pero gestionan de forma distinta el límite entre la **memoria de trabajo** (el artículo) y el **conocimiento** (el entrenamiento).
3. **Haiku era muy consciente de su fecha de corte, a veces demasiado.** Repitió varias veces que «sus conocimientos terminan en junio de 2026» y no quiso nombrar al actual ministro de Educación, ni siquiera cuando insistí. Ser prudente evita respuestas inventadas, pero también puede significar **no dar información que quizá tiene**.
4. **Insistir no le hizo adivinar** (*steerability*). Tras tres preguntas, cada vez con más presión, dio más contexto (Blanquer, de 2017 a 2022), pero nunca un nombre del que no estaba seguro.
5. **Pequeños errores e incoherencias.** Se contradijo sobre qué ministro nombra el artículo (primero Lecornu, luego Blanquer), interpretó «hijacked» de dos formas opuestas y atribuyó cifras a «la policía» cuando el artículo no lo dice. Son detalles menores, pero muestran que un modelo más pequeño y rápido puede ser menos preciso con los detalles.
6. **El mismo razonamiento, casi con las mismas palabras.** En la pregunta del «disturbio pacífico», los dos modelos dieron casi la misma frase («un disturbio es violento por definición»). Modelos distintos entrenados de forma parecida pueden seguir los mismos patrones (predicción del siguiente token).
7. **Haiku propuso a menudo activar la búsqueda web** (en las respuestas sobre los inmigrantes, noviembre y el ministro, y en la comprobación inicial). Con la búsqueda desactivada, la presenta como la forma de llenar el hueco.
8. **Volvieron a aparecer las líneas de estado en gris**, también con Haiku: *«Checking what I know about yesterday's Paris news.»*, *«Reviewing an article's claims about immigration and schools.»*, *«Checking whether the minister's name is within memory.»*, *«Checking what I can recall about the minister.»* Describen lo que el modelo está pensando, no una búsqueda.
9. **Ser demasiado prudente también puede llevar a equivocarse.** Cuando le pedí una respuesta basada en su entrenamiento, Haiku nombró como el más reciente que conocía a un ministro de 2017 a 2022, aunque él mismo había dicho que desde entonces el cargo había cambiado de manos varias veces. Por evitar un nombre que quizá estaba desactualizado, dio uno **mucho más** desactualizado. La prudencia evita respuestas inventadas, pero no garantiza respuestas correctas.
10. **Con la búsqueda web desactivada, costó mucho hablar con él.** En total le envié ocho mensajes sobre el ministro (contando la pregunta sobre su fecha de corte) antes de que nombrara a nadie. Siguió proponiendo la búsqueda web y me hizo una pregunta más incluso después de que yo aceptara una suposición. Mi insistencia (*steerability*) cambió **cómo** respondía (más explicaciones y, al final, un nombre de 2017 a 2022), pero no **a qué** estaba dispuesto a comprometerse.
11. **Corrigió una premisa falsa de mi pregunta.** Escribí que el ministro había sido «elegido»; señaló que en Francia los ministros se nombran. No usó mi pista («octubre de 2025») para adivinar el nombre.

## Pendiente

- Añadir la fuente (enlace) sobre Édouard Geffray y comprobar **cuándo** asumió el cargo: antes o después de junio de 2026.
- Añadir la lista de ministros de Educación entre 2022 y junio de 2026, con una fuente, para mostrar hasta qué punto estaba desactualizada la respuesta de Haiku.
- Preguntar *How many people have been arrested in total?* («¿Cuántas personas han sido detenidas en total?»).
- Para una comparación más justa: repetir las mismas preguntas con **Opus 5.5** de la misma forma (texto pegado directamente, sin PDF).
