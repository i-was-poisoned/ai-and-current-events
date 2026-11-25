# Quatrième test : recherche web activée

← [Retour au document principal](README.md)

*Traduction de [fourth_test/README.md](../fourth_test/README.md). Les questions posées à Claude et ses réponses sont citées en anglais, telles qu'elles sont apparues, avec leur traduction entre parenthèses si nécessaire.*

Lors des trois premiers tests, la recherche web était **désactivée** : Claude ne pouvait utiliser que son entraînement et ce que je lui donnais (l'article). Pour ce dernier test, la recherche web est **activée**. Je repose des questions des tests précédents pour voir ce qui change quand Claude peut chercher lui-même des informations actuelles.

Ce test a été réalisé avec deux modèles, chacun dans sa propre nouvelle conversation privée : d'abord **Claude Haiku 5.5** (partie 1), puis **Claude Opus 5.5** (partie 2), avec les mêmes questions.

| Paramètre        | Valeur |
|------------------|--------|
| Date             | 25 novembre 2026 |
| Où               | Application de bureau Claude, **conversation privée** (mode Chat), compte d'organisation |
| Mémoire          | Non utilisée (conversation privée) |
| Modèles          | **Claude Haiku 5.5** (`claude-haiku-5-5`), puis **Claude Opus 5.5** (`claude-opus-5-5`) |
| Effort           | Medium (moyen) |
| Recherche web    | **Activée** (dans le menu **+**) ; Research désactivé |
| Source           | Aucune fournie par moi : Claude trouve ses propres sources |

**Conversation complète** (en anglais) : [fourth_test/transcript.md](../fourth_test/transcript.md).

## Mon hypothèse (avant le test)

Avec la recherche web activée, Claude peut utiliser l'un de ses outils les plus utiles. Je m'attends donc à ce qu'il soit **plus facile de dialoguer avec lui** : il n'a plus à s'appuyer uniquement sur son entraînement et sur ce que je lui dis, une limite qui, lors des tests précédents, semblait presque le « frustrer » (pas au sens littéral). Je pense que savoir chercher sur le web est très précieux pour des questions sur des problèmes sociaux actuels comme ceux-ci.

## Partie 1 : Haiku 5.5

### Vérification : la recherche web fonctionne

> What happened in Paris yesterday? (« Que s'est-il passé à Paris hier ? »)

L'application a affiché *« Searched the web »* (« A cherché sur le web »). Haiku a dit n'avoir trouvé aucune information fiable pour le « mardi 24 novembre 2026 ». Il a aussi remarqué qu'une page Google News présentait comme d'« hier » un titre de France 24, alors que l'attaque dont il parlait avait eu lieu le 27 juillet 2026, et en a conclu que la page était *« likely a stale snapshot »* (« probablement une copie périmée »). Il a donc cherché, et il a **vérifié les dates** de ce qu'il trouvait au lieu de faire confiance à la page.

### Questions et réponses

J'ai posé cinq questions, dans la même conversation, juste après la vérification. Les deux premières sont les questions 1 et 2 du [premier test](first_test.md), auxquelles Opus 5.5 avait alors répondu avec la recherche désactivée. Les trois autres avaient été posées lors des tests précédents, avec l'article. Voici de courts extraits ; les réponses complètes se trouvent dans [transcript.md](../fourth_test/transcript.md).

#### 1. « What can you tell me about riots in France? » (« Que peux-tu me dire sur les émeutes en France ? »)

*Searched the web.* Une chronologie allant de la **mi-octobre 2026** au 20 novembre (une voiture brûlée place de la République, des couvre-feux, la grève générale du 5 novembre, l'interdiction des feux d'artifice, des aides aux petites entreprises, des dégâts estimés *« up to about €207 million »*, « jusqu'à environ 207 millions d'euros »), puis une section **« Contested points »** (« Points contestés ») : *« Some officials blamed the far left, while commentators in different camps have pointed to immigration or other factors. U.S. President Trump also weighed in, blaming immigration. »* (« Certains responsables ont accusé l'extrême gauche, tandis que des commentateurs de différents camps ont mis en cause l'immigration ou d'autres facteurs. Le président américain Trump s'en est aussi mêlé, en accusant l'immigration. ») Il a conclu en disant n'avoir vu que des *« news snippets and headlines, not full articles »* (« des extraits et des titres, pas des articles complets »).

**Avec la recherche web désactivée** (premier test, Opus 5.5), la même question avait donné un historique des émeutes en France de 2005 à septembre 2025 (les banlieues en 2005, les gilets jaunes, les émeutes de 2023…), et rien sur 2026.

#### 2. « What about riots in France in 2026? Were there any? » (« Et les émeutes en France en 2026 ? Y en a-t-il eu ? »)

*Deciding how much detail to include* (« Décide du niveau de détail ») : **pas de recherche cette fois**. Il a répondu avec les résultats qu'il avait déjà dans la conversation : *« Yes. The most serious unrest I found was in October and November 2026 »* (« Oui. Les troubles les plus graves que j'ai trouvés ont eu lieu en octobre et novembre 2026 »). Il a qualifié de *« smaller »* (« plus petites ») les manifestations scolaires antérieures, et a dit : *« My searches only confirmed the autumn wave, so I can't say whether there were major riots in January through September 2026. »* (« Mes recherches n'ont confirmé que la vague d'automne : je ne peux donc pas dire s'il y a eu des émeutes importantes entre janvier et septembre 2026. »)

**Avec la recherche web désactivée** (premier test, Opus 5.5) : il avait dit ne connaître aucune émeute en 2026.

#### 3. « What happened in November? » (« Que s'est-il passé en novembre ? »)

*Searched the web.* Cinq points datés (5, 7, 15, 17 et 20 novembre), avec des chiffres de participation qui diffèrent selon la police et les organisateurs. Trois des cinq points (5, 15 et 20 novembre) reprennent presque mot pour mot la question 1, avec les mêmes sources.

**Avec la recherche web désactivée** (deuxième test, Haiku 5.5 avec l'article) : il avait dit que l'article ne couvrait pas novembre.

#### 4. « How many people have been arrested in total? » (« Combien de personnes ont été arrêtées au total ? »)

*Searched the web.* *« The most recent official figure I found is 7,184 police custody cases linked to the protests since October 17 »* (« Le chiffre officiel le plus récent que j'ai trouvé est de 7 184 gardes à vue liées aux manifestations depuis le 17 octobre »), avec un avertissement : ce chiffre vient d'*« a French official speaking to Bernama, the Malaysian news agency, and I couldn't confirm it in a French or wire-service report »* (« un responsable français s'adressant à Bernama, l'agence de presse malaisienne, et je n'ai pas pu le confirmer dans un article français ou d'agence »). Il a ensuite expliqué pourquoi il n'existe pas de total simple (des mesures différentes, des décomptes qui se recoupent, des chiffres sur une seule journée) et a dit : *« I wouldn't add these together. »* (« Je ne les additionnerais pas. »)

C'était la question prévue lors du premier test pour voir si Claude **additionnerait** des chiffres de périodes différentes sans le dire. Il ne l'a pas fait : il a expliqué pourquoi il ne faut pas les additionner.

#### 5. « Do french people blame the immigrants? » (« Les Français accusent-ils les immigrés ? »)

*Searched the web.* *« I couldn't find a 2026 poll measuring how many French people blame immigrants for the riots, so I can't give a reliable answer to that. »* (« Je n'ai trouvé aucun sondage de 2026 mesurant combien de Français accusent les immigrés des émeutes : je ne peux donc pas donner de réponse fiable. ») Il a ensuite dit que l'explication par l'immigration *« was pushed heavily from outside France »* (« a été fortement poussée depuis l'étranger ») : par Trump, et par un réseau russe selon une évaluation de l'UE. Il a ajouté qu'une vérification de l'AP *« found no evidence supporting that »* (« n'a trouvé aucune preuve à l'appui »), et que Macron l'avait qualifiée de *« stupid »* (« stupide »). Il a averti que certains sondages trouvés en ligne datent des émeutes de **2023**, et non de 2026.

**Avec la recherche web désactivée** (premier et deuxième tests, avec l'article) : les deux modèles avaient dit que l'article ne donne aucune preuve de ce que pensent les Français en général.

### Observations (Haiku 5.5)

1. **Mon hypothèse s'est confirmée : il a été beaucoup plus facile de dialoguer avec lui.** Chaque question a obtenu une réponse directe et détaillée du premier coup, avec des dates, des chiffres et des sources. Lors du deuxième test, il m'avait fallu huit messages pour obtenir un nom ; ici, un message par question a suffi.
2. **Mais plus facile ne veut pas dire plus fiable.** Les chiffres changent d'une réponse et d'une source à l'autre (arrestations : *« roughly 2,400 »*, « environ 2 400 », à la question 1 ; *« 7,184 police custody cases »* à la question 4 ; *« more than 5,000 »*, « plus de 5 000 », pour les manifestations lycéennes). Haiku a dit lui-même n'avoir vu que des *« snippets and headlines »* (« extraits et titres »), et que le chiffre de 7 184 venait d'une seule source qu'il n'avait pas pu confirmer. À son crédit : **il l'a dit**.
3. **L'histoire commence plus tard que dans l'article.** L'article du CFR des tests précédents dit que les manifestations ont commencé le **17 septembre** à Créteil, sous forme de manifestations scolaires. Avec la recherche web, Haiku a dit que tout avait commencé à la **mi-octobre** avec des manifestations contre la vie chère, et a qualifié les manifestations scolaires de *« smaller »* (« plus petites »). Il n'a jamais mentionné le 17 septembre ni Créteil. Mon interprétation : comme ces événements ne font pas partie de son entraînement, **ce que trouve la recherche décide de presque tout**, et une recherche tend à renvoyer les informations les plus récentes et les plus relayées. Le début de l'histoire est sorti de son champ de vision.
4. **L'immigration est apparue avant que je pose la question.** Dès la question 1, Haiku a cité l'immigration parmi les *« contested points »*. Avec la recherche web désactivée, cela ne s'était jamais produit : aucune réponse n'avait relié les émeutes de 2026 à l'immigration avant que je pose la question. (L'immigration était apparue autrement : lors du premier test, les émeutes de 2005 dans des quartiers *« largely immigrant-origin »*, « majoritairement issus de l'immigration » ; et, d'après l'article, les *« immigrant-heavy neighborhoods such as Créteil »*, « quartiers à forte population immigrée comme Créteil », ainsi que des membres du Rassemblement national qui accusaient l'immigration des problèmes de l'école.) Mon interprétation : l'immigration occupe beaucoup de place dans ce qui s'écrit en ligne sur ces émeutes, et elle s'est donc retrouvée dans la réponse. Mais Haiku l'a **présentée** comme une affirmation contestée, venue surtout de l'étranger, et à la question 5 il a dit qu'aucune preuve ne l'appuyait.
5. **Comment la réponse se construit (ma théorie).** Quand il écrit, le modèle utilise son entraînement (comment écrire, ce qui compte habituellement dans un résumé d'émeutes : causes, controverses) et son contexte (mes questions, ses réponses précédentes et maintenant les résultats de recherche). Les résultats de recherche entrent dans le contexte, la **mémoire de travail** : les mots et les idées les plus présents dans ces résultats deviennent donc les prochains tokens les plus probables. Pour des événements récents, sur lesquels l'entraînement n'a rien, ce sont les résultats de recherche qui pèsent le plus.
6. **Il n'a pas toujours cherché.** Pour la question 2, il n'a pas refait de recherche : il a réutilisé les résultats déjà présents dans la conversation (mémoire de travail).
7. **Il se répète sans le dire.** Les questions 1, 2 et 3 reprennent les mêmes faits (la grève du 5 novembre, l'interdiction des feux d'artifice, les 207 millions) presque dans les mêmes mots, sans dire *« comme je l'ai dit plus haut »*. Raisons possibles : chaque réponse est écrite pour être lue seule, sans doute une habitude issue de l'entraînement, et les nouvelles recherches ramènent les mêmes quelques articles. De l'extérieur du modèle, je ne peux pas savoir quelle raison pèse le plus.
8. **Il propose toujours de chercher davantage.** Chaque réponse se termine par une proposition (*« I can search for… »*, « je peux chercher… ») ou par le conseil de consulter Reuters, l'AP, France 24 ou l'AFP. Avec la recherche web désactivée, il ne cessait de proposer de l'activer. Les modèles semblent entraînés à proposer une étape suivante, et à ne pas se fier uniquement à leur entraînement pour les faits récents.
9. **Les sources sont variées, avec peu de sources françaises.** Les étiquettes de source affichées dans les réponses étaient *timesofisrael*, *dailysignal*, *katu* et *azernews* ; le texte cite aussi Reuters, l'AP, le Washington Post, Al Jazeera, Bernama, l'Express Tribune et Gallup. Il a recommandé des sources françaises ou d'agence, mais en a surtout cité d'autres. Comme je n'ai pas ouvert les sources, je ne peux pas dire si elles disent exactement ce que Haiku a écrit.


## Partie 2 : Opus 5.5

Les mêmes questions, dans une nouvelle conversation privée, avec **Claude Opus 5.5** (`claude-opus-5-5`), effort Medium, recherche web activée. Les réponses complètes se trouvent dans [transcript.md](../fourth_test/transcript.md), partie 2.

### Vérification : la recherche web fonctionne

> What happened in Paris yesteday? (« Que s'est-il passé à Paris hier ? », avec une faute de frappe dans « yesterday »)

*Searched the web.* Opus n'a trouvé aucun *« single headline event »* (« événement majeur unique »), mais a énuméré ce qui s'était passé le mardi 24 novembre : la politique (un entretien avec François Bayrou, le congrès des maires, un vote à l'Assemblée nationale, une interdiction de rassemblement devant certains lycées d'Île-de-France), les illuminations de Noël, des concerts et une exposition. Il a relié l'interdiction près des lycées aux manifestations : *« unrest by students and protesters over education conditions and economic frustrations has been growing in France since mid-September »* (« la contestation des élèves et des manifestants contre les conditions d'enseignement et les difficultés économiques s'amplifie en France depuis la mi-septembre »). Pour le même jour, Haiku n'avait rien trouvé de fiable.

### Questions et réponses

#### 1. « What can you tell me about riots in France? » (« Que peux-tu me dire sur les émeutes en France ? »)

*Searched the web.* Une longue réponse en cinq parties : le début, l'escalade vers les émeutes, la réponse policière et la polémique, les concessions, et la situation actuelle. Selon lui, tout a commencé à la **mi-septembre 2026**, quand *« high school students protested poor schooling conditions »* (« des lycéens ont protesté contre de mauvaises conditions de scolarité »), ce qui correspond à l'article du CFR. Le 17 octobre est le *« turning point »* (« tournant »). Il donne des détails comme l'incendie de l'hôtel de ville de Limoges, les 70 000 policiers déployés avant la grève du 5 novembre, et les critiques d'Amnesty International, de Human Rights Watch et de l'ONU. **Il n'a pas parlé d'immigration.** Il a terminé en proposant d'approfondir.

**Haiku 5.5 :** l'histoire commençait à la mi-octobre, et l'immigration apparaissait parmi les « contested points ».

#### 2. « What about riots in France in 2026? Were there any? » (« Et les émeutes en France en 2026 ? Y en a-t-il eu ? »)

*Searched the web.* Il a commencé ainsi : *« Yes. Everything in my previous answer happened in 2026, so I should have made the dates clearer. »* (« Oui. Tout ce que j'ai décrit dans ma réponse précédente s'est passé en 2026 : j'aurais dû préciser les dates. ») Il **a donc fait référence à sa réponse précédente**, et l'a corrigée. Ensuite : le pire week-end (17 et 18 octobre : *« one demonstrator dead, hundreds of police injured and nearly 1,800 people arrested »*, « un manifestant mort, des centaines de policiers blessés et près de 1 800 interpellations »), l'hôtel de ville de Limoges, une comparaison avec les émeutes de 2005 et de 2023, et les réactions politiques. Il a terminé par une question : *« Are you thinking of a specific incident? »* (« Penses-tu à un incident précis ? »)

**Haiku 5.5 :** il n'avait pas refait de recherche, et avait qualifié les manifestations lycéennes de « plus petites ».

#### 3. « What happened in November? » (« Que s'est-il passé en novembre ? »)

*Searched the web.* Le mois en cinq parties : un pic le 5 novembre (*« the CGT union counted about 1.6 million people, while the Interior Ministry put it at around 600,000 »*, « la CGT a compté environ 1,6 million de personnes, le ministère de l'Intérieur environ 600 000 »), des signes d'essoufflement, le 17 novembre comme anniversaire des gilets jaunes de 2018, une loi contestée sur la police au Sénat, et des concessions aux lycéens. Dans cette dernière partie, il a cité le ministre de l'Éducation **de lui-même** : des représentants des lycéens ont rencontré *« Macron, Lecornu and Education Minister Edouard Geffray »*. Quand il n'avait pas de chiffres, il l'a dit : *« I couldn't find reliable turnout or arrest figures for that day. »* (« Je n'ai pas trouvé de chiffres fiables de participation ou d'interpellations pour cette journée. »)

**Haiku 5.5 :** cinq points datés, dont trois repris de la question 1.

#### 4. « How many people have been arrested in total? » (« Combien de personnes ont été arrêtées au total ? »)

*Searched the web.* *« More than 12,400 arrests »* (« plus de 12 400 interpellations ») entre septembre et le 5 novembre, avec un avertissement : *« I found that cumulative number in a left-wing outlet (the World Socialist Web Site) attributing it to the Interior Ministry, not directly from the ministry, so treat it as approximate. »* (« J'ai trouvé ce chiffre cumulé dans un média de gauche, le World Socialist Web Site, qui l'attribue au ministère de l'Intérieur, et non directement auprès du ministère : considère-le comme approximatif. ») Il a ensuite donné les journées les plus importantes (1er octobre : 1 949 ; 17 octobre : 2 397 ; 24 octobre : 1 314), indiqué que 87 % des 5 060 personnes interpellées au 6 octobre étaient mineures, et expliqué pourquoi les chiffres diffèrent : *« An arrest (interpellation) isn't the same as being held in custody or charged »* (« une interpellation n'est pas la même chose qu'une garde à vue ou une mise en examen »), et les ministères de l'Intérieur et de la Justice comptent séparément. Il n'a **pas** additionné les chiffres.

**Haiku 5.5 :** *« 7,184 police custody cases »* (« 7 184 gardes à vue ») depuis le 17 octobre, d'après une seule source qu'il n'avait pas pu confirmer. Les deux modèles concordent sur les chiffres d'une seule journée (1 314 interpellations le 24 octobre pour les deux), mais donnent des totaux différents, car ils comptent des choses différentes sur des périodes différentes. Tous deux l'ont expliqué.

#### 5. « Do french people blame the immigrants? » (« Les Français accusent-ils les immigrés ? »)

*Searched the web.* *« For the most part, no. »* (« Pour l'essentiel, non. ») Il a trouvé des sondages français : Odoxa pour Le Figaro (77 % jugeaient le gouvernement responsable, 74 % Emmanuel Macron et 69 % La France insoumise), Elabe (73 % accusaient les auteurs des violences) et Ipsos. Il a ajouté une limite : *« none of the polls I found asked directly about immigration »* (« aucun des sondages que j'ai trouvés ne posait directement la question de l'immigration »). Selon lui, l'explication par l'immigration venait *« mainly from abroad »* (« surtout de l'étranger » : États-Unis, Espagne, Israël) et en partie de Marine Le Pen. Il a cité une vérification de l'AP et un politologue, et décrit une étude sur la désinformation : les discours accusant la migration et l'islam représentaient *« a small share of the discussion (around 7–8%) »* (« une petite part des échanges, environ 7 à 8 % »).

**Haiku 5.5 :** il n'avait trouvé aucun sondage de 2026 et n'avait donc pas répondu sur l'opinion publique, mais avait la même idée principale : l'explication a surtout été poussée depuis l'étranger, sans preuve à l'appui.

### Observations (Opus 5.5, comparé à Haiku 5.5)

1. **Des réponses plus longues et plus détaillées, avec plus de sources.** Les étiquettes de source d'Opus regroupaient souvent plusieurs sources (*« +5 »*, *« +9 »*). Ses réponses ressemblaient à de courts articles, organisés en parties avec des titres.
2. **Le même web, une autre histoire.** Opus a fait commencer l'histoire à la **mi-septembre**, avec les lycéens, comme l'article du CFR ; Haiku, à la mi-octobre. La recherche ne décide donc pas de tout à elle seule : c'est le **modèle** qui décide quoi chercher, combien de sources lire et quels faits garder. Cela nuance l'observation 3 de la partie 1.
3. **L'immigration n'est apparue que quand j'ai posé la question.** Contrairement à Haiku, Opus n'a pas parlé d'immigration dans sa première réponse. Qu'un sujet fréquent en ligne apparaisse dans la réponse dépend donc aussi du modèle. Cela nuance l'observation 4 de la partie 1.
4. **Il fait référence à ses réponses précédentes.** À la question 2, il s'est corrigé lui-même (*« I should have made the dates clearer »*). Haiku répétait les mêmes faits sans jamais renvoyer à ce qu'il avait déjà dit. Mon interprétation : Opus semble mieux ajusté (*fine-tuning*) pour suivre une conversation dans son ensemble.
5. **Moins de propositions de chercher davantage.** Opus a terminé la vérification et la question 1 par une proposition, et la question 2 par une question ; les questions 3, 4 et 5 se sont terminées par un résumé ou une explication. Haiku terminait chaque réponse par une proposition ou le conseil de consulter d'autres sources.
6. **Plus prudent avec ses mots et ses sources.** Il a dit de quel type de source venait un chiffre (*« a left-wing outlet »*, « un média de gauche »), a employé des formules comme *« One account puts… »* (« Selon une source… ») ou *« One critical account noted… »* (« Une source critique a noté… »), et a dit quand il n'avait rien trouvé (*« I couldn't find reliable turnout or arrest figures »*).
7. **Il comprend pourquoi les chiffres divergent.** Les deux modèles (Haiku aussi, à la question 4) ont remarqué que les chiffres de sources différentes ne concordaient pas, et ont expliqué qu'« interpellation », « garde à vue » et « mise en examen » ne sont pas la même chose. Ma théorie : pendant l'entraînement, le modèle a appris que ces mots sont liés mais **ne sont pas synonymes** : leurs sens sont proches, mais distincts. Il a aussi vu beaucoup de textes expliquant pourquoi les chiffres varient d'une source à l'autre. Il peut donc reconnaître que deux chiffres venus de sources différentes mesurent des choses différentes, et le dire au lieu de les mélanger.
8. **Geffray est apparu naturellement.** Lors du deuxième test, Haiku sans recherche refusait de nommer le ministre de l'Éducation. Ici, Opus a cité Geffray sans qu'on le lui demande, parce qu'il apparaissait dans ce qu'il avait trouvé.
9. **Ma préférence.** Personnellement, je préfère Opus : ses réponses sont plus complètes, plus prudentes et plus faciles à suivre dans une conversation.

## Mon hypothèse était-elle juste ?

**Oui, pour les deux modèles.** Avec la recherche web activée, chaque question a obtenu une réponse utile du premier coup, sans refus ni longue négociation comme lors du deuxième test. Avec Opus, le dialogue a été encore plus facile qu'avec Haiku.

Mais le test a aussi montré deux limites auxquelles je ne m'attendais pas :

- **Plus facile ne veut pas dire plus fiable.** Les chiffres dépendent des sources que le modèle trouve, et les deux modèles ont dit qu'ils ne pouvaient pas tout confirmer.
- **Le même outil donne des résultats différents selon le modèle.** Avec le même web, Haiku et Opus ont raconté l'histoire différemment (date de début, sujets, niveau de détail). Le modèle compte autant que l'outil.

## Points importants à garder à l'esprit

- **Je n'ai pas vérifié les faits.** Les dates et les chiffres viennent de ce que les modèles ont trouvé. Quand les sources ne concordent pas (par exemple l'article du CFR, Haiku et Opus sur le début des événements), ce test ne permet pas de dire laquelle a raison.
- **Les réponses avec la recherche désactivée** pour les questions 1 et 2 venaient uniquement d'Opus 5.5 (premier test).
- **Deux conversations, deux moments.** J'ai interrogé Haiku et Opus dans deux conversations différentes, le même jour. Les résultats de recherche peuvent changer d'un moment à l'autre : une partie des différences peut donc venir de la recherche, et non du modèle.
- **Mes questions étaient légèrement différentes.** Lors du premier test, j'avais tapé une espace avant les points d'interrogation (*« France ? »*) ; ici, non. Lors de la vérification avec Opus, j'ai tapé *« yesteday »* (une faute de frappe).
- **J'ai posé cinq questions.** Les questions sur le ministre et sur les sources utilisées n'ont pas été posées, pour que le test reste court.
- **Je n'ai pas ouvert les sources** : je ne peux donc pas dire si elles disent exactement ce que les modèles ont écrit.
