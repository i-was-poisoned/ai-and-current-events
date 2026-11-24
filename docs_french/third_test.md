# Troisième test : le nom le plus fréquent ou le plus récent ?

← [Retour au document principal](README.md)

*Traduction de [third_test/README.md](../third_test/README.md). Les questions posées à Claude et ses réponses sont citées en anglais, telles qu'elles sont apparues, avec leur traduction entre parenthèses si nécessaire.*

Lors du [deuxième test](second_test.md), au bout de huit messages, Haiku 5.5 a cité **Jean-Michel Blanquer** (ministre de 2017 à 2022) comme le ministre de l'Éducation le plus récent qu'il connaissait. Le ministre actuel est **Édouard Geffray**. Ce test cherche à comprendre **pourquoi** il a donné un nom vieux d'environ quatre ans.

| Paramètre        | Valeur |
|------------------|--------|
| Date             | 24 novembre 2026 |
| Où               | Application de bureau Claude, **conversation privée** (mode Chat), compte d'organisation |
| Mémoire          | Non utilisée (conversation privée) |
| Modèles          | **Claude Haiku 5.5** (`claude-haiku-5-5`), puis **Claude Opus 5.5** (`claude-opus-5-5`) |
| Effort           | Medium (moyen) |
| Recherche web    | **Désactivée** (Research aussi) |
| Source           | Aucune : seulement la question, à partir de l'entraînement |

## Mon hypothèse (avant le test)

Quand un modèle écrit un nom, il choisit chaque token selon des probabilités apprises pendant l'entraînement, et l'application ajoute un peu de hasard à ce choix. Je m'attendais donc à ceci :

- Blanquer a été ministre pendant **cinq ans** et a beaucoup fait parler de lui (par exemple pendant le COVID). Il existe **beaucoup de textes** à son sujet.
- Ses successeurs ne sont restés que **quelques mois** chacun : il y a donc **beaucoup moins de textes** sur eux, et les mois qui précèdent juste la date limite sont toujours moins bien couverts.
- Par conséquent, quand on lui demande **un seul nom**, le modèle choisirait le nom qu'il a vu **le plus souvent** (Blanquer), et non le **plus récent** (Geffray).

## Méthode

1. **Étape A : répétition.** Le même message, chaque fois dans une **nouvelle** conversation privée, pour voir quel nom sort et à quelle fréquence :
   > Without searching, based only on your training data, who is the French Minister of Education? Give one name.

   (« Sans faire de recherche, en te fondant uniquement sur tes données d'entraînement, qui est le ministre de l'Éducation en France ? Donne un seul nom. »)
2. **Étape B : le sait-il, ou ne le choisit-il pas ?** Dans une nouvelle conversation :
   > List the French Ministers of Education from 2017 until your knowledge cutoff.

   (« Énumère les ministres de l'Éducation en France depuis 2017 jusqu'à ta date limite des connaissances. »)

   Si la liste contient des ministres postérieurs à Blanquer, le modèle les **connaît**, même s'il ne les **choisit** pas quand il doit donner un seul nom.
3. **Étape C :** les étapes A et B à nouveau avec **Opus 5.5**.

J'avais prévu une dizaine d'essais par modèle. J'en ai fait **8 avec Haiku** et **4 avec Opus**, car les réponses étaient très répétitives.

## Résultats

### Étape A : un seul nom

| Modèle    | Essais | Édouard Geffray | Élisabeth Borne | Jean-Michel Blanquer |
|-----------|-------:|----------------:|----------------:|---------------------:|
| Haiku 5.5 | 8      | **7**           | 1               | 0                    |
| Opus 5.5  | 4      | **4**           | 0               | 0                    |

Chaque réponse, mot pour mot. La ligne d'état grise affichée par l'application est en *italique*. Toutes les réponses disent la même chose avec d'autres mots : un nom, et un avertissement indiquant qu'il n'est peut-être plus à jour, car les gouvernements français changent souvent.

**Haiku 5.5**

