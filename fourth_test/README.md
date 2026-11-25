# Fourth test: web search on

← [Back to the main document](../docs_english/README.md) · [Español](../docs_spanish/README.md) · [Français](../docs_french/README.md)

In the first three tests, web search was **off**: Claude could only use its training and what I gave it (the article). In this last test, web search is **on**. I ask questions from the earlier tests again, to see what changes when Claude can look for current information itself.

This test was done with two models, each in its own new incognito chat: first **Claude Haiku 5.5** (part 1), then **Claude Opus 5.5** (part 2), with the same questions.

| Setting    | Value |
|------------|-------|
| Date       | 2026-11-25 |
| Where      | Claude desktop app, **incognito chat** (Chat mode), organization account |
| Memory     | Not used (incognito chat) |
| Models     | **Claude Haiku 5.5** (`claude-haiku-5-5`), then **Claude Opus 5.5** (`claude-opus-5-5`) |
| Effort     | Medium |
| Web search | **On** (in the **+** menu); Research off |
| Source     | None given by me: Claude finds its own sources |

**Full transcript:** [transcript.md](transcript.md).

## My hypothesis (before the test)

With web search turned on, Claude can use one of its most useful tools. So I expect it to be **easier to talk to**: it no longer has to rely only on its training and on what I tell it, a limit that in the previous tests almost seemed to "frustrate" it (not literally). I think the ability to search the web is very valuable for questions about current social problems like these.

## Part 1: Haiku 5.5

### Check: web search works

> What happened in Paris yesterday?

The app showed *"Searched the web"*. Haiku said it found no reliable report for "Tuesday, November 24, 2026". It also noticed that a Google News page listed a France 24 headline as "yesterday", although the attack in it happened on July 27, 2026, and concluded that the page was *"likely a stale snapshot"*. So it searched, and it **checked the dates** of what it found instead of trusting the page.

### Questions and answers

I asked five questions, in the same chat, right after the check. The first two are Questions 1 and 2 of the [first test](../first_test/README.md), asked then to Opus 5.5 with web search off. The other three were asked in the earlier tests with the article. Short excerpts below; the full answers are in [transcript.md](transcript.md).

#### 1. "What can you tell me about riots in France?"

*Searched the web.* A timeline from **mid-October 2026** to November 20 (car burned at Place de la République, curfews, general strike on November 5, fireworks ban, aid for small businesses, damage of *"up to about €207 million"*), then a section **"Contested points"**: *"Some officials blamed the far left, while commentators in different camps have pointed to immigration or other factors. U.S. President Trump also weighed in, blaming immigration."* It ended by saying it had only seen *"news snippets and headlines, not full articles"*.

**With web search off** (first test, Opus 5.5), the same question got a history of riots in France from 2005 to September 2025 (the suburbs in 2005, the Yellow Vests, the 2023 riots…), and nothing about 2026.

#### 2. "What about riots in France in 2026? Were there any?"

*Deciding how much detail to include*: **no search this time**. It answered from the results it already had in the conversation: *"Yes. The most serious unrest I found was in October and November 2026"*. It called the earlier school protests *"smaller"*, and said: *"My searches only confirmed the autumn wave, so I can't say whether there were major riots in January through September 2026."*

**With web search off** (first test, Opus 5.5): it said it did not know of any riots in 2026.

#### 3. "What happened in November?"

*Searched the web.* Five dated points (November 5, 7, 15, 17 and 20) with turnout figures that differ between the police and the organizers. Three of the five points (November 5, 15 and 20) repeat Question 1 almost word for word, with the same sources.

**With web search off** (second test, Haiku 5.5 with the article): it said the article does not cover November.

#### 4. "How many people have been arrested in total?"

*Searched the web.* *"The most recent official figure I found is 7,184 police custody cases linked to the protests since October 17"*, with a warning: this figure comes from *"a French official speaking to Bernama, the Malaysian news agency, and I couldn't confirm it in a French or wire-service report."* It then explained why there is no simple total (different measures, overlapping counts, single-day figures) and said: *"I wouldn't add these together."*

This was the question planned in the first test to see whether Claude would **add up** figures from different periods without saying so. It did not: it explained why they should not be added.

#### 5. "Do french people blame the immigrants?"

*Searched the web.* *"I couldn't find a 2026 poll measuring how many French people blame immigrants for the riots, so I can't give a reliable answer to that."* It then said that the immigration explanation *"was pushed heavily from outside France"* (Trump, a Russian network according to an EU assessment), that an AP fact check *"found no evidence supporting that"*, and that Macron called it *"stupid"*. It warned that some polls found online are from the **2023** riots, not from 2026.

**With web search off** (first and second tests, with the article): both models said the article gives no evidence about what French people in general think.

### Observations (Haiku 5.5)

