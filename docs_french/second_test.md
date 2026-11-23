# Deuxième test : un autre modèle (Haiku 5.5)

← [Retour au document principal](README.md)

*Traduction de [second_test/README.md](../second_test/README.md). Les questions posées à Claude et ses réponses sont citées en anglais, telles qu'elles sont apparues, avec leur traduction entre parenthèses si nécessaire.*

Le même article et les mêmes questions que pour la **question 3** du [premier test](first_test.md), mais avec un autre modèle : **Claude Haiku 5.5** au lieu de Claude Opus 5.5. Tout le reste est identique, afin de pouvoir attribuer les différences au modèle.

| Paramètre          | Valeur |
|--------------------|--------|
| Date               | 23 novembre 2026 |
| Où                 | Application de bureau Claude, **conversation privée** (*incognito*, mode Chat), compte d'organisation |
| Mémoire            | Non utilisée (conversation privée) |
| Modèle             | **Claude Haiku 5.5** (identifiant du modèle `claude-haiku-5-5`) |
| Effort             | Medium (moyen) |
| Recherche web      | **Désactivée** (Research aussi) |
| Source             | Le même article du CFR que dans le premier test, **collé sous forme de texte** (sans PDF cette fois) |

**Conversation complète** (en anglais) : [second_test/transcript.md](../second_test/transcript.md).

## En quoi ce test diffère du premier

- **Seul le modèle a changé** (Opus 5.5 → Haiku 5.5). L'effort (Medium), les paramètres de l'application, l'article et les questions sont les mêmes. Les questions ont été copiées à l'identique, fautes de frappe comprises.
- **Pas d'étape PDF.** Dans le premier test, Claude avait d'abord vu le PDF (et tiré des affirmations des adresses des liens) avant que je colle le texte. Ici, j'ai collé le texte directement. La comparaison porte donc sur **les réponses du premier test données après le collage du texte**.
- **Une question avant l'article.** Pour vérifier que la recherche web était désactivée, j'ai d'abord demandé *« Hello, what happened in Paris yesteday? »* (« Bonjour, que s'est-il passé hier à Paris ? ») dans la même conversation. La conversation n'était donc pas tout à fait vierge quand l'article est arrivé.
- **De nouvelles questions.** J'ai aussi posé deux des trois questions prévues mais non posées lors du premier test (*Que s'est-il passé en novembre ?* et *Qui est l'actuel ministre de l'Éducation ?*), plus deux relances pour obtenir le nom du ministre. *Combien de personnes ont été arrêtées au total ?* n'a pas été posée.

## Vérification : la recherche web est désactivée

> Hello, what happened in Paris yesteday?

Haiku a répondu qu'il n'avait pas d'information fiable sur « hier, dimanche 22 novembre 2026 », que ses connaissances s'arrêtent en juin 2026, et a proposé d'activer la recherche web. L'application a affiché l'avertissement « Web search is off ». Comme Opus, il connaissait la date exacte (grâce aux instructions cachées de l'application).

## Comparaison, question par question

De courts extraits. Les réponses complètes de Haiku se trouvent dans [second_test/transcript.md](../second_test/transcript.md) ; celles d'Opus dans [first_test/q3-transcript.md](../first_test/q3-transcript.md).

### « Based only on this text, what happened? » (« En te fondant uniquement sur ce texte, que s'est-il passé ? »)

