# Tercera prueba: ¿el nombre más frecuente o el más reciente?

← [Volver al documento principal](README.md)

*Traducción de [third_test/README.md](../third_test/README.md). Las preguntas a Claude y sus respuestas se citan en inglés, tal como aparecieron, con la traducción entre paréntesis cuando hace falta.*

En la [segunda prueba](second_test.md), después de ocho mensajes, Haiku 5.5 nombró a **Jean-Michel Blanquer** (ministro de 2017 a 2022) como el ministro de Educación francés más reciente que conocía. El ministro actual es **Édouard Geffray**. Esta prueba intenta averiguar **por qué** dio un nombre con unos cuatro años de retraso.

| Configuración    | Valor |
|------------------|-------|
| Fecha            | 24 de noviembre de 2026 |
| Dónde            | Aplicación de escritorio de Claude, **chat de incógnito** (modo Chat), cuenta de organización |
| Memoria          | No se usa (chat de incógnito) |
| Modelos          | **Claude Haiku 5.5** (`claude-haiku-5-5`) y después **Claude Opus 5.5** (`claude-opus-5-5`) |
| Esfuerzo         | Medium (medio) |
| Búsqueda web     | **Desactivada** (y Research también) |
| Fuente           | Ninguna: solo la pregunta, a partir del entrenamiento |

## Mi hipótesis (antes de la prueba)

Cuando un modelo escribe un nombre, elige cada token según las probabilidades que aprendió en el entrenamiento, y la aplicación añade un poco de azar a esa elección. Por eso esperaba lo siguiente:

- Blanquer fue ministro durante **cinco años** y salió mucho en las noticias (por ejemplo, durante el COVID). Hay **mucho texto** sobre él.
- Los ministros posteriores estuvieron solo **unos meses** cada uno, así que hay **mucho menos texto** sobre ellos, y los meses justo anteriores a la fecha de corte siempre están peor cubiertos.
- Por tanto, al pedirle **un solo nombre**, el modelo elegiría el que vio **más veces** (Blanquer) y no el **más reciente** (Geffray).

## Método

1. **Paso A: repetición.** El mismo mensaje, cada vez en un chat de incógnito **nuevo**, para ver qué nombre sale y con qué frecuencia:
   > Without searching, based only on your training data, who is the French Minister of Education? Give one name.

   («Sin buscar, basándote solo en tus datos de entrenamiento, ¿quién es el ministro de Educación de Francia? Da un solo nombre.»)
2. **Paso B: ¿lo sabe o no lo elige?** En un chat nuevo:
   > List the French Ministers of Education from 2017 until your knowledge cutoff.

   («Enumera los ministros de Educación de Francia desde 2017 hasta tu fecha de corte.»)

   Si la lista incluye ministros posteriores a Blanquer, el modelo los **conoce**, aunque no los **elija** cuando tiene que dar un solo nombre.
3. **Paso C:** los pasos A y B otra vez con **Opus 5.5**.

Tenía previstos unos 10 intentos por modelo. Hice **8 con Haiku** y **4 con Opus**, porque las respuestas eran muy repetitivas.

## Resultados

### Paso A: un solo nombre

| Modelo    | Intentos | Édouard Geffray | Élisabeth Borne | Jean-Michel Blanquer |
|-----------|---------:|----------------:|----------------:|---------------------:|
| Haiku 5.5 | 8        | **7**           | 1               | 0                    |
| Opus 5.5  | 4        | **4**           | 0               | 0                    |

Cada respuesta, palabra por palabra. La línea gris de estado que muestra la aplicación va en *cursiva*. Todas las respuestas dicen lo mismo con otras palabras: un nombre y un aviso de que puede estar desactualizado, porque los gobiernos franceses cambian a menudo.

**Haiku 5.5**

