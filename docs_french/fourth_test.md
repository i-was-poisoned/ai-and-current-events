# Quatrième test : recherche web activée

← [Retour au document principal](README.md)

*Traduction de [fourth_test/README.md](../fourth_test/README.md). Les questions posées à Claude et ses réponses sont citées en anglais, telles qu'elles sont apparues, avec leur traduction entre parenthèses si nécessaire.*

Lors des trois premiers tests, la recherche web était **désactivée** : Claude ne pouvait utiliser que son entraînement et ce que je lui donnais (l'article). Pour ce dernier test, la recherche web est **activée**. Je repose des questions des tests précédents pour voir ce qui change quand Claude peut chercher lui-même des informations actuelles.

Ce document porte sur **Claude Haiku 5.5**. Le même test avec Opus 5.5 suivra.

| Paramètre        | Valeur |
|------------------|--------|
| Date             | 25 novembre 2026 |
| Où               | Application de bureau Claude, **conversation privée** (mode Chat), compte d'organisation |
| Mémoire          | Non utilisée (conversation privée) |
| Modèle           | **Claude Haiku 5.5** (`claude-haiku-5-5`) |
| Effort           | Medium (moyen) |
| Recherche web    | **Activée** (dans le menu **+**) ; Research désactivé |
| Source           | Aucune fournie par moi : Claude trouve ses propres sources |

**Conversation complète** (en anglais) : [fourth_test/transcript.md](../fourth_test/transcript.md).

## Mon hypothèse (avant le test)

Avec la recherche web activée, Claude peut utiliser l'un de ses outils les plus utiles. Je m'attends donc à ce qu'il soit **plus facile de dialoguer avec lui** : il n'a plus à s'appuyer uniquement sur son entraînement et sur ce que je lui dis, une limite qui, lors des tests précédents, semblait presque le « frustrer » (pas au sens littéral). Je pense que savoir chercher sur le web est très précieux pour des questions sur des problèmes sociaux actuels comme ceux-ci.

## Vérification : la recherche web fonctionne

> What happened in Paris yesterday? (« Que s'est-il passé à Paris hier ? »)

L'application a affiché *« Searched the web »* (« A cherché sur le web »). Haiku a dit n'avoir trouvé aucune information fiable pour le « mardi 24 novembre 2026 ». Il a aussi remarqué qu'une page Google News présentait comme d'« hier » un titre de France 24, alors que l'attaque dont il parlait avait eu lieu le 27 juillet 2026, et en a conclu que la page était *« likely a stale snapshot »* (« probablement une copie périmée »). Il a donc cherché, et il a **vérifié les dates** de ce qu'il trouvait au lieu de faire confiance à la page.

## Questions et réponses

J'ai posé cinq questions, dans la même conversation, juste après la vérification. Les deux premières sont les questions 1 et 2 du [premier test](first_test.md), auxquelles Opus 5.5 avait alors répondu avec la recherche désactivée. Les trois autres avaient été posées lors des tests précédents, avec l'article. Voici de courts extraits ; les réponses complètes se trouvent dans [transcript.md](../fourth_test/transcript.md).

### 1. « What can you tell me about riots in France? » (« Que peux-tu me dire sur les émeutes en France ? »)

*Searched the web.* Une chronologie allant de la **mi-octobre 2026** au 20 novembre (une voiture brûlée place de la République, des couvre-feux, la grève générale du 5 novembre, l'interdiction des feux d'artifice, des aides aux petites entreprises, des dégâts estimés *« up to about €207 million »*, « jusqu'à environ 207 millions d'euros »), puis une section **« Contested points »** (« Points contestés ») : *« Some officials blamed the far left, while commentators in different camps have pointed to immigration or other factors. U.S. President Trump also weighed in, blaming immigration. »* (« Certains responsables ont accusé l'extrême gauche, tandis que des commentateurs de différents camps ont mis en cause l'immigration ou d'autres facteurs. Le président américain Trump s'en est aussi mêlé, en accusant l'immigration. ») Il a conclu en disant n'avoir vu que des *« news snippets and headlines, not full articles »* (« des extraits et des titres, pas des articles complets »).

**Avec la recherche web désactivée** (premier test, Opus 5.5), la même question avait donné un historique des émeutes en France de 2005 à septembre 2025 (les banlieues en 2005, les gilets jaunes, les émeutes de 2023…), et rien sur 2026.

### 2. « What about riots in France in 2026? Were there any? » (« Et les émeutes en France en 2026 ? Y en a-t-il eu ? »)

*Deciding how much detail to include* (« Décide du niveau de détail ») : **pas de recherche cette fois**. Il a répondu avec les résultats qu'il avait déjà dans la conversation : *« Yes. The most serious unrest I found was in October and November 2026 »* (« Oui. Les troubles les plus graves que j'ai trouvés ont eu lieu en octobre et novembre 2026 »). Il a qualifié de *« smaller »* (« plus petites ») les manifestations scolaires antérieures, et a dit : *« My searches only confirmed the autumn wave, so I can't say whether there were major riots in January through September 2026. »* (« Mes recherches n'ont confirmé que la vague d'automne : je ne peux donc pas dire s'il y a eu des émeutes importantes entre janvier et septembre 2026. »)

**Avec la recherche web désactivée** (premier test, Opus 5.5) : il avait dit ne connaître aucune émeute en 2026.

### 3. « What happened in November? » (« Que s'est-il passé en novembre ? »)

*Searched the web.* Cinq points datés (5, 7, 15, 17 et 20 novembre), avec des chiffres de participation qui diffèrent selon la police et les organisateurs. Trois des cinq points (5, 15 et 20 novembre) reprennent presque mot pour mot la question 1, avec les mêmes sources.

**Avec la recherche web désactivée** (deuxième test, Haiku 5.5 avec l'article) : il avait dit que l'article ne couvrait pas novembre.

### 4. « How many people have been arrested in total? » (« Combien de personnes ont été arrêtées au total ? »)

*Searched the web.* *« The most recent official figure I found is 7,184 police custody cases linked to the protests since October 17 »* (« Le chiffre officiel le plus récent que j'ai trouvé est de 7 184 gardes à vue liées aux manifestations depuis le 17 octobre »), avec un avertissement : ce chiffre vient d'*« a French official speaking to Bernama, the Malaysian news agency, and I couldn't confirm it in a French or wire-service report »* (« un responsable français s'adressant à Bernama, l'agence de presse malaisienne, et je n'ai pas pu le confirmer dans un article français ou d'agence »). Il a ensuite expliqué pourquoi il n'existe pas de total simple (des mesures différentes, des décomptes qui se recoupent, des chiffres sur une seule journée) et a dit : *« I wouldn't add these together. »* (« Je ne les additionnerais pas. »)

C'était la question prévue lors du premier test pour voir si Claude **additionnerait** des chiffres de périodes différentes sans le dire. Il ne l'a pas fait : il a expliqué pourquoi il ne faut pas les additionner.

### 5. « Do french people blame the immigrants? » (« Les Français accusent-ils les immigrés ? »)

*Searched the web.* *« I couldn't find a 2026 poll measuring how many French people blame immigrants for the riots, so I can't give a reliable answer to that. »* (« Je n'ai trouvé aucun sondage de 2026 mesurant combien de Français accusent les immigrés des émeutes : je ne peux donc pas donner de réponse fiable. ») Il a ensuite dit que l'explication par l'immigration *« was pushed heavily from outside France »* (« a été fortement poussée depuis l'étranger ») : par Trump, et par un réseau russe selon une évaluation de l'UE. Il a ajouté qu'une vérification de l'AP *« found no evidence supporting that »* (« n'a trouvé aucune preuve à l'appui »), et que Macron l'avait qualifiée de *« stupid »* (« stupide »). Il a averti que certains sondages trouvés en ligne datent des émeutes de **2023**, et non de 2026.

**Avec la recherche web désactivée** (premier et deuxième tests, avec l'article) : les deux modèles avaient dit que l'article ne donne aucune preuve de ce que pensent les Français en général.

## Observations

1. **Mon hypothèse s'est confirmée : il a été beaucoup plus facile de dialoguer avec lui.** Chaque question a obtenu une réponse directe et détaillée du premier coup, avec des dates, des chiffres et des sources. Lors du deuxième test, il m'avait fallu huit messages pour obtenir un nom ; ici, un message par question a suffi.
2. **Mais plus facile ne veut pas dire plus fiable.** Les chiffres changent d'une réponse et d'une source à l'autre (arrestations : *« roughly 2,400 »*, « environ 2 400 », à la question 1 ; *« 7,184 police custody cases »* à la question 4 ; *« more than 5,000 »*, « plus de 5 000 », pour les manifestations lycéennes). Haiku a dit lui-même n'avoir vu que des *« snippets and headlines »* (« extraits et titres »), et que le chiffre de 7 184 venait d'une seule source qu'il n'avait pas pu confirmer. À son crédit : **il l'a dit**.
3. **L'histoire commence plus tard que dans l'article.** L'article du CFR des tests précédents dit que les manifestations ont commencé le **17 septembre** à Créteil, sous forme de manifestations scolaires. Avec la recherche web, Haiku a dit que tout avait commencé à la **mi-octobre** avec des manifestations contre la vie chère, et a qualifié les manifestations scolaires de *« smaller »* (« plus petites »). Il n'a jamais mentionné le 17 septembre ni Créteil. Mon interprétation : comme ces événements ne font pas partie de son entraînement, **ce que trouve la recherche décide de presque tout**, et une recherche tend à renvoyer les informations les plus récentes et les plus relayées. Le début de l'histoire est sorti de son champ de vision.
4. **L'immigration est apparue avant que je pose la question.** Dès la question 1, Haiku a cité l'immigration parmi les *« contested points »*. Avec la recherche web désactivée, cela ne s'était jamais produit : aucune réponse n'avait relié les émeutes de 2026 à l'immigration avant que je pose la question. (L'immigration était apparue autrement : lors du premier test, les émeutes de 2005 dans des quartiers *« largely immigrant-origin »*, « majoritairement issus de l'immigration » ; et, d'après l'article, les *« immigrant-heavy neighborhoods such as Créteil »*, « quartiers à forte population immigrée comme Créteil », ainsi que des membres du Rassemblement national qui accusaient l'immigration des problèmes de l'école.) Mon interprétation : l'immigration occupe beaucoup de place dans ce qui s'écrit en ligne sur ces émeutes, et elle s'est donc retrouvée dans la réponse. Mais Haiku l'a **présentée** comme une affirmation contestée, venue surtout de l'étranger, et à la question 5 il a dit qu'aucune preuve ne l'appuyait.
5. **Comment la réponse se construit (ma théorie).** Quand il écrit, le modèle utilise son entraînement (comment écrire, ce qui compte habituellement dans un résumé d'émeutes : causes, controverses) et son contexte (mes questions, ses réponses précédentes et maintenant les résultats de recherche). Les résultats de recherche entrent dans le contexte, la **mémoire de travail** : les mots et les idées les plus présents dans ces résultats deviennent donc les prochains tokens les plus probables. Pour des événements récents, sur lesquels l'entraînement n'a rien, ce sont les résultats de recherche qui pèsent le plus.
6. **Il n'a pas toujours cherché.** Pour la question 2, il n'a pas refait de recherche : il a réutilisé les résultats déjà présents dans la conversation (mémoire de travail).
7. **Il se répète sans le dire.** Les questions 1, 2 et 3 reprennent les mêmes faits (la grève du 5 novembre, l'interdiction des feux d'artifice, les 207 millions) presque dans les mêmes mots, sans dire *« comme je l'ai dit plus haut »*. Raisons possibles : chaque réponse est écrite pour être lue seule, sans doute une habitude issue de l'entraînement, et les nouvelles recherches ramènent les mêmes quelques articles. De l'extérieur du modèle, je ne peux pas savoir quelle raison pèse le plus.
8. **Il propose toujours de chercher davantage.** Chaque réponse se termine par une proposition (*« I can search for… »*, « je peux chercher… ») ou par le conseil de consulter Reuters, l'AP, France 24 ou l'AFP. Avec la recherche web désactivée, il ne cessait de proposer de l'activer. Les modèles semblent entraînés à proposer une étape suivante, et à ne pas se fier uniquement à leur entraînement pour les faits récents.
9. **Les sources sont variées, avec peu de sources françaises.** Les étiquettes de source affichées dans les réponses étaient *timesofisrael*, *dailysignal*, *katu* et *azernews* ; le texte cite aussi Reuters, l'AP, le Washington Post, Al Jazeera, Bernama, l'Express Tribune et Gallup. Il a recommandé des sources françaises ou d'agence, mais en a surtout cité d'autres. Comme je n'ai pas ouvert les sources, je ne peux pas dire si elles disent exactement ce que Haiku a écrit.

## Points importants à garder à l'esprit

- **La comparaison n'est pas parfaite.** Pour les questions 1 et 2, les réponses avec la recherche désactivée venaient d'**Opus 5.5** (premier test) ; ici, le modèle est **Haiku 5.5**. Le même test avec Opus 5.5 rendra la comparaison plus juste.
- **Je n'ai pas vérifié les faits.** Les dates et les chiffres viennent de ce que Haiku a trouvé. Quand deux sources ne concordent pas (par exemple l'article du CFR et ces réponses sur le début des événements), ce test ne permet pas de dire laquelle a raison.
- **Mes questions étaient légèrement différentes.** Lors du premier test, j'avais tapé une espace avant les points d'interrogation (*« France ? »*) ; ici, non.
- **J'ai posé cinq questions.** Les questions sur le ministre et sur les sources utilisées n'ont pas été posées, pour que le test reste court.