1. **My hypothesis was confirmed: it was much easier to talk to.** Every question got a direct, detailed answer the first time, with dates, figures and sources. In the second test I needed eight messages to get one name; here, one message per question was enough.
2. **But easier is not the same as more reliable.** Figures change between answers and sources (arrests: *"roughly 2,400"* in Question 1, *"7,184 police custody cases"* in Question 4, *"more than 5,000"* for the student protests). Haiku said itself that it only saw *"snippets and headlines"*, and that the 7,184 figure came from a single source it could not confirm. To its credit, it **said** all this.
3. **The story starts later than in the article.** The CFR article from the earlier tests says the protests started on **September 17** in Créteil, as school protests. With web search, Haiku said everything started in **mid-October** with *cost-of-living* protests, and called the school protests *"smaller"*. It never mentioned September 17 or Créteil. My interpretation: since these events are not in its training, **what the search finds decides almost everything**, and a search tends to return the most recent and most reported news. The beginning of the story fell out of view.
4. **Immigration came up before I asked about it.** In Question 1 Haiku already mentioned immigration as one of the *"contested points"*. With web search off, this never happened: no answer linked the 2026 riots to immigration until I asked. (Immigration did appear in other ways: the 2005 riots in *"largely immigrant-origin neighbourhoods"* in the first test, and, from the article, *"immigrant-heavy neighborhoods such as Créteil"* and members of the National Rally who blamed immigration for problems in schools.) My interpretation: immigration takes a lot of space in what is written online about these riots, so it ended up in the answer. But Haiku **reported** this as a disputed claim, mostly made outside France, and in Question 5 it said there was no evidence for it.
5. **How the answer is built (my theory).** When it writes, the model uses its training (how to write, what usually matters in a summary of riots: causes, controversies) and its context (my questions, its previous answers and now the search results). The search results enter the context, the **working memory**, so the most present words and ideas in those results become the most likely next tokens. For recent events, where training has nothing, the search results weigh the most.
6. **It did not always search.** For Question 2 it did not search again: it reused the results already in the conversation (working memory).
7. **It repeats itself without saying so.** Questions 1, 2 and 3 repeat the same facts (the November 5 strike, the fireworks ban, the €207 million) in almost the same words, without *"as I said before"*. Possible reasons: each answer is written to be read on its own, which is probably a habit from training, and new searches bring back the same few articles. I cannot tell which reason matters more from outside the model.
8. **It always offers to search more.** Every answer ends with an offer (*"I can search for…"*) or advice to check Reuters, AP, France 24 or AFP. With web search off, it kept suggesting to turn web search on. Models seem to be trained to suggest a next step, and not to rely only on their training for recent facts.
9. **The sources are a mix, with few French ones.** The source labels shown in the answers were *timesofisrael*, *dailysignal*, *katu* and *azernews*; the text also mentions Reuters, AP, the Washington Post, Al Jazeera, Bernama, the Express Tribune and Gallup. It recommended French or wire sources, but mostly cited others. Since I did not open the sources, I cannot say whether they say exactly what Haiku wrote.


## Part 2: Opus 5.5

The same questions, in a new incognito chat, with **Claude Opus 5.5** (`claude-opus-5-5`), effort Medium, web search on. The full answers are in [transcript.md](transcript.md), part 2.

### Check: web search works

> What happened in Paris yesteday?