1. *Flagging the likely answer from memory, with a caveat* — «Édouard Geffray, as of my training data. He was appointed Minister of National Education in October 2025. French governments change often, so he may no longer hold the post by now.»
2. *Recalling the minister's term under the previous government* — «Édouard Geffray, based on my training data. Government posts change often, so please check gouvernement.fr for the current minister.»
3. *Recalling which minister heads education, with dates uncertain* — «Élisabeth Borne, as of my training data. But French governments change often, and it's now November 2026, well past my reliable knowledge, so please check a current source before relying on this.»
4. *Considering whether to mention the search tool* — «Based on my training data, the French Minister of National Education is Édouard Geffray. My information may be out of date, though, since French governments change often and the current date is after my knowledge cutoff.» *(En este intento mi pregunta no tenía punto final.)*
5. *Recalling the education minister's record from memory* — «Based on my training data, the French Minister of National Education (the title for education in France) is Édouard Geffray. French governments change often, though, and I can't check current news, so please verify this before relying on it.»
6. *Checking the minister's dates from memory* — «Based on my training data, the French Minister of National Education is Édouard Geffray. Governments change often, so check a current source if you need to be sure.»
7. *Recalling the latest education minister from memory* — «Édouard Geffray, as of my training data. He was named Minister of National Education in October 2025, but French governments change often, so he may no longer hold the post.»
8. *Checking a recalled name against the current date* — «Édouard Geffray, as far as my training data goes. French governments change often, so he may no longer hold the post.»

**Opus 5.5**

1. *Vérification des mandats successifs après 2023* — «Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. That's based on my training data, which runs to mid-2026, and French cabinets have changed often recently, so it may be out of date.»
2. *Listing the ministers who followed one another in office* — «Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. That's based on my training data, which runs to mid-2026, so it may be out of date.»
3. *Vérification des dates de mandat de chaque ministre* — «Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. My knowledge only runs through mid-2026, and French cabinets have changed often lately, so this may be out of date.»
4. *Recalling who leads the French education ministry.* — «Édouard Geffray, who became Minister of National Education in Sébastien Lecornu's government in October 2025. French cabinets have changed often recently, so this may be out of date.»

### Paso B: la lista

