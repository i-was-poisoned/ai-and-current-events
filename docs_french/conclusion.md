# Conclusion

← [Retour au document principal](README.md)

*Traduction de [conclusion.md](../conclusion.md).*

Au fil de quatre tests, j'ai interrogé Claude (Opus 5.5 et Haiku 5.5) sur les manifestations et les émeutes en France à l'automne 2026, des événements survenus **après** leur entraînement. D'abord avec la recherche web désactivée, puis avec un article de presse, ensuite avec des questions répétées, et enfin avec la recherche web activée. Voici ce que j'ai appris.

## 1. Quand il ne savait pas, il le disait

Avec la recherche web désactivée, Claude ne savait rien des événements de 2026, et il l'a **dit** au lieu d'inventer quelque chose. Il n'a pas essayé de « combler les trous » avec des informations qu'il n'avait pas. En termes de prédiction du prochain token, la suite la plus probable qu'il a apprise pendant l'entraînement était « je ne sais pas », et non une réponse inventée.

Cela montre aussi une limite : je ne peux pas « apprendre » quelque chose de nouveau au modèle au cours d'une conversation. Ce que je peux faire, c'est lui donner des informations (un article) ou le laisser chercher. Dans les deux cas, la nouvelle information n'existe que dans la conversation, pas dans le modèle.

## 2. Les outils font partie du contexte

Avec la recherche web désactivée, Claude me demandait souvent de l'activer, surtout Haiku. Il traitait tout ce qu'il disait sur l'actualité comme une supposition, et disait qu'il serait **plus fiable** avec la recherche web activée. Même quand j'ai essayé de l'orienter dans l'autre sens en lui disant que je ne voulais pas l'activer, il a continué à le proposer. C'est probablement un comportement appris lors de l'ajustement (*fine-tuning*) : le modèle a conscience des limites de ses connaissances et sait quel outil les comble.

Pour moi, c'est l'une des découvertes les plus importantes : **le contexte (la mémoire de travail) ne se construit pas seulement à partir de ce que j'écris, mais aussi des outils que je permets au modèle d'utiliser.** Activer ou désactiver la recherche web change ce que le modèle peut savoir dans une conversation. De tous ses outils, la recherche web est l'un des plus importants pour l'actualité.

## 3. Ce qui se trouve dans le contexte influence fortement les tokens suivants

À plusieurs reprises, ce qui était déjà dans la conversation a façonné la réponse :

- Lors du deuxième test, Haiku a introduit Jean-Michel Blanquer dans la conversation par erreur, puis a donné son nom comme le ministre le plus récent qu'il connaissait, avec environ quatre ans de retard. Dans une conversation vierge (troisième test), il a cité le bon ministre 7 fois sur 8.
- Avec la recherche web activée, les réponses se sont surtout construites à partir de ce que la recherche trouvait. Des sujets fréquents en ligne, comme l'immigration, pouvaient apparaître avant que je pose la question.

Le modèle ne se contente pas de répondre à ma question : il prolonge tout ce qu'il peut voir.

## 4. Des erreurs peuvent apparaître même avec une source

Quand j'ai donné à Claude un article de presse, la plupart de ses réponses s'y sont tenues, mais certains détails ont malgré tout été **inventés ou ajoutés**. Quand il ne voyait que les adresses web des sources de l'article, il en a conclu que les manifestations avaient commencé « vers le 1er octobre » (l'article dit le 17 septembre), et quelques détails issus de son entraînement se sont glissés sans avertissement.

Je ne suis pas tout à fait sûr de la raison, mais je pense que c'est ce qui se passe quand **la prédiction du prochain token rencontre un trou dans les connaissances** : quand le modèle ne voit qu'une partie de l'information, il comble le vide avec ce qui lui semble le plus probable, et le résultat peut paraître plausible tout en étant faux.

## 5. Sans recherche, les questions qui changent avec le temps étaient difficiles

Avec la recherche web désactivée, Claude refusait parfois de répondre à des questions dont la réponse change avec le temps, comme le nom du ministre de l'Éducation en France. Lors du deuxième test, il a fallu huit messages pour obtenir un nom, et ce nom n'était plus à jour. Lors du troisième test, une seule question claire a suffi : la formulation de la question compte (pilotabilité).

## 6. Les deux modèles sont nettement différents

Haiku 5.5 a donné des réponses plus courtes, dans un autre style d'écriture, avec davantage de listes. Il s'est aussi contredit plus souvent, a été moins constant d'un essai à l'autre et, avec la recherche web activée, a raconté une histoire moins complète. Dans ces tests, **Haiku a semblé moins fiable qu'Opus** pour des questions sur l'actualité sociale. Opus a donné des réponses plus longues et plus prudentes, a mieux suivi la conversation et a dit plus clairement d'où venaient ses informations. Ces conclusions reposent sur un petit nombre de questions et d'essais.

## 7. Avec tous ses outils, travailler avec l'IA est beaucoup plus facile, mais pas sans erreurs

Avec la recherche web activée, presque toutes les questions ont obtenu une réponse directe et détaillée du premier coup. Les réponses venaient **surtout de la recherche, et non de l'entraînement**, même si l'entraînement a sans doute servi à structurer les phrases et à comprendre l'information, par exemple qu'« interpellation » et « garde à vue » ne sont pas la même chose.

Mais il y a eu des erreurs dans chaque test : des dates fausses, des contradictions, des noms dépassés et des chiffres qui changeaient d'une source à l'autre. Les modèles n'ont donc pas toujours raison. La meilleure façon de travailler avec l'IA est d'**exploiter ses forces et de gérer ses faiblesses** :

- activer les outils dont elle a besoin (pour l'actualité, la recherche web) ;
- lui donner un bon contexte, en se rappelant que tout ce qui se trouve dans la conversation influence la réponse ;
- poser des questions claires, et les poser plusieurs fois quand c'est important ;
- vérifier soi-même les faits importants dans les sources.

## Les quatre notions, en une phrase chacune

- **Prédiction du prochain token :** le modèle écrit toujours la suite la plus probable ; quand une information manque, cette suite peut être « je ne sais pas », ou un détail plausible mais faux.
- **Connaissances :** l'entraînement s'arrête à une date limite ; ensuite, le modèle ne peut savoir que ce que lui apportent la conversation ou ses outils.
- **Mémoire de travail :** tout ce qui se trouve dans la conversation (mes mots, ses réponses précédentes, les documents et les résultats de recherche) façonne la suite, parfois plus que son entraînement.
- **Pilotabilité :** la formulation d'une question et les outils que j'autorise changent beaucoup la réponse, mais insister davantage ne mène pas toujours à une meilleure réponse.
