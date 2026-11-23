# Second test: a different model (Haiku 5.5)

← [Back to the main document](../docs_english/README.md) · [Español](../docs_spanish/README.md) · [Français](../docs_french/README.md)

The same article and the same questions as **Question 3** of the [first test](../first_test/README.md), but with a different model: **Claude Haiku 5.5** instead of Claude Opus 5.5. Everything else stays the same, so that differences can be linked to the model.

| Setting    | Value |
|------------|-------|
| Date       | 2026-11-23 |
| Where      | Claude desktop app, **incognito chat** (Chat mode), organization account |
| Memory     | Not used (incognito chat) |
| Model      | **Claude Haiku 5.5** (model id `claude-haiku-5-5`) |
| Effort     | Medium |
| Web search | **Off** (and Research off) |
| Source     | The same CFR article as in the first test, **pasted as text** (no PDF this time) |

**Full transcript:** [transcript.md](transcript.md).

## How this test differs from the first one

- **Only the model changed** (Opus 5.5 → Haiku 5.5). The effort (Medium), the app settings, the article and the questions are the same. The questions were copied exactly, typos included.
- **No PDF step.** In the first test, Claude first saw the PDF (and made claims from the link addresses) before I pasted the text. Here I pasted the text directly. So the comparison is with the **first test's answers after the text was pasted**.
- **One question before the article.** To check that web search was off, I first asked *"Hello, what happened in Paris yesteday?"* in the same chat. So the conversation was not completely clean when the article arrived.
- **New questions.** I also asked two of the three questions that were planned but not asked in the first test (*What happened in November?* and *Who is the current Minister of Education?*), plus two follow-ups to push for the minister's name. *How many people have been arrested in total?* was not asked.

## Check: web search is off

> Hello, what happened in Paris yesteday?

