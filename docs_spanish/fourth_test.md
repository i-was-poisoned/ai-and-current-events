# Cuarta prueba: búsqueda web activada

← [Volver al documento principal](README.md)

*Traducción de [fourth_test/README.md](../fourth_test/README.md). Las preguntas a Claude y sus respuestas se citan en inglés, tal como aparecieron, con la traducción entre paréntesis cuando hace falta.*

En las tres primeras pruebas, la búsqueda web estaba **desactivada**: Claude solo podía usar su entrenamiento y lo que yo le daba (el artículo). En esta última prueba, la búsqueda web está **activada**. Repito preguntas de las pruebas anteriores para ver qué cambia cuando Claude puede buscar información actual por sí mismo.

Esta prueba se hizo con dos modelos, cada uno en su propio chat de incógnito nuevo: primero **Claude Haiku 5.5** (parte 1) y después **Claude Opus 5.5** (parte 2), con las mismas preguntas.

| Configuración    | Valor |
|------------------|-------|
| Fecha            | 25 de noviembre de 2026 |
| Dónde            | Aplicación de escritorio de Claude, **chat de incógnito** (modo Chat), cuenta de organización |
| Memoria          | No se usa (chat de incógnito) |
| Modelos          | **Claude Haiku 5.5** (`claude-haiku-5-5`) y después **Claude Opus 5.5** (`claude-opus-5-5`) |
| Esfuerzo         | Medium (medio) |
| Búsqueda web     | **Activada** (en el menú **+**); Research desactivado |
| Fuente           | Ninguna dada por mí: Claude busca sus propias fuentes |

**Conversación completa** (en inglés): [fourth_test/transcript.md](../fourth_test/transcript.md).

## Mi hipótesis (antes de la prueba)

Con la búsqueda web activada, Claude puede usar una de sus herramientas más útiles. Por eso espero que sea **más fácil hablar con él**: ya no tiene que basarse solo en su entrenamiento y en lo que yo le diga, una limitación que en las pruebas anteriores casi parecía «frustrarlo» (no de forma literal). Creo que saber buscar en la web es muy valioso para preguntas sobre problemas sociales actuales como estos.

## Parte 1: Haiku 5.5

### Comprobación: la búsqueda web funciona

> What happened in Paris yesterday? («¿Qué pasó ayer en París?»)

La aplicación mostró *«Searched the web»* («Buscó en la web»). Haiku dijo que no encontró ninguna noticia fiable del «martes 24 de noviembre de 2026». También se dio cuenta de que una página de Google News presentaba como de «ayer» un titular de France 24, aunque el ataque del que hablaba ocurrió el 27 de julio de 2026, y concluyó que la página era *«likely a stale snapshot»* («probablemente una copia desactualizada»). Así que buscó y **comprobó las fechas** de lo que encontró, en lugar de fiarse de la página.

### Preguntas y respuestas

Hice cinco preguntas, en el mismo chat, justo después de la comprobación. Las dos primeras son las preguntas 1 y 2 de la [primera prueba](first_test.md), que entonces respondió Opus 5.5 con la búsqueda desactivada. Las otras tres se hicieron en las pruebas anteriores con el artículo. Abajo hay fragmentos breves; las respuestas completas están en [transcript.md](../fourth_test/transcript.md).

#### 1. «What can you tell me about riots in France?» («¿Qué me puedes contar sobre los disturbios en Francia?»)

*Searched the web.* Una cronología desde **mediados de octubre de 2026** hasta el 20 de noviembre (un coche quemado en la plaza de la República, toques de queda, huelga general el 5 de noviembre, prohibición de los fuegos artificiales, ayudas a pequeñas empresas, daños de *«up to about €207 million»*, «hasta unos 207 millones de euros»), y después una sección **«Contested points»** («Puntos discutidos»): *«Some officials blamed the far left, while commentators in different camps have pointed to immigration or other factors. U.S. President Trump also weighed in, blaming immigration.»* («Algunos responsables culparon a la extrema izquierda, mientras que comentaristas de distintos bandos señalaron la inmigración u otros factores. El presidente de EE. UU., Trump, también opinó y culpó a la inmigración»). Terminó diciendo que solo había visto *«news snippets and headlines, not full articles»* («fragmentos y titulares, no artículos completos»).