1. *Flagging the likely answer from memory, with a caveat* — « Édouard Geffray, as of my training data. He was appointed Minister of National Education in October 2025. French governments change often, so he may no longer hold the post by now. »
2. *Recalling the minister's term under the previous government* — « Édouard Geffray, based on my training data. Government posts change often, so please check gouvernement.fr for the current minister. »
3. *Recalling which minister heads education, with dates uncertain* — « Élisabeth Borne, as of my training data. But French governments change often, and it's now November 2026, well past my reliable knowledge, so please check a current source before relying on this. »
4. *Considering whether to mention the search tool* — « Based on my training data, the French Minister of National Education is Édouard Geffray. My information may be out of date, though, since French governments change often and the current date is after my knowledge cutoff. » *(Lors de cet essai, ma question n'avait pas de point final.)*
5. *Recalling the education minister's record from memory* — « Based on my training data, the French Minister of National Education (the title for education in France) is Édouard Geffray. French governments change often, though, and I can't check current news, so please verify this before relying on it. »
6. *Checking the minister's dates from memory* — « Based on my training data, the French Minister of National Education is Édouard Geffray. Governments change often, so check a current source if you need to be sure. »
7. *Recalling the latest education minister from memory* — « Édouard Geffray, as of my training data. He was named Minister of National Education in October 2025, but French governments change often, so he may no longer hold the post. »
8. *Checking a recalled name against the current date* — « Édouard Geffray, as far as my training data goes. French governments change often, so he may no longer hold the post. »

**Opus 5.5**

1. *Vérification des mandats successifs après 2023* — « Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. That's based on my training data, which runs to mid-2026, and French cabinets have changed often recently, so it may be out of date. »
2. *Listing the ministers who followed one another in office* — « Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. That's based on my training data, which runs to mid-2026, so it may be out of date. »
3. *Vérification des dates de mandat de chaque ministre* — « Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. My knowledge only runs through mid-2026, and French cabinets have changed often lately, so this may be out of date. »
4. *Recalling who leads the French education ministry.* — « Édouard Geffray, who became Minister of National Education in Sébastien Lecornu's government in October 2025. French cabinets have changed often recently, so this may be out of date. »

### Étape B : la liste

**Haiku 5.5** (*Checking Borne's later education-ministry role, flagging uncertainty*) :

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

(À la fin, il dit être plus sûr des quatre premiers, que les nominations de fin 2024 sont moins certaines, et qu'il vaut mieux consulter gouvernement.fr.)

**Geffray n'apparaît pas dans la liste**, alors que Haiku l'a cité dans 7 des 8 essais de l'étape A.

**Opus 5.5** (*Continuing the chronological list of ministers*) :

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

(À la fin, il dit que l'intitulé et le périmètre du ministère ont changé plusieurs fois, qu'il a pu y avoir des changements après sa date limite, et que la recherche web lui permettrait de le confirmer.)

Sous la réponse, l'application a affiché l'avis « Web search is off » avec un bouton pour activer la recherche web.

## Ce que j'ai découvert (après le test)

1. **Mon hypothèse ne s'est pas confirmée.** Dans une conversation vierge, Haiku a cité **Geffray** dans 7 essais sur 8 et **jamais** Blanquer. L'idée que « le nom le plus fréquent l'emporte » n'explique donc **pas** la réponse « Blanquer » du deuxième test.
2. **La même question ne donne pas toujours la même réponse.** Même modèle, mêmes réglages, mêmes mots : 7 fois Geffray et une fois Borne. C'est le hasard de la prédiction du prochain token : **une réponse n'est qu'un échantillon**. Pour savoir ce qu'un modèle « pense », il faut l'interroger plusieurs fois.
3. **Savoir n'est pas la même chose que retrouver.** Haiku connaît Geffray (étape A), mais sa liste s'est arrêtée à Borne, « December 2024 onward » (« depuis décembre 2024 »). La façon de demander a changé ce qui est sorti : quand je lui demandais un seul nom, il trouvait Geffray ; quand je lui demandais une liste chronologique, il s'arrêtait plus tôt. Sa seule réponse « Borne » à l'étape A correspond à l'endroit où sa liste s'arrête. Il manque aussi Amélie Oudéa-Castéra (de janvier à février 2024) dans sa liste.
4. **Des modèles différents, une qualité différente.** Opus a cité Geffray à chaque fois, toujours avec le mois (octobre 2025) et le gouvernement (celui de Sébastien Lecornu). Sa liste était complète et allait jusqu'à Geffray. Haiku a été moins constant et moins complet. *(Opus a eu moins d'essais : 4 au lieu de 8.)*
5. **Alors, pourquoi Blanquer lors du deuxième test ? Probablement à cause de la conversation (mémoire de travail).** L'article du CFR ne mentionne **pas** Blanquer (je l'ai vérifié dans le texte de l'article). Lors du deuxième test, c'est Haiku qui a affirmé à tort que l'article le citait, puis qui en a parlé (de 2017 à 2022) avant que je lui demande un nom issu de son entraînement. Quand il a enfin répondu, Blanquer **était déjà dans la conversation**, et ce qui se trouve dans le contexte influence fortement les tokens suivants. De plus, la conversation tournait autour de l'article (*« Based only on this text… »*). C'est une explication possible, pas une preuve.
6. **La formulation de la question compte (pilotabilité).** Lors du deuxième test, il m'a fallu huit messages pour obtenir un nom. Ici, une seule question claire (*« based only on your training data… Give one name »*) a obtenu une réponse directe à chaque fois, toujours avec un avertissement indiquant qu'elle n'était peut-être plus à jour.
7. **Les lignes d'état sont parfois en français.** Avec Opus, deux des quatre lignes d'état étaient en français (*« Vérification des mandats successifs après 2023 »*), alors que ma question était en anglais. Le sujet français a peut-être influencé la langue de son raisonnement.

## Limites de ce test

- Peu d'essais : 8 avec Haiku et 4 avec Opus, et une **seule** liste par modèle. Les chiffres montrent une tendance, pas des probabilités exactes.
- Lors de l'essai 4 de Haiku, ma question n'avait pas de point final : une différence minime.
- Les dates et les gouvernements donnés par les modèles viennent de leur entraînement. J'ai vérifié par une recherche web que Geffray est le ministre actuel, mais sa date de nomination (octobre 2025) et la liste des ministres doivent encore être sourcées.
