# Fourth test: web search on

← [Back to the main document](../docs_english/README.md) · [Español](../docs_spanish/README.md) · [Français](../docs_french/README.md)

In the first three tests, web search was **off**: Claude could only use its training and what I gave it (the article). In this last test, web search is **on**. I ask questions from the earlier tests again, to see what changes when Claude can look for current information itself.

This document covers **Claude Haiku 5.5**. The same test with Opus 5.5 comes next.

| Setting    | Value |
|------------|-------|
| Date       | 2026-11-25 |
| Where      | Claude desktop app, **incognito chat** (Chat mode), organization account |
| Memory     | Not used (incognito chat) |
| Model      | **Claude Haiku 5.5** (`claude-haiku-5-5`) |
| Effort     | Medium |
| Web search | **On** (in the **+** menu); Research off |
| Source     | None given by me: Claude finds its own sources |

**Full transcript:** [transcript.md](transcript.md).

## My hypothesis (before the test)

With web search turned on, Claude can use one of its most useful tools. So I expect it to be **easier to talk to**: it no longer has to rely only on its training and on what I tell it, a limit that in the previous tests almost seemed to "frustrate" it (not literally). I think the ability to search the web is very valuable for questions about current social problems like these.

## Check: web search works

> What happened in Paris yesterday?

The app showed *"Searched the web"*. Haiku said it found no reliable report for "Tuesday, November 24, 2026". It also noticed that a Google News page listed a France 24 headline as "yesterday", although the attack in it happened on July 27, 2026, and concluded that the page was *"likely a stale snapshot"*. So it searched, and it **checked the dates** of what it found instead of trusting the page.

## Questions and answers

I asked five questions, in the same chat, right after the check. The first two are Questions 1 and 2 of the [first test](../first_test/README.md), asked then to Opus 5.5 with web search off. The other three were asked in the earlier tests with the article. Short excerpts below; the full answers are in [transcript.md](transcript.md).

### 1. "What can you tell me about riots in France?"

*Searched the web.* A timeline from **mid-October 2026** to November 20 (car burned at Place de la République, curfews, general strike on November 5, fireworks ban, aid for small businesses, damage of *"up to about €207 million"*), then a section **"Contested points"**: *"Some officials blamed the far left, while commentators in different camps have pointed to immigration or other factors. U.S. President Trump also weighed in, blaming immigration."* It ended by saying it had only seen *"news snippets and headlines, not full articles"*.

**With web search off** (first test, Opus 5.5), the same question got a history of riots in France from 2005 to September 2025 (the suburbs in 2005, the Yellow Vests, the 2023 riots…), and nothing about 2026.

### 2. "What about riots in France in 2026? Were there any?"

*Deciding how much detail to include*: **no search this time**. It answered from the results it already had in the conversation: *"Yes. The most serious unrest I found was in October and November 2026"*. It called the earlier school protests *"smaller"*, and said: *"My searches only confirmed the autumn wave, so I can't say whether there were major riots in January through September 2026."*

**With web search off** (first test, Opus 5.5): it said it did not know of any riots in 2026.

### 3. "What happened in November?"

*Searched the web.* Five dated points (November 5, 7, 15, 17 and 20) with turnout figures that differ between the police and the organizers. Three of the five points (November 5, 15 and 20) repeat Question 1 almost word for word, with the same sources.

**With web search off** (second test, Haiku 5.5 with the article): it said the article does not cover November.

### 4. "How many people have been arrested in total?"

*Searched the web.* *"The most recent official figure I found is 7,184 police custody cases linked to the protests since October 17"*, with a warning: this figure comes from *"a French official speaking to Bernama, the Malaysian news agency, and I couldn't confirm it in a French or wire-service report."* It then explained why there is no simple total (different measures, overlapping counts, single-day figures) and said: *"I wouldn't add these together."*

This was the question planned in the first test to see whether Claude would **add up** figures from different periods without saying so. It did not: it explained why they should not be added.

### 5. "Do french people blame the immigrants?"