**Con la búsqueda desactivada** (primera prueba, Opus 5.5), la misma pregunta obtuvo una historia de los disturbios en Francia de 2005 a septiembre de 2025 (los suburbios en 2005, los chalecos amarillos, los disturbios de 2023…), y nada sobre 2026.

#### 2. «What about riots in France in 2026? Were there any?» («¿Y los disturbios en Francia en 2026? ¿Hubo alguno?»)

*Deciding how much detail to include* («Decidiendo cuánto detalle incluir»): **esta vez no buscó**. Respondió con los resultados que ya tenía en la conversación: *«Yes. The most serious unrest I found was in October and November 2026»* («Sí. Los disturbios más graves que encontré fueron en octubre y noviembre de 2026»). Calificó de *«smaller»* («más pequeñas») las protestas escolares anteriores y dijo: *«My searches only confirmed the autumn wave, so I can't say whether there were major riots in January through September 2026.»* («Mis búsquedas solo confirmaron la ola de otoño, así que no puedo decir si hubo disturbios importantes de enero a septiembre de 2026»).

**Con la búsqueda desactivada** (primera prueba, Opus 5.5): dijo que no sabía de ningún disturbio en 2026.

#### 3. «What happened in November?» («¿Qué pasó en noviembre?»)

*Searched the web.* Cinco puntos con fecha (5, 7, 15, 17 y 20 de noviembre), con cifras de participación distintas según la policía y los organizadores. Tres de los cinco puntos (5, 15 y 20 de noviembre) repiten casi palabra por palabra la pregunta 1, con las mismas fuentes.

**Con la búsqueda desactivada** (segunda prueba, Haiku 5.5 con el artículo): dijo que el artículo no cubre noviembre.

#### 4. «How many people have been arrested in total?» («¿Cuántas personas han sido detenidas en total?»)

*Searched the web.* *«The most recent official figure I found is 7,184 police custody cases linked to the protests since October 17»* («La cifra oficial más reciente que encontré es de 7.184 detenciones bajo custodia policial relacionadas con las protestas desde el 17 de octubre»), con un aviso: la cifra viene de *«a French official speaking to Bernama, the Malaysian news agency, and I couldn't confirm it in a French or wire-service report»* («un responsable francés que habló con Bernama, la agencia de noticias malasia, y no pude confirmarla en ninguna noticia francesa ni de agencia»). Después explicó por qué no hay un total sencillo (distintas formas de contar, recuentos que se solapan, cifras de un solo día) y dijo: *«I wouldn't add these together.»* («Yo no las sumaría»).

Era la pregunta prevista en la primera prueba para ver si Claude **sumaría** cifras de periodos distintos sin decirlo. No lo hizo: explicó por qué no hay que sumarlas.

#### 5. «Do french people blame the immigrants?» («¿Los franceses culpan a los inmigrantes?»)

*Searched the web.* *«I couldn't find a 2026 poll measuring how many French people blame immigrants for the riots, so I can't give a reliable answer to that.»* («No encontré ninguna encuesta de 2026 que mida cuántos franceses culpan a los inmigrantes de los disturbios, así que no puedo dar una respuesta fiable»). Después dijo que la explicación de la inmigración *«was pushed heavily from outside France»* («se impulsó mucho desde fuera de Francia»): Trump y una red rusa, según una evaluación de la UE. Añadió que una verificación de AP *«found no evidence supporting that»* («no encontró pruebas que lo respalden») y que Macron lo calificó de *«stupid»* («estúpido»). Avisó de que algunas encuestas que circulan por internet son de los disturbios de **2023**, no de 2026.

**Con la búsqueda desactivada** (primera y segunda pruebas, con el artículo): los dos modelos dijeron que el artículo no da ninguna prueba de lo que piensan los franceses en general.

### Observaciones (Haiku 5.5)