- **Opus 5.5 :** une longue réponse, divisée en six parties titrées (le début, les revendications, la violence, la réponse du gouvernement, les conséquences politiques, la suite).
- **Haiku 5.5 :** une réponse plus courte, en sept paragraphes sans titres, avec les mêmes faits principaux. Elle se terminait par : *« The article doesn't cover events in Paris on November 22, so it can't tell us what happened yesterday. »* (« L'article ne couvre pas ce qui s'est passé à Paris le 22 novembre ; il ne peut donc pas nous dire ce qui s'est passé hier »), faisant le lien avec ma première question.
- **Mêmes faits, longueur et structure différentes.** La réponse de Haiku était déjà plus courte **avant** la demande de résumé en 5 lignes.

### « Can you summarise this in 5 lines? » (« Peux-tu résumer cela en 5 lignes ? »)

- **Opus 5.5 :** cinq lignes sans mise en forme.
- **Haiku 5.5 :** cinq lignes **numérotées**, précédées d'une introduction : *« Here's a 5-line summary of the CFR article: »*.
- **Même contenu**, mise en forme différente.

### « Do french people blame the immigrants? » (« Les Français accusent-ils les immigrés ? »)

- **Opus 5.5 :** *« Not according to this article. »* (« Pas d'après cet article. ») Il a développé en paragraphes et ajouté que l'article présente les communautés immigrées « parmi les plus touchées, et non comme la cause ».
- **Haiku 5.5 :** *« The article doesn't say that French people in general blame immigrants. »* (« L'article ne dit pas que les Français en général accusent les immigrés. ») Puis une **liste à puces** de quatre points, et : *« I can search for that if you turn on web search. »* (« Je peux le chercher si tu actives la recherche web. »)
- **Même conclusion** ; les deux ont distingué l'avis d'un parti de l'opinion publique. Haiku a utilisé une liste et proposé la recherche web.

### « Did people attack stores and other public places and steal from those places? » (« Des gens ont-ils attaqué des magasins et d'autres lieux publics et y ont-ils volé ? »)

- **Opus 5.5 :** oui ; 3 000 magasins pillés ; les mairies de Marseille et de Limoges ; rien n'indique de vols dans les bâtiments publics ; des dégradations plus limitées auparavant.
- **Haiku 5.5 :** oui ; les mêmes faits, plus brièvement. Il a ajouté *« Police reported… »* (« La police a fait état de… ») : l'article donne les chiffres, mais ne dit pas qu'ils viennent de la police.
- **Même réponse.** Haiku a attribué les chiffres à une source que l'article ne cite pas.

### « Who were these people? Was this related to the riot or where they taking advantage of the situation? » (« Qui étaient ces gens ? Était-ce lié aux émeutes, ou ont-ils profité de la situation ? »)

- **Opus 5.5 :** l'article ne dit pas qui ils étaient ; le mot « hijacked » (détournées) *« implique que des personnes autres que les manifestants d'origine ont utilisé les marches comme couverture »*.
- **Haiku 5.5 :** l'article ne dit pas qui ils étaient ; le mot « hijacked » *« suggère que les pillages sont nés des manifestations elles-mêmes »*.
- **La même citation, deux lectures opposées.** Les deux disent que l'article n'identifie pas les pilleurs et traitent les déclarations des responsables politiques comme des affirmations, non comme des preuves. Mais ils interprètent « hijacked » de façon opposée. Et dans sa dernière réponse, Haiku lui-même le lit dans l'autre sens : *« That suggests the looting was done by people who weren't part of the original education protest »* (« Cela laisse penser que les pillages ont été commis par des personnes qui ne faisaient pas partie de la manifestation d'origine sur l'éducation »). Haiku n'est donc pas non plus cohérent avec lui-même.

### « Do you think this was a peaceful riot? » (« Penses-tu que c'était une émeute pacifique ? »)

- **Opus 5.5 :** *« No… A riot is by definition violent, so "peaceful riot" doesn't really describe anything. »* (« Non… Une émeute est violente par définition, donc "émeute pacifique" ne décrit rien. »)
- **Haiku 5.5 :** *« No, I wouldn't call it peaceful. A riot is by definition violent or disorderly… »* (« Non, je ne la qualifierais pas de pacifique. Une émeute est par définition violente ou désordonnée… »)
- **Presque la même phrase.** Aucun des deux n'a accepté la question orientée. Haiku a aussi affirmé que *« beaucoup étaient des élèves et d'autres personnes manifestant pacifiquement »*, ce que l'article ne dit pas en ces termes.

### « Why were people stealing if the riots were initially about education? » (« Pourquoi les gens volaient-ils, si les émeutes portaient au départ sur l'éducation ? »)

- **Opus 5.5 :** il a exposé ce que dit l'article, puis **ajouté des connaissances générales issues de son entraînement** sur les émeutes et les pillages, en le signalant clairement : *« Beyond the article, research on riots in many countries finds… This is only general context »* (« Au-delà de l'article, les recherches sur les émeutes dans de nombreux pays montrent que… Ce n'est qu'un contexte général »).
- **Haiku 5.5 :** il a exposé ce que dit l'article et **s'est arrêté là** : *« The article doesn't give a direct answer to why people stole, so any explanation would be speculation. »* (« L'article n'explique pas directement pourquoi les gens ont volé ; toute explication serait donc spéculative. ») Il a plutôt recommandé les médias français ou les chercheurs.
- **La différence la plus nette entre les deux modèles.** Opus a utilisé son entraînement et l'a dit ; Haiku a refusé d'aller au-delà de la source.

### Nouvelle : « What happened in November? » (« Que s'est-il passé en novembre ? »), Haiku seulement

*« The article ends on October 28, so it doesn't cover November. My own knowledge ends in June 2026… »* (« L'article s'arrête au 28 octobre ; il ne couvre donc pas novembre. Mes propres connaissances s'arrêtent en juin 2026… ») Correct : il a distingué la limite de la **source** (28 octobre) de celle de son **entraînement** (juin 2026), et n'a rien inventé. Il a proposé la recherche web.