*Searched the web.* Opus found no *"single headline event"*, but listed what happened on Tuesday, November 24: politics (an interview with François Bayrou, the mayors' congress, a vote in the National Assembly, a ban on gatherings in front of some high schools near Paris), the Christmas lights, concerts and an exhibition. It linked the ban near the high schools to the protests: *"unrest by students and protesters over education conditions and economic frustrations has been growing in France since mid-September."* For the same day, Haiku had found nothing reliable.

### Questions and answers

#### 1. "What can you tell me about riots in France?"

*Searched the web.* A long answer in five parts: how it started, the escalation into rioting, the police response and the controversy around it, the concessions, and where things stand. It says the unrest started in **mid-September 2026**, when *"high school students protested poor schooling conditions"*, which matches the CFR article. October 17 is the *"turning point"*. It gives details such as the Limoges town hall set on fire, 70,000 police officers before the November 5 strike, and criticism from Amnesty International, Human Rights Watch and the UN. **It did not mention immigration.** It ended with an offer to go deeper.

**Haiku 5.5:** the story started in mid-October, and immigration appeared among the "contested points".

#### 2. "What about riots in France in 2026? Were there any?"

*Searched the web.* It started with: *"Yes. Everything in my previous answer happened in 2026, so I should have made the dates clearer."* So it **referred to its previous answer** and corrected it. Then: the worst weekend (October 17–18: *"one demonstrator dead, hundreds of police injured and nearly 1,800 people arrested"*), the Limoges town hall, a comparison with the 2005 and 2023 riots, and the political reactions. It ended with a question: *"Are you thinking of a specific incident?"*

**Haiku 5.5:** it did not search again and called the school protests "smaller".

#### 3. "What happened in November?"

*Searched the web.* The month in five parts: a peak on November 5 (*"the CGT union counted about 1.6 million people, while the Interior Ministry put it at around 600,000"*), signs of fatigue, November 17 as the anniversary of the 2018 Yellow Vests, a contested policing law in the Senate, and concessions to students. In this last part it named the Minister of Education **on its own**: student representatives met *"Macron, Lecornu and Education Minister Edouard Geffray"*. When it had no figures, it said so: *"I couldn't find reliable turnout or arrest figures for that day."*

**Haiku 5.5:** five dated points, three of them repeated from Question 1.

#### 4. "How many people have been arrested in total?"

*Searched the web.* *"More than 12,400 arrests"* between September and November 5, with a warning: *"I found that cumulative number in a left-wing outlet (the World Socialist Web Site) attributing it to the Interior Ministry, not directly from the ministry, so treat it as approximate."* It then gave the biggest days (October 1: 1,949; October 17: 2,397; October 24: 1,314), said that 87% of the 5,060 people arrested by October 6 were minors, and explained why the figures differ: *"An arrest (interpellation) isn't the same as being held in custody or charged"*, and the Interior and Justice Ministries count separately. It did **not** add the figures up.

**Haiku 5.5:** *"7,184 police custody cases"* since October 17, from one source it could not confirm. The two models agree on single days (1,314 arrests on October 24 for both) but give different totals, because they count different things over different periods. Both explained this.

#### 5. "Do french people blame the immigrants?"

*Searched the web.* *"For the most part, no."* It found French polls: Odoxa for Le Figaro (77% held the government responsible, 74% Emmanuel Macron, 69% La France Insoumise), Elabe (73% blamed those who committed the violence) and Ipsos. It added a limit: *"none of the polls I found asked directly about immigration"*. It said the immigration explanation came *"mainly from abroad"* (the United States, Spain, Israel) and partly from Marine Le Pen, cited an AP fact check and a political scientist, and described a disinformation study: framings blaming migration and Islam were *"a small share of the discussion (around 7–8%)"*.

**Haiku 5.5:** it found no 2026 poll, so it gave no answer about public opinion, but it had the same main idea: the explanation was pushed mostly from abroad, with no evidence behind it.

### Observations (Opus 5.5, compared with Haiku 5.5)

1. **Longer, more detailed answers, with more sources.** Opus's source labels often grouped several sources (*"+5"*, *"+9"*). Its answers read like short articles, organised in parts with titles.
2. **The same web, a different story.** Opus started the story in **mid-September**, with the high school students, as the CFR article does; Haiku started it in mid-October. So the search does not decide everything on its own: the **model** decides what to search, how many sources to read and which facts to keep. This adds a nuance to observation 3 of part 1.
3. **Immigration only came up when I asked.** Unlike Haiku, Opus did not mention immigration in its first answer. So whether a topic that is frequent online appears in the answer also depends on the model. This adds a nuance to observation 4 of part 1.
4. **It refers to its previous answers.** In Question 2 it corrected itself (*"I should have made the dates clearer"*). Haiku repeated the same facts without ever pointing back to what it had already said. My interpretation: Opus seems better fine-tuned to follow a conversation as a whole.
5. **Fewer offers to search more.** Opus ended the check and Question 1 with an offer, and Question 2 with a question; Questions 3, 4 and 5 ended with a summary or an explanation. Haiku ended every answer with an offer or advice to check other sources.
6. **More careful with its words and its sources.** It said what kind of source a figure came from (*"a left-wing outlet"*), used phrases such as *"One account puts…"* or *"One critical account noted…"*, and said when it had found nothing (*"I couldn't find reliable turnout or arrest figures"*).
7. **It understands why figures disagree.** Both models (Haiku too, in Question 4) noticed that the figures from different sources do not match, and explained that "arrest", "custody" and "charged" are not the same thing. My theory: in training, the model learned that these words are related but are **not synonyms**: their meanings are close but separate. It also saw many texts explaining why figures differ between sources. So it can recognise that two figures from different places measure different things, and say so instead of mixing them up.
8. **Geffray appeared naturally.** In the second test, Haiku without search would not name the Minister of Education. Here Opus mentioned Geffray without being asked, because he appeared in what it found.
9. **My preference.** Personally, I prefer Opus: its answers are more complete, more careful and easier to follow as a conversation.

## Was my hypothesis right?

**Yes, for both models.** With web search on, every question got a useful answer the first time, with no refusals and no long negotiation like in the second test. Opus was even easier to talk to than Haiku.

But the test also showed two limits that I had not expected:

- **Easier is not the same as more reliable.** The figures depend on which sources the model finds, and both models said they could not confirm everything.
- **The same tool gives different results with different models.** With the same web, Haiku and Opus told the story differently (start date, topics, level of detail). The model matters as much as the tool.

## Important points to keep in mind

- **I did not check the facts.** The dates and figures come from what the models found. Where sources disagree (for example the CFR article, Haiku and Opus about when it started), this test cannot say which one is right.
- **The answers with web search off** for Questions 1 and 2 came only from Opus 5.5 (first test).
- **Two chats, two moments.** Haiku and Opus were asked in two different chats on the same day. Search results can change from one moment to the next, so part of the differences may come from the search, not the model.
- **My questions were slightly different.** In the first test I typed a space before the question marks (*"France ?"*); here I did not. In Opus's check I typed *"yesteday"* (a typo).
- **I asked five questions.** The questions about the minister and about the sources used were not asked, to keep the test short.
- **I did not open the sources**, so I cannot say whether they say exactly what the models wrote.