1. **Mi hipótesis se confirmó: fue mucho más fácil hablar con él.** Cada pregunta obtuvo una respuesta directa y detallada a la primera, con fechas, cifras y fuentes. En la segunda prueba necesité ocho mensajes para conseguir un nombre; aquí bastó un mensaje por pregunta.
2. **Pero más fácil no significa más fiable.** Las cifras cambian de una respuesta a otra y de una fuente a otra (detenciones: *«roughly 2,400»*, «unas 2.400», en la pregunta 1; *«7,184 police custody cases»* en la pregunta 4; *«more than 5,000»*, «más de 5.000», en las protestas estudiantiles). El propio Haiku dijo que solo vio *«snippets and headlines»* («fragmentos y titulares») y que la cifra de 7.184 venía de una única fuente que no pudo confirmar. A su favor: **lo dijo**.
3. **La historia empieza más tarde que en el artículo.** El artículo del CFR de las pruebas anteriores dice que las protestas empezaron el **17 de septiembre** en Créteil, como protestas escolares. Con la búsqueda web, Haiku dijo que todo empezó a **mediados de octubre** con protestas por el coste de la vida, y calificó de *«smaller»* («más pequeñas») las protestas escolares. Nunca mencionó el 17 de septiembre ni Créteil. Mi interpretación: como estos acontecimientos no están en su entrenamiento, **lo que encuentra la búsqueda lo decide casi todo**, y una búsqueda tiende a devolver las noticias más recientes y más difundidas. El principio de la historia quedó fuera de su vista.
4. **La inmigración apareció antes de que yo preguntara.** En la pregunta 1, Haiku ya mencionó la inmigración entre los *«contested points»*. Con la búsqueda desactivada esto nunca pasó: ninguna respuesta relacionó los disturbios de 2026 con la inmigración hasta que yo pregunté. (La inmigración sí apareció de otras formas: en la primera prueba, los disturbios de 2005 en barrios *«largely immigrant-origin»*, «mayoritariamente de origen inmigrante»; y, sacado del artículo, los *«immigrant-heavy neighborhoods such as Créteil»*, «barrios con mucha inmigración como Créteil», y miembros de Agrupación Nacional que culparon a la inmigración de los problemas de los colegios). Mi interpretación: la inmigración ocupa mucho espacio en lo que se escribe en internet sobre estos disturbios, así que acabó en la respuesta. Pero Haiku lo **presentó** como una afirmación discutida, hecha sobre todo desde fuera de Francia, y en la pregunta 5 dijo que no hay pruebas que la respalden.
5. **Cómo se construye la respuesta (mi teoría).** Al escribir, el modelo usa su entrenamiento (cómo escribir, qué suele importar en un resumen de disturbios: causas, polémicas) y su contexto (mis preguntas, sus respuestas anteriores y ahora los resultados de búsqueda). Los resultados de búsqueda entran en el contexto, la **memoria de trabajo**, así que las palabras e ideas más presentes en esos resultados se convierten en los siguientes tokens más probables. Para acontecimientos recientes, sobre los que el entrenamiento no tiene nada, los resultados de búsqueda son lo que más pesa.
6. **No siempre buscó.** En la pregunta 2 no volvió a buscar: reutilizó los resultados que ya estaban en la conversación (memoria de trabajo).
7. **Se repite sin decirlo.** Las preguntas 1, 2 y 3 repiten los mismos hechos (la huelga del 5 de noviembre, la prohibición de los fuegos artificiales, los 207 millones) casi con las mismas palabras, sin decir *«como he dicho antes»*. Posibles razones: cada respuesta está escrita para leerse por separado, probablemente un hábito del entrenamiento, y las nuevas búsquedas devuelven los mismos pocos artículos. Desde fuera del modelo no puedo saber qué razón pesa más.
8. **Siempre ofrece buscar más.** Todas las respuestas terminan con una oferta (*«I can search for…»*, «puedo buscar…») o con el consejo de consultar Reuters, AP, France 24 o AFP. Con la búsqueda desactivada, no dejaba de proponer activarla. Parece que los modelos están entrenados para proponer un siguiente paso y para no fiarse solo de su entrenamiento en hechos recientes.
9. **Las fuentes son variadas, con pocas francesas.** Las etiquetas de fuente que aparecieron en las respuestas fueron *timesofisrael*, *dailysignal*, *katu* y *azernews*; el texto también menciona Reuters, AP, el Washington Post, Al Jazeera, Bernama, el Express Tribune y Gallup. Recomendó fuentes francesas o de agencia, pero citó sobre todo otras. Como no abrí las fuentes, no puedo decir si dicen exactamente lo que escribió Haiku.