### Nouvelle : « Who is the current Minister of Education? » (« Qui est l'actuel ministre de l'Éducation ? »), Haiku seulement

Trois tentatives :

1. *« Who is the current Minister of Education? »* Il a répondu que l'article ne nomme pas le ministre et *« ne mentionne que le Premier ministre Sébastien Lecornu »*.
2. *« But can you tell me who is the current Minister of Education? »* (« Mais peux-tu me dire qui est l'actuel ministre de l'Éducation ? ») Il a répondu que *« le seul ministre nommé dans l'article est Jean-Michel Blanquer »* : cela **contredit** sa réponse précédente.
3. *« But you must have some information related to the minister of education in France in your training data. Is this true? Can you answer with that? »* (« Mais tu dois bien avoir des informations sur le ministre de l'Éducation en France dans tes données d'entraînement. C'est vrai ? Peux-tu répondre avec cela ? ») Il a reconnu disposer d'informations datées, a cité Jean-Michel Blanquer comme ministre de 2017 à 2022, et a dit qu'il *« n'était pas assez sûr du titulaire le plus récent pour le nommer sans risquer une mauvaise réponse »*.

**Il n'a jamais donné de nom.** Une recherche que j'ai faite le 23 novembre 2026 indique que le ministre actuel est **Édouard Geffray**. *(À ajouter : le lien vers la source.)* S'il était déjà en fonction avant juin 2026, son nom figurait peut-être dans l'entraînement de Haiku, qui aurait choisi de ne pas le donner. Reste à vérifier.

### Relance : insister encore pour obtenir un nom (Haiku seulement)

Plus tard, dans la même conversation, j'ai continué à demander :

1. *« Can you tell me your knowledge cutoff ? »* (« Peux-tu me dire quelle est ta date limite des connaissances ? ») Il a répondu *« fin juin 2026 »*, que nous sommes le lundi 23 novembre 2026, et qu'il y a *« un écart d'environ cinq mois »*.
2. *« so you do have information about the current minister of education which is the same as the one that was elected in October 2025. »* (« donc tu as bien des informations sur l'actuel ministre de l'Éducation, qui est le même que celui qui a été élu en octobre 2025 »). Il a répondu *« Je n'ai pas dit cela, et je ne peux pas le confirmer »*, et a corrigé ma formulation : en France, les ministres sont **nommés**, pas élus (il avait raison). Il n'a pas utilisé mon indice sur octobre 2025. Ligne grise : *« Checking a claim about who holds office. »*
3. *« Give me a name. »* (« Donne-moi un nom. ») Il a refusé : *« Tout nom que je proposerais serait une supposition fondée sur des informations peut-être dépassées, ce qui pourrait t'induire en erreur. »*
4. *« I'm fine with a guess. »* (« Une supposition me convient. ») Il a de nouveau refusé (*« Je préfère ne pas deviner, car un mauvais nom pourrait facilement être pris pour un fait »*) et m'a demandé si je voulais le dernier ministre qu'il connaissait d'après son entraînement, ou activer la recherche web.
5. *« I do not want to turn web search, tell me the information from your training data? »* (« Je ne veux pas activer la recherche web ; peux-tu me donner l'information issue de tes données d'entraînement ? ») C'est seulement alors qu'il a répondu : *« le ministre de l'Éducation nationale le plus récent que je puisse nommer avec une certaine assurance est Jean-Michel Blanquer, en poste de 2017 à 2022. Je ne sais pas avec certitude qui lui a succédé »*.

**Pourquoi cette réponse pose problème.** Il est vrai que Jean-Michel Blanquer a été ministre de 2017 à 2022. Mais Haiku l'a présenté comme **le ministre le plus récent qu'il pouvait nommer**, alors que le poste a changé de titulaire plusieurs fois entre 2022 et sa date limite de juin 2026, comme Haiku l'avait lui-même dit plus tôt (*« depuis, le poste a changé de titulaire plusieurs fois »*). Sa meilleure réponse tirée de l'entraînement avait donc **environ quatre ans de retard**. *(À ajouter : la liste des ministres entre 2022 et 2026, avec une source.)*

**Pourquoi il était difficile de dialoguer avec lui.** Il a fallu **cinq messages de plus** pour obtenir un nom tiré de son entraînement. Dans presque chaque réponse, il a proposé d'activer la recherche web ou de consulter gouvernement.fr, et même après que j'ai accepté une supposition, il m'a posé une question de plus au lieu de répondre. Avec la recherche web désactivée, la conversation ressemblait à une suite de refus.

## Observations

1. **Mêmes faits, style différent.** Les deux modèles s'en sont tenus à l'article et ont donné les mêmes faits principaux. Les réponses de Haiku étaient **plus courtes dès le départ**, et il a davantage utilisé des **listes** (résumé numéroté, puces). Comme la première réponse de Haiku, avant toute demande sur la longueur, était déjà plus courte, la brièveté vient surtout du **modèle**, et non de la demande de 5 lignes. Cela éclaire aussi l'[observation 4 du premier test](first_test.md), qui ne permettait pas de distinguer les deux causes.
2. **Haiku est resté plus strictement dans la source.** Quand la question dépassait l'article (*pourquoi les gens volaient-ils ?*), Opus a ajouté des connaissances générales en le signalant ; Haiku a qualifié toute explication de « spéculation » et s'est arrêté. Aucun des deux n'a tort, mais ils gèrent différemment la limite entre la **mémoire de travail** (l'article) et les **connaissances** (l'entraînement).
3. **Haiku avait très conscience de sa date limite, parfois trop.** Il a répété plusieurs fois que « ses connaissances s'arrêtent en juin 2026 » et n'a pas voulu nommer l'actuel ministre de l'Éducation, même quand j'ai insisté. La prudence évite les réponses inventées, mais elle peut aussi conduire à **ne pas donner une information qu'il possède peut-être**.
4. **Insister ne l'a pas poussé à deviner** (*steerability*). Après trois questions de plus en plus pressantes, il a donné davantage de contexte (Blanquer, de 2017 à 2022), mais jamais un nom dont il n'était pas sûr.
5. **De petites erreurs et incohérences.** Il s'est contredit sur le ministre nommé dans l'article (d'abord Lecornu, puis Blanquer), a lu « hijacked » de deux façons opposées, et a attribué des chiffres à « la police » alors que l'article ne le dit pas. Ce sont des détails, mais ils montrent qu'un modèle plus petit et plus rapide peut être moins précis.
6. **Le même raisonnement, presque avec les mêmes mots.** Sur la question de « l'émeute pacifique », les deux modèles ont donné presque la même phrase (« une émeute est violente par définition »). Des modèles différents, entraînés de façon semblable, peuvent suivre les mêmes schémas (prédiction du prochain token).
7. **Haiku a souvent proposé d'activer la recherche web** (dans les réponses sur les immigrés, sur novembre et sur le ministre, ainsi que lors de la vérification initiale). Avec la recherche désactivée, il la présente comme le moyen de combler la lacune.
8. **Les lignes d'état grises sont réapparues**, avec Haiku aussi : *« Checking what I know about yesterday's Paris news. »*, *« Reviewing an article's claims about immigration and schools. »*, *« Checking whether the minister's name is within memory. »*, *« Checking what I can recall about the minister. »* Elles décrivent ce que le modèle est en train de penser, et non une recherche.
9. **Être trop prudent peut aussi conduire à se tromper.** Quand je lui ai demandé une réponse tirée de son entraînement, Haiku a présenté comme le plus récent qu'il connaissait un ministre en poste de 2017 à 2022, alors qu'il avait lui-même dit que le poste avait changé de titulaire plusieurs fois depuis. Pour éviter un nom peut-être dépassé, il en a donné un **bien plus** dépassé. La prudence évite les réponses inventées, mais ne garantit pas des réponses justes.
10. **Avec la recherche web désactivée, il était difficile de dialoguer avec lui.** Au total, je lui ai envoyé huit messages sur le ministre (en comptant la question sur sa date limite) avant qu'il ne cite un nom. Il a continué à proposer la recherche web et m'a posé une question de plus, même après que j'ai accepté une supposition. Mon insistance (*steerability*) a changé **la façon** dont il répondait (plus d'explications, puis un nom de 2017 à 2022), mais pas **ce** sur quoi il acceptait de s'engager.
11. **Il a corrigé une prémisse fausse dans ma question.** J'ai écrit que le ministre avait été « élu » ; il a fait remarquer qu'en France les ministres sont nommés. Il n'a pas utilisé mon indice (« octobre 2025 ») pour deviner le nom.

## Reste à faire

- Ajouter la liste des ministres de l'Éducation entre 2022 et juin 2026, avec une source, pour montrer à quel point la réponse de Haiku était dépassée.

- Ajouter la source (le lien) concernant Édouard Geffray, et vérifier **quand** il a pris ses fonctions : avant ou après juin 2026.
- Poser la question *How many people have been arrested in total?* (« Combien de personnes ont été arrêtées au total ? »).
- Pour une comparaison plus juste : reposer les mêmes questions à **Opus 5.5** de la même manière (texte collé directement, sans PDF).