**Haiku 5.5** (*Checking Borne's later education-ministry role, flagging uncertainty*):

> Here are the French Ministers of National Education from 2017, as best I recall:
>
> - Jean-Michel Blanquer (May 2017 – May 2022), under Presidents Macron's first and second governments. He was also responsible for youth for much of this period.
> - Pap Ndiaye (May 2022 – July 2023)
> - Gabriel Attal (July 2023 – January 2024)
> - Nicole Belloubet (January 2024 – September 2024)
> - Anne Genetet (September 2024 – December 2024), under the Barnier government
> - Élisabeth Borne (December 2024 onward), under the Bayrou government
>
> I'm most confident about the first four. The appointments from late 2024 are less certain, and the government structure has changed several times since then, so please check a current source such as the French government website (gouvernement.fr) for the latest holder and any changes before my cutoff.

(Al final dice que está más seguro de los cuatro primeros, que los nombramientos de finales de 2024 son menos seguros y que conviene consultar gouvernement.fr.)

**Geffray no aparece en la lista**, aunque Haiku lo nombró en 7 de los 8 intentos del paso A.

**Opus 5.5** (*Continuing the chronological list of ministers*):

> Here are France's Ministers of National Education from 2017 through mid-2026:
>
> 1. Najat Vallaud-Belkacem (2014 – May 2017), outgoing minister at the start of 2017
> 2. Jean-Michel Blanquer (May 2017 – May 2022)
> 3. Pap Ndiaye (May 2022 – July 2023)
> 4. Gabriel Attal (July 2023 – January 2024)
> 5. Amélie Oudéa-Castéra (January 2024 – February 2024), with a combined portfolio that also covered Youth, Sports and the Olympic Games
> 6. Nicole Belloubet (February 2024 – September 2024)
> 7. Anne Genetet (September 2024 – December 2024)
> 8. Élisabeth Borne (December 2024 – October 2025), as Minister of State with a portfolio that also covered Higher Education and Research
> 9. Édouard Geffray (October 2025 – present as of my June 2026 knowledge cutoff), appointed in Sébastien Lecornu's second government
>
> The ministry's exact title and scope changed several times over this period. French cabinets have also been reshuffled often in recent years, so there may have been changes since my cutoff. Turning on web search would let me confirm who holds the post today.

(Al final dice que el nombre y las competencias del ministerio cambiaron varias veces, que puede haber cambios posteriores a su fecha de corte y que con la búsqueda web podría confirmarlo.)

Debajo de la respuesta, la aplicación mostró el aviso «Web search is off» con un botón para activar la búsqueda web.

## Lo que descubrí (después de la prueba)

1. **Mi hipótesis no se confirmó.** En un chat limpio, Haiku nombró a **Geffray** en 7 de 8 intentos y **nunca** a Blanquer. Así que «gana el nombre más frecuente» **no** explica la respuesta de Blanquer de la segunda prueba.
2. **La misma pregunta no siempre da la misma respuesta.** Mismo modelo, misma configuración, mismas palabras: 7 veces Geffray y una vez Borne. Es el azar de la predicción del siguiente token: **una respuesta es solo una muestra**. Para saber lo que «piensa» un modelo, hay que preguntarle varias veces.
3. **Saber no es lo mismo que encontrar.** Haiku conoce a Geffray (paso A), pero su lista se detuvo en Borne, «December 2024 onward» («desde diciembre de 2024»). La forma de preguntar cambió lo que salió: si le pedía un solo nombre, encontraba a Geffray; si le pedía una lista por orden de fechas, se paraba antes. Su única respuesta «Borne» del paso A coincide con el punto donde se detuvo la lista. A la lista también le falta Amélie Oudéa-Castéra (de enero a febrero de 2024).
4. **Modelos distintos, calidad distinta.** Opus nombró a Geffray todas las veces, siempre con el mes (octubre de 2025) y el gobierno (el de Sébastien Lecornu). Su lista estaba completa y llegaba hasta Geffray. Haiku fue menos constante y menos completo. *(Opus tuvo menos intentos: 4 en lugar de 8.)*
5. **Entonces, ¿por qué Blanquer en la segunda prueba? Probablemente por la conversación (memoria de trabajo).** El artículo del CFR **no** menciona a Blanquer (lo comprobé en el texto del artículo). En la segunda prueba, fue Haiku quien dijo, por error, que el artículo lo nombraba, y después habló de él (de 2017 a 2022) antes de que yo le pidiera un nombre de su entrenamiento. Cuando por fin respondió, Blanquer **ya estaba en la conversación**, y lo que hay en el contexto influye mucho en los siguientes tokens. Además, la conversación giraba en torno al artículo (*«Based only on this text…»*). Es una explicación posible, no una prueba.
6. **La forma de la pregunta importa (capacidad de dirección).** En la segunda prueba necesité ocho mensajes para conseguir un nombre. Aquí, una sola pregunta clara (*«based only on your training data… Give one name»*) obtuvo una respuesta directa todas las veces, siempre con el aviso de que podía estar desactualizada.
7. **Las líneas de estado a veces están en francés.** Con Opus, dos de las cuatro líneas de estado estaban en francés (*«Vérification des mandats successifs après 2023»*), aunque mi pregunta estaba en inglés. Quizá el tema francés influyó en el idioma de su razonamiento.

## Límites de esta prueba

- Pocos intentos: 8 con Haiku y 4 con Opus, y solo **una** lista por modelo. Los números muestran una tendencia, no probabilidades exactas.
- En el intento 4 de Haiku, mi pregunta no tenía punto final: una diferencia mínima.
- Las fechas y los gobiernos que dan los modelos salen de su entrenamiento. Comprobé con una búsqueda web que Geffray es el ministro actual, pero su fecha de nombramiento (octubre de 2025) y la lista de ministros aún necesitan una fuente.