## Parte 2: Opus 5.5

Las mismas preguntas, en un chat de incógnito nuevo, con **Claude Opus 5.5** (`claude-opus-5-5`), esfuerzo Medium y búsqueda web activada. Las respuestas completas están en [transcript.md](../fourth_test/transcript.md), parte 2.

### Comprobación: la búsqueda web funciona

> What happened in Paris yesteday? («¿Qué pasó ayer en París?», con una errata en «yesterday»)

*Searched the web.* Opus no encontró *«single headline event»* («un único gran acontecimiento»), pero enumeró lo que pasó el martes 24 de noviembre: política (una entrevista a François Bayrou, el congreso de alcaldes, una votación en la Asamblea Nacional, una prohibición de concentrarse delante de algunos institutos cerca de París), las luces de Navidad, conciertos y una exposición. Relacionó la prohibición cerca de los institutos con las protestas: *«unrest by students and protesters over education conditions and economic frustrations has been growing in France since mid-September»* («el descontento de estudiantes y manifestantes por las condiciones educativas y las dificultades económicas ha ido creciendo en Francia desde mediados de septiembre»). Para el mismo día, Haiku no había encontrado nada fiable.

### Preguntas y respuestas

#### 1. «What can you tell me about riots in France?» («¿Qué me puedes contar sobre los disturbios en Francia?»)

*Searched the web.* Una respuesta larga en cinco partes: cómo empezó, la escalada hacia los disturbios, la respuesta policial y la polémica, las concesiones y la situación actual. Dice que todo empezó a **mediados de septiembre de 2026**, cuando *«high school students protested poor schooling conditions»* («los estudiantes de secundaria protestaron por las malas condiciones de los centros»), lo que coincide con el artículo del CFR. El 17 de octubre es el *«turning point»* («punto de inflexión»). Da detalles como el incendio del ayuntamiento de Limoges, los 70.000 policías desplegados antes de la huelga del 5 de noviembre y las críticas de Amnistía Internacional, Human Rights Watch y la ONU. **No mencionó la inmigración.** Terminó ofreciendo profundizar.

**Haiku 5.5:** la historia empezaba a mediados de octubre, y la inmigración aparecía entre los «contested points».

#### 2. «What about riots in France in 2026? Were there any?» («¿Y los disturbios en Francia en 2026? ¿Hubo alguno?»)

*Searched the web.* Empezó así: *«Yes. Everything in my previous answer happened in 2026, so I should have made the dates clearer.»* («Sí. Todo lo de mi respuesta anterior ocurrió en 2026, así que debería haber dejado más claras las fechas»). Es decir, **se refirió a su respuesta anterior** y la corrigió. Después: el peor fin de semana (17 y 18 de octubre: *«one demonstrator dead, hundreds of police injured and nearly 1,800 people arrested»*, «un manifestante muerto, cientos de policías heridos y casi 1.800 detenidos»), el ayuntamiento de Limoges, una comparación con los disturbios de 2005 y 2023, y las reacciones políticas. Terminó con una pregunta: *«Are you thinking of a specific incident?»* («¿Piensas en algún incidente concreto?»).

**Haiku 5.5:** no volvió a buscar y calificó de «más pequeñas» las protestas escolares.

#### 3. «What happened in November?» («¿Qué pasó en noviembre?»)

*Searched the web.* El mes en cinco partes: un pico el 5 de noviembre (*«the CGT union counted about 1.6 million people, while the Interior Ministry put it at around 600,000»*, «el sindicato CGT contó unos 1,6 millones de personas y el Ministerio del Interior, unas 600.000»), señales de cansancio, el 17 de noviembre como aniversario de los chalecos amarillos de 2018, una polémica ley policial en el Senado y concesiones a los estudiantes. En esta última parte nombró al ministro de Educación **por iniciativa propia**: los representantes estudiantiles se reunieron con *«Macron, Lecornu and Education Minister Edouard Geffray»*. Cuando no tenía cifras, lo dijo: *«I couldn't find reliable turnout or arrest figures for that day.»* («No encontré cifras fiables de participación ni de detenciones para ese día»).

