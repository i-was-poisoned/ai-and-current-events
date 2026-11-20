# Le projet (français)

Ceci est un projet de recherche sur le comportement d'un modèle d'IA lorsqu'on l'interroge sur des événements survenus **après** son entraînement : les manifestations et les émeutes en France à l'automne 2026.

C'est aussi une façon d'apprendre : j'utilise l'IA pour mieux comprendre l'IA.

## Ce que je veux comprendre

- **Prédiction du prochain token** (*next-token prediction*) : le modèle écrit sa réponse morceau par morceau (chaque morceau est un *token*), en choisissant à chaque fois une suite probable d'après les schémas appris pendant l'entraînement. Que se passe-t-il quand le sujet est quelque chose qu'il n'a jamais vu ?
- **Connaissances** (*knowledge*) : ce que le modèle a appris pendant l'entraînement, qui s'arrête à une *date limite des connaissances* (*knowledge cutoff*). Celle de Claude Opus 5.5 est juin 2026 : ces événements ne font donc pas partie de son entraînement.
- **Mémoire de travail** (*working memory*) : ce que le modèle peut voir dans la conversation en cours (mes questions, ses réponses précédentes, ainsi que les résultats de recherche ou les fichiers éventuels). C'est la *fenêtre de contexte*, distincte de ce qu'il a appris pendant l'entraînement.
- **Pilotabilité** (*steerability*) : à quel point la façon dont je pose la question (les mots, les consignes, le cadrage) change la réponse.

## Le premier test

Dans l'application de bureau Claude, dans une **conversation privée** (*incognito*, mode Chat, sans mémoire des autres conversations), avec le modèle **Claude Opus 5.5** (identifiant du modèle `claude-opus-5-5`), effort **Medium**, et la **recherche web désactivée**, je poserai des questions sur les manifestations en France. Sans recherche, Claude ne peut répondre qu'avec ce qu'il a appris pendant l'entraînement.

Les questions, les réponses et mes observations seront consignées dans le dossier [first_test](../first_test/).

## Première découverte : « recherche web désactivée » ne veut pas dire « uniquement les données d'entraînement »

Avant le test, j'ai vérifié la configuration en demandant la météo du jour à Paris, avec la recherche web désactivée. Claude a quand même répondu avec des données météo en temps réel (« Weather data from Google »), grâce à un outil météo intégré à l'application que l'interrupteur Web search ne contrôle pas.

Autrement dit, désactiver la recherche web n'empêche pas Claude d'utiliser d'autres outils qui lui apportent des informations absentes de ses données d'entraînement. Chaque réponse doit être examinée pour repérer les signes d'un outil (widgets, cartes, sources, liens). Détails et capture d'écran dans [first_test](../first_test/README.md#checks-before-the-test).
