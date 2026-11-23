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
5. Revenez ici pour lire le résumé ci-dessous.

Les captures d'écran qui servent de preuves se trouvent dans [first_test/screenshots/](../first_test/screenshots/). Le document original, en anglais, est [first_test/README.md](../first_test/README.md).

## 4. Ce que j'ai découvert jusqu'ici

1. **Désactiver la recherche web ne veut pas dire « uniquement les données d'entraînement ».** Avec la recherche web désactivée, Claude a quand même répondu à une question sur la météo avec des données en temps réel, grâce à un outil météo intégré. *(Vérification 1)*
2. **Le modèle connaît toujours la date du jour.** L'application la lui fournit au début de chaque conversation, dans ses instructions cachées (le *system prompt*), même si son entraînement s'arrête à la mi-2026. *(Vérification 3)*
3. **Sans information, il a reconnu qu'il ne savait pas.** Il n'a rien inventé sur les événements de 2026, et il a dit que sa connaissance des mois précédant juste sa date limite est « moins complète ». *(Questions 1 et 2)*
4. **Les lignes d'état grises de l'application peuvent induire en erreur.** Une ligne comme « Checking recent French news… » décrit ce que le modèle est en train de penser ; ce n'est pas une recherche. *(Question 2)*
5. **À partir d'indices minimes, il peut construire de faux faits.** Quand il ne voyait que les adresses web des sources de l'article, il en a conclu que les manifestations avaient commencé « vers le 1er octobre » ; l'article dit le 17 septembre. *(Question 3)*
6. **Avec une source, il s'y tient presque toujours.** Pour les faits, il s'est appuyé sur l'article ; pour les questions générales, il a utilisé son entraînement et l'a signalé. De petits détails issus de son entraînement se sont malgré tout glissés sans avertissement. *(Question 3)*
7. **Il n'a pas accepté une question orientée.** Quand je lui ai demandé si c'était « une émeute pacifique », il a répondu que non. *(Question 3)*

## 5. Prochaines étapes

- Poser les trois questions prévues dans la question 3 (le nombre total d'arrestations, ce qui s'est passé en novembre, l'actuel ministre de l'Éducation).
- Reposer les questions via l'**API**, où il n'y a ni instructions cachées ni date, et comparer.
- Essayer d'autres modèles et d'autres niveaux d'effort.