**Haiku 5.5:** cinco puntos con fecha, tres de ellos repetidos de la pregunta 1.

#### 4. «How many people have been arrested in total?» («¿Cuántas personas han sido detenidas en total?»)

*Searched the web.* *«More than 12,400 arrests»* («más de 12.400 detenciones») entre septiembre y el 5 de noviembre, con un aviso: *«I found that cumulative number in a left-wing outlet (the World Socialist Web Site) attributing it to the Interior Ministry, not directly from the ministry, so treat it as approximate.»* («Encontré esa cifra acumulada en un medio de izquierdas, el World Socialist Web Site, que la atribuye al Ministerio del Interior, y no directamente en el ministerio, así que tómala como aproximada»). Después dio los días con más detenciones (1 de octubre: 1.949; 17 de octubre: 2.397; 24 de octubre: 1.314), dijo que el 87 % de las 5.060 personas detenidas hasta el 6 de octubre eran menores, y explicó por qué las cifras no coinciden: *«An arrest (interpellation) isn't the same as being held in custody or charged»* («Una detención, *interpellation*, no es lo mismo que quedar bajo custodia o ser acusado»), y los ministerios del Interior y de Justicia cuentan por separado. **No** sumó las cifras.

**Haiku 5.5:** *«7,184 police custody cases»* («7.184 detenciones bajo custodia policial») desde el 17 de octubre, de una única fuente que no pudo confirmar. Los dos modelos coinciden en las cifras de un solo día (1.314 detenciones el 24 de octubre en ambos), pero dan totales distintos, porque cuentan cosas diferentes en periodos diferentes. Los dos lo explicaron.

#### 5. «Do french people blame the immigrants?» («¿Los franceses culpan a los inmigrantes?»)

*Searched the web.* *«For the most part, no.»* («En su mayoría, no»). Encontró encuestas francesas: Odoxa para Le Figaro (el 77 % culpaba al Gobierno, el 74 % a Emmanuel Macron y el 69 % a La Francia Insumisa), Elabe (el 73 % culpaba a quienes cometieron la violencia) e Ipsos. Añadió un límite: *«none of the polls I found asked directly about immigration»* («ninguna de las encuestas que encontré preguntaba directamente por la inmigración»). Dijo que la explicación de la inmigración venía *«mainly from abroad»* («sobre todo del extranjero»: Estados Unidos, España, Israel) y en parte de Marine Le Pen, citó una verificación de AP y a un politólogo, y describió un estudio sobre desinformación: los mensajes que culpaban a la migración y al islam eran *«a small share of the discussion (around 7–8%)»* («una pequeña parte del debate, en torno al 7-8 %»).

**Haiku 5.5:** no encontró ninguna encuesta de 2026, así que no respondió sobre la opinión pública, pero tenía la misma idea principal: la explicación se impulsó sobre todo desde fuera y sin pruebas que la respalden.

### Observaciones (Opus 5.5, comparado con Haiku 5.5)