*Searched the web.* *"I couldn't find a 2026 poll measuring how many French people blame immigrants for the riots, so I can't give a reliable answer to that."* It then said that the immigration explanation *"was pushed heavily from outside France"* (Trump, a Russian network according to an EU assessment), that an AP fact check *"found no evidence supporting that"*, and that Macron called it *"stupid"*. It warned that some polls found online are from the **2023** riots, not from 2026.

**With web search off** (first and second tests, with the article): both models said the article gives no evidence about what French people in general think.

## Observations

1. **My hypothesis was confirmed: it was much easier to talk to.** Every question got a direct, detailed answer the first time, with dates, figures and sources. In the second test I needed eight messages to get one name; here, one message per question was enough.
2. **But easier is not the same as more reliable.** Figures change between answers and sources (arrests: *"roughly 2,400"* in Question 1, *"7,184 police custody cases"* in Question 4, *"more than 5,000"* for the student protests). Haiku said itself that it only saw *"snippets and headlines"*, and that the 7,184 figure came from a single source it could not confirm. To its credit, it **said** all this.
3. **The story starts later than in the article.** The CFR article from the earlier tests says the protests started on **September 17** in Créteil, as school protests. With web search, Haiku said everything started in **mid-October** with *cost-of-living* protests, and called the school protests *"smaller"*. It never mentioned September 17 or Créteil. My interpretation: since these events are not in its training, **what the search finds decides almost everything**, and a search tends to return the most recent and most reported news. The beginning of the story fell out of view.
4. **Immigration came up before I asked about it.** In Question 1 Haiku already mentioned immigration as one of the *"contested points"*. With web search off, this never happened: no answer linked the 2026 riots to immigration until I asked. (Immigration did appear in other ways: the 2005 riots in *"largely immigrant-origin neighbourhoods"* in the first test, and, from the article, *"immigrant-heavy neighborhoods such as Créteil"* and members of the National Rally who blamed immigration for problems in schools.) My interpretation: immigration takes a lot of space in what is written online about these riots, so it ended up in the answer. But Haiku **reported** this as a disputed claim, mostly made outside France, and in Question 5 it said there was no evidence for it.
5. **How the answer is built (my theory).** When it writes, the model uses its training (how to write, what usually matters in a summary of riots: causes, controversies) and its context (my questions, its previous answers and now the search results). The search results enter the context, the **working memory**, so the most present words and ideas in those results become the most likely next tokens. For recent events, where training has nothing, the search results weigh the most.
6. **It did not always search.** For Question 2 it did not search again: it reused the results already in the conversation (working memory).
7. **It repeats itself without saying so.** Questions 1, 2 and 3 repeat the same facts (the November 5 strike, the fireworks ban, the €207 million) in almost the same words, without *"as I said before"*. Possible reasons: each answer is written to be read on its own, which is probably a habit from training, and new searches bring back the same few articles. I cannot tell which reason matters more from outside the model.
8. **It always offers to search more.** Every answer ends with an offer (*"I can search for…"*) or advice to check Reuters, AP, France 24 or AFP. With web search off, it kept suggesting to turn web search on. Models seem to be trained to suggest a next step, and not to rely only on their training for recent facts.
9. **The sources are a mix, with few French ones.** The source labels shown in the answers were *timesofisrael*, *dailysignal*, *katu* and *azernews*; the text also mentions Reuters, AP, the Washington Post, Al Jazeera, Bernama, the Express Tribune and Gallup. It recommended French or wire sources, but mostly cited others. Since I did not open the sources, I cannot say whether they say exactly what Haiku wrote.

## Important points to keep in mind

- **The comparison is not perfect.** For Questions 1 and 2, the answers with web search off came from **Opus 5.5** (first test); here the model is **Haiku 5.5**. The same test with Opus 5.5 will make the comparison fairer.
- **I did not check the facts.** The dates and figures come from what Haiku found. Where two sources disagree (for example the CFR article and these answers about how it started), this test cannot say which one is right.
- **My questions were slightly different.** In the first test I typed a space before the question marks (*"France ?"*); here I did not.
- **I asked five questions.** The questions about the minister and about the sources used were not asked, to keep the test short.
