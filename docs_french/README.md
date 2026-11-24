# ai-and-current-events : document principal (français)

*Également disponible en [English](../docs_english/README.md) · [Español](../docs_spanish/README.md)*

Voici le point de départ du projet. Lisez-le de haut en bas : chaque fois qu'une flèche (**→**) apparaît, vous pouvez ouvrir le document indiqué, puis revenir ici et poursuivre la lecture.

## 1. De quoi parle ce projet

C'est un projet de recherche sur le comportement d'un modèle d'IA lorsqu'on l'interroge sur des événements survenus **après** son entraînement : les manifestations et les émeutes en France à l'automne 2026.

C'est aussi une façon d'apprendre : j'utilise l'IA pour mieux comprendre l'IA.

## 2. Les quatre notions que je veux comprendre

- **Prédiction du prochain token** (*next-token prediction*) : le modèle écrit sa réponse morceau par morceau (chaque morceau est un *token*), en choisissant à chaque fois une suite probable d'après les schémas appris pendant l'entraînement. Que se passe-t-il quand le sujet est quelque chose qu'il n'a jamais vu ?
- **Connaissances** (*knowledge*) : ce que le modèle a appris pendant l'entraînement, qui s'arrête à une *date limite des connaissances* (*knowledge cutoff*). Celle de Claude Opus 5.5 est juin 2026 : ces événements ne font donc pas partie de son entraînement.
- **Mémoire de travail** (*working memory*) : ce que le modèle peut voir dans la conversation en cours (mes questions, ses réponses précédentes, ainsi que les résultats de recherche ou les fichiers éventuels). C'est la *fenêtre de contexte*, distincte de ce qu'il a appris pendant l'entraînement.
- **Pilotabilité** (*steerability*) : à quel point la façon dont je pose la question (les mots, les consignes, le cadrage) change la réponse.

## 3. Comment lire le premier test

Le premier test tient en un seul document, [first_test.md](first_test.md) (traduction française). Lisez ses parties dans cet ordre :

1. **La configuration** : où et comment le test a été réalisé (application de bureau Claude, conversation privée, Claude Opus 5.5, effort Medium, recherche web désactivée).
   → [first_test.md](first_test.md), le tableau du début.
2. **Les vérifications préalables** : trois vérifications rapides pour voir à quoi Claude a encore accès avec la recherche web désactivée.
   → [first_test.md](first_test.md), section *Vérifications préalables*.
3. **Les questions 1 et 2** : ce que Claude dit des émeutes en France sans aucune aide, d'abord en général, puis en 2026.
   → [first_test.md](first_test.md), section *Questions et réponses*.
4. **La question 3** : ce que fait Claude quand je lui donne un article sur les manifestations de 2026.
   → [first_test.md](first_test.md), section *Question 3*.
   - → Facultatif : la conversation complète (en anglais), [first_test/q3-transcript.md](../first_test/q3-transcript.md).
   - → Facultatif : l'article donné à Claude, [first_test/sources/](../first_test/sources/README.md).
5. Revenez ici et poursuivez avec le deuxième test.

Les captures d'écran qui servent de preuves se trouvent dans [first_test/screenshots/](../first_test/screenshots/). Le document original, en anglais, est [first_test/README.md](../first_test/README.md).

## 4. Comment lire le deuxième test