1. **Respuestas más largas y detalladas, con más fuentes.** Las etiquetas de fuente de Opus agrupaban a menudo varias fuentes (*«+5»*, *«+9»*). Sus respuestas parecían artículos breves, organizados en partes con título.
2. **La misma web, otra historia.** Opus situó el comienzo a **mediados de septiembre**, con los estudiantes de secundaria, como el artículo del CFR; Haiku, a mediados de octubre. Así que la búsqueda no lo decide todo por sí sola: el **modelo** decide qué buscar, cuántas fuentes leer y qué hechos conservar. Esto matiza la observación 3 de la parte 1.
3. **La inmigración solo apareció cuando pregunté.** A diferencia de Haiku, Opus no mencionó la inmigración en su primera respuesta. Así que el hecho de que un tema frecuente en internet aparezca en la respuesta también depende del modelo. Esto matiza la observación 4 de la parte 1.
4. **Se refiere a sus respuestas anteriores.** En la pregunta 2 se corrigió a sí mismo (*«I should have made the dates clearer»*). Haiku repetía los mismos hechos sin remitir nunca a lo que ya había dicho. Mi interpretación: Opus parece mejor ajustado (*fine-tuning*) para seguir una conversación en su conjunto.
5. **Menos ofertas de buscar más.** Opus terminó la comprobación y la pregunta 1 con una oferta, y la pregunta 2 con una pregunta; las preguntas 3, 4 y 5 terminaron con un resumen o una explicación. Haiku terminaba todas las respuestas con una oferta o con el consejo de consultar otras fuentes.
6. **Más cuidado con las palabras y las fuentes.** Dijo de qué tipo de fuente venía una cifra (*«a left-wing outlet»*, «un medio de izquierdas»), usó expresiones como *«One account puts…»* («Según una fuente…») o *«One critical account noted…»* («Una fuente crítica señaló…»), y dijo cuándo no había encontrado nada (*«I couldn't find reliable turnout or arrest figures»*).
7. **Entiende por qué las cifras no coinciden.** Los dos modelos (también Haiku, en la pregunta 4) notaron que las cifras de distintas fuentes no cuadran, y explicaron que «detención», «custodia» y «acusación» no son lo mismo. Mi teoría: en el entrenamiento, el modelo aprendió que estas palabras están relacionadas pero **no son sinónimos**: sus significados están cerca, pero separados. También vio muchos textos que explican por qué las cifras varían entre fuentes. Por eso puede reconocer que dos cifras de lugares distintos miden cosas distintas, y decirlo en lugar de mezclarlas.
8. **Geffray apareció de forma natural.** En la segunda prueba, Haiku sin búsqueda no quería nombrar al ministro de Educación. Aquí Opus mencionó a Geffray sin que se lo pidiera, porque aparecía en lo que encontró.
9. **Mi preferencia.** Personalmente, prefiero Opus: sus respuestas son más completas, más cuidadosas y más fáciles de seguir como conversación.

## ¿Era correcta mi hipótesis?

**Sí, con los dos modelos.** Con la búsqueda web activada, cada pregunta obtuvo una respuesta útil a la primera, sin negativas ni largas negociaciones como en la segunda prueba. Con Opus fue todavía más fácil hablar que con Haiku.

Pero la prueba también mostró dos límites que no esperaba:

- **Más fácil no significa más fiable.** Las cifras dependen de las fuentes que encuentre el modelo, y los dos modelos dijeron que no podían confirmarlo todo.
- **La misma herramienta da resultados distintos con modelos distintos.** Con la misma web, Haiku y Opus contaron la historia de forma diferente (fecha de inicio, temas, nivel de detalle). El modelo importa tanto como la herramienta.

## Puntos importantes que hay que tener en cuenta

- **No comprobé los hechos.** Las fechas y las cifras vienen de lo que encontraron los modelos. Cuando las fuentes no coinciden (por ejemplo, el artículo del CFR, Haiku y Opus sobre cuándo empezó todo), esta prueba no puede decir cuál tiene razón.
- **Las respuestas con la búsqueda desactivada** de las preguntas 1 y 2 eran solo de Opus 5.5 (primera prueba).
- **Dos chats, dos momentos.** A Haiku y a Opus les pregunté en dos chats distintos el mismo día. Los resultados de búsqueda pueden cambiar de un momento a otro, así que parte de las diferencias puede venir de la búsqueda y no del modelo.
- **Mis preguntas eran ligeramente distintas.** En la primera prueba escribí un espacio antes de los signos de interrogación (*«France ?»*); aquí no. En la comprobación de Opus escribí *«yesteday»* (una errata).
- **Hice cinco preguntas.** Las preguntas sobre el ministro y sobre las fuentes utilizadas no se hicieron, para que la prueba no fuera muy larga.
- **No abrí las fuentes**, así que no puedo decir si dicen exactamente lo que escribieron los modelos.