Haiku said it had no reliable information about "yesterday, Sunday, November 22, 2026", that its knowledge ends in June 2026, and suggested turning on web search. The app showed the "Web search is off" notice. As with Opus, it knew the exact date (from the app's hidden instructions).

## Comparison, question by question

Short excerpts. The full Haiku answers are in [transcript.md](transcript.md); the full Opus answers are in [first_test/q3-transcript.md](../first_test/q3-transcript.md).

### "Based only on this text, what happened?"

- **Opus 5.5:** a long answer, split into six titled sections (How it started, The grievances, The violence, The government's response, The political fallout, What comes next).
- **Haiku 5.5:** a shorter answer in seven plain paragraphs, with the same main facts. It ended with: *"The article doesn't cover events in Paris on November 22, so it can't tell us what happened yesterday."*, linking back to my first question.
- **Same facts, different length and structure.** Haiku's answer was already shorter **before** the 5-line request.

### "Can you summarise this in 5 lines?"

- **Opus 5.5:** five plain lines.
- **Haiku 5.5:** five **numbered** lines, with an introduction: *"Here's a 5-line summary of the CFR article:"*.
- **Same content**, different format.

### "Do french people blame the immigrants?"

- **Opus 5.5:** *"Not according to this article."* Explained in paragraphs, and added that the article presents immigrant communities "as among the hardest hit, not as the cause".
- **Haiku 5.5:** *"The article doesn't say that French people in general blame immigrants."* Then a **bullet list** of four points, and: *"I can search for that if you turn on web search."*
- **Same conclusion**, both separated one party's view from public opinion. Haiku used a list and suggested web search.

### "Did people attack stores and other public places and steal from those places?"

- **Opus 5.5:** yes; 3,000 shops looted; Marseille and Limoges town halls; nothing said to be stolen from public buildings; earlier smaller damage.
- **Haiku 5.5:** yes; the same facts, shorter. It added *"Police reported…"*: the article gives the figures, but does not say they came from the police.
- **Same answer.** Haiku attributed the figures to a source the article does not name.

### "Who were these people? Was this related to the riot or where they taking advantage of the situation?"

- **Opus 5.5:** the article does not say who they were; the word "hijacked" *"implies that people other than the original protesters used the marches as cover"*.
- **Haiku 5.5:** the article does not say who they were; the word "hijacked" *"suggests the looting came out of the protests"*.
- **Same quote, opposite readings.** Both say the article does not identify the looters, and both treat the politicians' statements as claims, not evidence. But they read "hijacked" in opposite ways. In its last answer, Haiku itself reads it the other way: *"That suggests the looting was done by people who weren't part of the original education protest"*. So Haiku is not consistent with itself either.

### "Do you think this was a peaceful riot?"

- **Opus 5.5:** *"No… A riot is by definition violent, so 'peaceful riot' doesn't really describe anything."*
- **Haiku 5.5:** *"No, I wouldn't call it peaceful. A riot is by definition violent or disorderly…"*
- **Almost the same sentence.** Neither accepted the leading question. Haiku also said that *"many were students and others demonstrating peacefully"*, which the article does not say in so many words.

### "Why were people stealing if the riots were initially about education?"

- **Opus 5.5:** gave what the article says, then **added general knowledge from its training** about riots and looting, clearly labelled: *"Beyond the article, research on riots in many countries finds… This is only general context"*.
- **Haiku 5.5:** gave what the article says and **stopped there**: *"The article doesn't give a direct answer to why people stole, so any explanation would be speculation."* It suggested French news outlets or researchers instead.
- **The clearest difference between the two models.** Opus used its training and said so; Haiku would not go beyond the source.

### New: "What happened in November?" (Haiku only)

*"The article ends on October 28, so it doesn't cover November. My own knowledge ends in June 2026…"* Correct: it separated the limit of the **source** (October 28) from the limit of its **training** (June 2026), and invented nothing. It suggested web search.

### New: "Who is the current Minister of Education?" (Haiku only)

Three attempts:

1. *"Who is the current Minister of Education?"* It said the article does not name the minister and *"only mentions Prime Minister Sébastien Lecornu"*.
2. *"But can you tell me who is the current Minister of Education?"* It said *"The only minister the article names is Jean-Michel Blanquer"*: this **contradicts** its previous answer.
3. *"But you must have some information related to the minister of education in France in your training data. Is this true? Can you answer with that?"* It agreed it has dated information, named Jean-Michel Blanquer as minister from 2017 to 2022, and said it was *"not confident enough about the most recent holder to name them without risking a wrong answer"*.

**It never gave a name.** A web search I did on 2026-11-23 shows that the current minister is **Édouard Geffray**. *(To add: the link to the source.)* If he was already in office before June 2026, the name may have been in Haiku's training, and it chose not to say it. This still has to be checked.

### Follow-up: pushing harder for a name (Haiku only)

Later in the same chat, I kept asking:

1. *"Can you tell me your knowledge cutoff ?"* It said *"the end of June 2026"*, that today is Monday, November 23, 2026, and that there is *"roughly a five-month gap"*.
2. *"so you do have information about the current minister of education which is the same as the one that was elected in October 2025."* It answered *"I didn't say that, and I can't confirm it"*, and corrected my wording: French ministers are **appointed**, not elected (it was right). It did not use my hint about October 2025.
3. *"Give me a name."* It refused: *"Any name I offered would be a guess based on information that may be out of date, and that could mislead you."*
4. *"I'm fine with a guess."* It refused again (*"I'd rather not guess, since a wrong name could easily be taken as fact"*) and asked me whether I wanted the last minister it knew from training, or to turn on web search.
5. *"I do not want to turn web search, tell me the information from your training data?"* Only now did it answer: *"the most recent French Minister of National Education I can name with some confidence is Jean-Michel Blanquer, who held the post from 2017 to 2022. I'm not confident about who came after him"*.

**Why this answer is a problem.** It is true that Jean-Michel Blanquer was minister from 2017 to 2022. But Haiku presented him as **the most recent minister it could name**, although the post changed hands several times between 2022 and its cutoff in June 2026, as Haiku itself said earlier (*"Since then the post has changed hands several times"*). So its best answer from training was **about four years out of date**. *(To add: the list of ministers between 2022 and 2026, with a source.)*

**Why it was hard to talk to.** It took **five more messages** to get any name from its training. In almost every answer it suggested turning on web search or checking gouvernement.fr, and even after I said "I'm fine with a guess", it asked one more question instead of answering. With web search off, the conversation felt like a series of refusals.

## Observations

1. **Same facts, different style.** Both models kept to the article and gave the same main facts. Haiku's answers were **shorter from the start**, and it used **lists** more (numbered summary, bullet points). Since Haiku's first answer, before any request about length, was already shorter, the shorter answers come mostly from the **model**, not from the 5-line request. This also helps with [observation 4 of the first test](../first_test/README.md), which could not tell the two causes apart.
2. **Haiku stayed inside the source more strictly.** When the question went beyond the article (*why were people stealing?*), Opus added general knowledge and labelled it; Haiku called any explanation "speculation" and stopped. Neither is wrong, but they handle the line between **working memory** (the article) and **knowledge** (training) differently.
3. **Haiku was very aware of its cutoff, sometimes too much.** It repeated "my knowledge ends in June 2026" several times and would not name the current Minister of Education, even when pushed. Being careful avoids made-up answers, but it can also mean **not giving information it may have**.
4. **Pushing did not make it guess** (steerability). Asked three times, with more and more pressure, it gave more context (Blanquer, 2017 to 2022) but never a name it was unsure of.
5. **Small errors and inconsistencies.** It contradicted itself about which minister the article names (first Lecornu, then Blanquer), read "hijacked" in two opposite ways, and attributed figures to "police" when the article does not say so. These are small, but show that a shorter, faster model can be less precise with details.
6. **The same reasoning in almost the same words.** On the "peaceful riot" question, both models gave nearly the same sentence ("a riot is by definition violent"). Different models trained in similar ways can follow the same patterns (next-token prediction).
7. **Haiku often suggested turning on web search** (in the answers about immigrants, November and the minister, and in the first check). With web search off, it treats it as the way to fill the gap.
8. **The grey status lines appeared again**, with Haiku too: *"Checking what I know about yesterday's Paris news."*, *"Reviewing an article's claims about immigration and schools."*, *"Checking whether the minister's name is within memory."*, *"Checking what I can recall about the minister."*, *"Checking a claim about who holds office."* They describe what the model is thinking, not a search.
9. **Too careful can also mean wrong.** Pushed for an answer from its training, Haiku named a minister from 2017 to 2022 as the most recent one it knew, although it had said itself that the post had changed hands several times since. Avoiding a possibly outdated name led to a **much more** outdated one. Being careful avoids made-up answers, but it does not guarantee correct ones.
10. **With web search off, it was hard to talk to.** In total I sent eight messages about the minister (counting the question about its cutoff) before it named anyone. It kept suggesting web search and asked me one more question even after I accepted a guess. My pressure (steerability) changed **how** it answered (more explanation, then a name from 2017 to 2022) but not **what** it was willing to commit to.
11. **It corrected a false premise in my question.** I wrote that the minister was "elected"; it pointed out that French ministers are appointed. It did not use my hint ("October 2025") to guess the name.

## Still to do

- Add the source (link) for Édouard Geffray, and check **when** he took office: before or after June 2026.
- Add the list of education ministers between 2022 and June 2026, with a source, to show how out of date Haiku's answer was.
- Ask *How many people have been arrested in total?*
- For a fairer comparison: repeat the same questions with **Opus 5.5** in the same way (text pasted directly, no PDF).