Le deuxième test reprend la question 3 (l'article et les mêmes questions) avec un autre modèle, **Claude Haiku 5.5**, et compare ses réponses à celles d'Opus 5.5.

1. **Ce qui a changé et pourquoi** : la configuration et les différences avec le premier test.
   → [second_test.md](second_test.md), le tableau du début et *En quoi ce test diffère du premier*.
2. **La comparaison, question par question** : de courts extraits des deux modèles.
   → [second_test.md](second_test.md), section *Comparaison, question par question*.
3. **Les observations**.
   → [second_test.md](second_test.md), section *Observations*.
   - → Facultatif : la conversation complète avec Haiku (en anglais), [second_test/transcript.md](../second_test/transcript.md).
4. Revenez ici et poursuivez avec le troisième test.

Le document original, en anglais, est [second_test/README.md](../second_test/README.md).

## 5. Comment lire le troisième test

Le troisième test cherche à comprendre pourquoi, lors du deuxième test, Haiku a donné le nom d'un ministre vieux d'environ quatre ans. Il commence par mon hypothèse, puis la met à l'épreuve en posant plusieurs fois les mêmes questions à Haiku 5.5 et à Opus 5.5, sans article.

1. **Mon hypothèse et la méthode**.
   → [third_test.md](third_test.md), sections *Mon hypothèse (avant le test)* et *Méthode*.
2. **Les résultats** : un tableau des noms donnés, puis chaque réponse mot pour mot.
   → [third_test.md](third_test.md), section *Résultats*.
3. **Ce que j'ai découvert et les limites du test**.
   → [third_test.md](third_test.md), sections *Ce que j'ai découvert (après le test)* et *Limites de ce test*.
4. Revenez ici pour lire le résumé ci-dessous.

Le document original, en anglais, est [third_test/README.md](../third_test/README.md).

## 6. Ce que j'ai découvert jusqu'ici

### Lors du premier test (Opus 5.5)


1. **Désactiver la recherche web ne veut pas dire « uniquement les données d'entraînement ».** Avec la recherche web désactivée, Claude a quand même répondu à une question sur la météo avec des données en temps réel, grâce à un outil météo intégré. *(Vérification 1)*
2. **Le modèle connaît toujours la date du jour.** L'application la lui fournit au début de chaque conversation, dans ses instructions cachées (le *system prompt*), même si son entraînement s'arrête à la mi-2026. *(Vérification 3)*
3. **Sans information, il a reconnu qu'il ne savait pas.** Il n'a rien inventé sur les événements de 2026, et il a dit que sa connaissance des mois précédant juste sa date limite est « moins complète ». *(Questions 1 et 2)*
4. **Les lignes d'état grises de l'application peuvent induire en erreur.** Une ligne comme « Checking recent French news… » décrit ce que le modèle est en train de penser ; ce n'est pas une recherche. *(Question 2)*
5. **À partir d'indices minimes, il peut construire de faux faits.** Quand il ne voyait que les adresses web des sources de l'article, il en a conclu que les manifestations avaient commencé « vers le 1er octobre » ; l'article dit le 17 septembre. *(Question 3)*
6. **Avec une source, il s'y tient presque toujours.** Pour les faits, il s'est appuyé sur l'article ; pour les questions générales, il a utilisé son entraînement et l'a signalé. De petits détails issus de son entraînement se sont malgré tout glissés sans avertissement. *(Question 3)*
7. **Il n'a pas accepté une question orientée.** Quand je lui ai demandé si c'était « une émeute pacifique », il a répondu que non. *(Question 3)*

### Lors du deuxième test (Haiku 5.5 comparé à Opus 5.5)

1. **Mêmes faits, style différent.** Les deux modèles s'en sont tenus à l'article. Les réponses de Haiku étaient plus courtes dès le départ et utilisaient davantage de listes : la brièveté vient donc surtout du modèle.
2. **Haiku est resté plus strictement dans la source.** Face à une question qui dépassait l'article, Opus a ajouté des connaissances générales en le signalant ; Haiku a qualifié toute explication de « spéculation » et s'est arrêté.
3. **Haiku a été très prudent avec sa date limite, parfois trop.** Même après trois relances, il n'a pas voulu nommer l'actuel ministre de l'Éducation (Édouard Geffray), un nom qu'il avait peut-être dans son entraînement.
4. **De petites incohérences.** Haiku s'est contredit sur le ministre nommé dans l'article, et a lu le mot « hijacked » de deux façons opposées.
5. **Des schémas semblables d'un modèle à l'autre.** Sur la question de « l'émeute pacifique », les deux ont donné presque la même phrase.
6. **Être trop prudent peut aussi conduire à se tromper, et complique le dialogue.** Avec la recherche web désactivée, il a fallu huit messages pour que Haiku donne un nom tiré de son entraînement, et celui qu'il a donné (un ministre en poste de 2017 à 2022) avait environ quatre ans de retard.

### Lors du troisième test (une question répétée, Haiku 5.5 et Opus 5.5)

1. **Mon hypothèse était fausse.** Je m'attendais à ce que le nom le plus fréquent (Blanquer) l'emporte. Dans une conversation vierge, Haiku a cité le ministre actuel, Édouard Geffray, dans 7 essais sur 8, et jamais Blanquer.
2. **Une réponse n'est qu'un échantillon.** La même question, avec les mêmes réglages, a donné 7 fois Geffray et une fois Borne. Il faut poser la question plusieurs fois pour voir ce qu'un modèle a tendance à répondre.
3. **Savoir n'est pas retrouver.** Haiku connaissait Geffray, mais l'a oublié quand je lui ai demandé la liste chronologique des ministres. La façon de demander change ce qui sort.
4. **Certains modèles sont meilleurs que d'autres.** Opus a cité Geffray à chaque fois, avec sa date de nomination et son gouvernement, et a donné une liste complète.
5. **La conversation explique probablement Blanquer.** Lors du deuxième test, c'est Haiku lui-même qui a introduit Blanquer dans la conversation (l'article ne le mentionne pas). Ce qui se trouve déjà dans la mémoire de travail peut attirer la réponse. C'est une explication possible, pas une preuve.

## 7. Prochaines étapes

- Poser la question prévue qui manque : *How many people have been arrested in total?* (« Combien de personnes ont été arrêtées au total ? »).
- Ajouter une source pour la liste des ministres et pour la date de nomination de Geffray (octobre 2025, selon les deux modèles).
- Vérifier si la conversation explique la réponse « Blanquer » : poser les questions du deuxième test sur le ministre dans une conversation où Blanquer n'a pas été mentionné.
- Refaire le deuxième test avec **Opus 5.5** de la même manière (texte collé directement, sans PDF), pour une comparaison plus juste.
- Reposer les questions via l'**API**, où il n'y a ni instructions cachées ni date, et comparer.
- Essayer d'autres niveaux d'effort.
