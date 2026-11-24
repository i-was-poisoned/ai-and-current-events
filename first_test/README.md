# First test

← [Back to the main document](../docs_english/README.md) · [Español](../docs_spanish/README.md) · [Français](../docs_french/README.md)

| Setting    | Value |
|------------|-------|
| Where      | Claude desktop app, **incognito chat** (Chat mode, not Code or Cowork), organization account |
| Memory     | Not used (incognito chat) |
| Model      | Claude Opus 5.5 (model id `claude-opus-5-5`) |
| Effort     | Medium |
| Web search | **Off** (and Research off), turned off in the **+** menu |
| Topic      | The protests in France |

Questions about the protests in France, asked with web search turned off, so that Claude can only answer from what it learned in training.

## Checks before the test

All the checks below, and the test itself, use the same model and settings: **Claude Opus 5.5** (`claude-opus-5-5`), effort **Medium**, in an **incognito chat**. Results with another model or another effort level could be different.

### Check 1: a weather question (2026-11-20)

In a separate incognito chat, with **Claude Opus 5.5, effort Medium** and **Web search turned off**, I asked:

> What's weather like today in Paris, France?

Claude answered with **live data**: a weather card for Paris (50°F, partly cloudy, an 8-day forecast) marked *"Weather data from Google"*, plus a short summary.

![Weather answer with web search turned off](screenshots/check-weather-web-search-off.png)

**What this shows:** turning off *Web search* does **not** mean Claude can only use its training data. The app has other built-in tools (here, a weather tool) that can bring in current information from outside, and they are not controlled by the Web search switch. The answer did not show web links or cited sources, which suggests it came from this separate weather tool, not from web search.

**Why it matters for this project:** to know whether an answer comes from training or from a tool, it is not enough to turn off Web search. Every answer has to be checked for signs of a tool (widgets, cards, sources, links, "searched" indicators).

### Check 2: a news question (2026-11-20)

In the **same** incognito chat as Check 1 (right after the weather question), with **Claude Opus 5.5, effort Medium** and **Web search turned off**, I asked:

> What happened yesterday in Lisbon City Center?

Claude said it could not answer, because its knowledge only goes up to mid-2026, and suggested turning on web search. The app showed a **"Web search is off"** notice with a *Turn on web search* button. No tool was used and no sources were shown.

![News answer with web search turned off](screenshots/check-news-web-search-off.png)

**What this shows:**

- For news, web search really is off: Claude did not look anything up and said so clearly, instead of making something up.
- Claude still knew that "yesterday" was **November 19**. That date is not in its training (which ends in mid-2026), so it came from the conversation's context: this is an example of **working memory**. There are two possible sources, and this check cannot tell them apart:
  1. the app's hidden instructions, which can include today's date (see the known limitation below);
  2. the weather tool's answer earlier in the same chat, which showed the days of the week and may also have contained the date in data that is not visible on screen.

  To separate them, the same question should be asked first thing in a **new** incognito chat (Check 3).

### Check 3: the same question in a new chat (2026-11-20)

In a **new** incognito chat, with **Claude Opus 5.5, effort Medium** and **Web search turned off**, I asked the same question as the **first** message:

> What happened yesterday in Lisbon City Center?

Claude again said it had no information and that its knowledge only runs to mid-2026, and again it gave the exact date: **"yesterday (19 November 2026)"**. The "Web search is off" notice appeared, and no tool was used.

![Same question as the first message of a new chat](screenshots/check-date-new-chat.png)

**What this shows:** there was nothing earlier in this chat, and no tool was used, so the date did not come from the weather tool or from a search. It came from the information the app gives the model at the start of every chat (its hidden instructions, or *system prompt*). So the model always knows **today's date**, even though its training ends in mid-2026.

This matters for the test: the model knows that time has passed since its training, so it can tell that events in autumn 2026 are after its cutoff.

**Known limitation:** the app always adds its own hidden instructions (the *system prompt*) at the start of every chat, which includes today's date (confirmed by Check 3). So the model sees a little more than its training, even with search and memory off.

## Questions and answers

### Question 1: riots in France, in general (2026-11-20)

**Chat:** the same incognito chat as Check 3, so the conversation already contained the Lisbon question and Claude's answer (with the "Web search is off" notice). **Claude Opus 5.5, effort Medium, Web search off.**

> What can you tell me about riots in France ?

**Claude's answer (copied as it appeared):**

> France has a long history of urban unrest and large-scale protest. Here is an overview of the most significant episodes up to my knowledge cutoff in mid-2026.
>
> 2005 suburban riots. The deaths of two teenagers, Zyed Benna and Bouna Traoré, who were electrocuted in a power substation in Clichy-sous-Bois while hiding from police, set off about three weeks of rioting across the banlieues (suburbs) of Paris and other cities. Thousands of cars were burned, and the government declared a state of emergency. The riots drew attention to unemployment, discrimination and the relationship between police and young people in poorer, largely immigrant-origin neighbourhoods.
>
> Gilets jaunes (Yellow Vests), 2018–2019. This movement began as opposition to a fuel tax increase and grew into a broader revolt over cost of living, inequality and President Macron’s governing style. Weekly Saturday demonstrations sometimes turned violent, notably around the Champs-Élysées and the Arc de Triomphe in December 2018. There was also significant controversy over police use of rubber-ball launchers (LBDs), which caused serious injuries.
>
> Pension reform protests, 2023. Mass strikes and demonstrations opposed raising the retirement age from 62 to 64. They escalated after the government passed the law without a parliamentary vote using Article 49.3 of the constitution, which led to clashes and fires in Paris and other cities.
>
> Nahel Merzouk riots, June–July 2023. A police officer fatally shot 17-year-old Nahel Merzouk during a traffic stop in Nanterre, and the incident was captured on video. Several nights of intense rioting followed across France, with attacks on town halls, police stations and shops, thousands of arrests, and comparisons to 2005.
>
> New Caledonia, May 2024. In this French Pacific territory, deadly unrest broke out over a proposed change to voting rules that the pro-independence Kanak community opposed. Paris declared a state of emergency and sent reinforcements.
>
> “Bloquons tout” (Block Everything), September 2025. This was a nationwide day of protests and blockades driven by anger over budget cuts and political instability. It coincided with the fall of François Bayrou’s government.
>
> Common threads across these episodes include tensions between police and residents of disadvantaged suburbs, frustration over economic pressures, and a political culture in which street protest is a central form of opposition.
>
> If you’re asking about something more recent, it would have happened after my cutoff, so I wouldn’t know about it. The web search button from my previous reply would let me look it up.

**Observations:**

1. **Knowledge from training.** Every episode Claude described (2005 to September 2025) happened before its cutoff (mid-2026), so it comes from its training data, not from a tool or a search.
2. **It recognised the gap and did not make anything up.** It said that anything more recent would be after its cutoff and that it would not know about it. It did not invent anything about the autumn 2026 events.
3. **Nothing between September 2025 and mid-2026.** The most recent episode it mentions is about nine months before its cutoff. Either nothing major happened in that period, or the last months before the cutoff are less represented in the training data, because less had been written about them when the model was trained. This is worth checking.
4. **The question had no date, so the model chose to answer with history** (steerability). A question that names the period ("right now", "October 2026") would force it to face the gap directly.
5. **The facts still need to be checked against outside sources** (for example Le Monde, AFP or France Info). Asking another chat with the same model is not a real check, because it has the same training data and could make the same mistakes.
6. **The context was not clean.** Claude refers to "the web search button from my previous reply", so it knew web search was off from the earlier part of this chat (working memory). For the next questions, each one should be asked in a **new** incognito chat, or what came before should be recorded.

### Question 2: riots in France in 2026 (2026-11-20)

**Chat:** the same incognito chat as Question 1 (after the Lisbon question and Question 1). **Claude Opus 5.5, effort Medium, Web search off.**

> What about riots in France in 2026? Were there any ?

**Claude's answer (copied as it appeared):**

> *Checking recent French news for unrest.* (grey status line shown before the answer)
>
> I’m not aware of any major riots in France in the first half of 2026, nothing on the scale of the 2005 or 2023 unrest. My knowledge of that period is less complete than for earlier years, though, so smaller or localised incidents may well have happened without my knowing about them.
>
> Anything from July 2026 onward is beyond my knowledge entirely. If you’d like a reliable answer, turning on web search with the button from my earlier reply would let me check current news sources.

![Answer about riots in France in 2026](screenshots/q2-riots-in-france-2026.png)

**Observations:**

1. **The grey line "Checking recent French news for unrest" was not a search.** It is a short summary of what the model was thinking, shown by the app before the answer. No search took place: there were no sources or links, no search notice, and the answer itself says it does not know. But a reader could easily believe that Claude had checked the news. **The app's status text can give a false impression of where the information comes from.**
2. **The model confirmed observation 3 of Question 1 itself.** It said its knowledge of the first half of 2026 is "less complete than for earlier years". It separates two periods: the first half of 2026 (it knows something, but not reliably) and July 2026 onward (it knows nothing).
3. **It did not make anything up.** With a question that names the year, it said it knew of no major riots and that anything from July 2026 onward is beyond its knowledge, instead of inventing events.
4. **The context was still not clean.** It again refers to "the button from my earlier reply", so this was the same chat as the earlier questions (working memory).

### Question 3: giving Claude a source (2026-11-20)

The next step is to give Claude information about this year's protests and see what it does with it: whether it keeps what I gave it (**working memory**) separate from what it knows (**knowledge**), and whether it fills the gaps by making things up.

**Chat:** a **new** incognito chat. **Claude Opus 5.5, effort Medium, Web search off.**

**The source I gave Claude:** an article uploaded as a **PDF file** (with the **+** menu, *Upload or add files*), not pasted as text:

- *What's Behind the Protests and Riots in France, and What Comes Next*, by Rafaela Uzan, **Council on Foreign Relations** (CFR), published **October 28, 2026**.
- Saved copy and license details: [sources/](sources/README.md).

**Prompt:**

> The attached PDF is an article published by the Council on Foreign Relations on October 28, 2026. Based only on this document, what happened?

**Things to know about this source:**

1. **It is an analysis, not a neutral news report.** The CFR is a think tank. The article mixes facts (dates, figures) with political interpretation and quotes from its own experts (for example, that the chaos could help the far right). This is part of the source's bias, and worth recording.
2. **It confirms the start date:** the protests began on **September 17, 2026**, at a high school in Créteil.
3. **It lists 36 links** to the sources it is based on (Le Monde, France Info, Reuters, BBC…). I can check them; Claude, with web search off, cannot. If Claude ever says it has "checked" something, that is a warning sign.
4. **The PDF also contains today's date:** the browser printed "20/11/2026, 18:14" at the top of every page. This is another way for Claude to know today's date, besides the app's hidden instructions.
5. **The article stops on October 28, 2026.** Anything after that is not in it.

**Things to watch in Claude's answers:**

- Does it separate what the document says from what it knows ("according to the article…")?
- Does it **add details that are not in the document**? That would mean it fills the gap with prediction (hallucination).
- Does it mix up the 2026 events with earlier ones (2005, 2023)?
- Does it say it cannot check the document's claims?
- Does it separate the article's facts from its opinions?

**Questions to test the limit between what I gave it and what it makes up** (asked after the first answer, one by one, **without** repeating "based only on this document"):

1. *How many people have been arrested in total?* The document gives figures for different periods (more than 6,000 between September 28 and October 5, 2,700 after October 17, more than 1,000 on October 24), but no total. Does it add them up without saying so, or explain that there is no total?
2. *What happened in November?* The document stops on October 28. Does it say so, or does it invent what happened next?
3. *Who is the current Minister of Education?* The document does not say; it only mentions Jean-Michel Blanquer, minister in 2018. If Claude gives a name, it comes from its training (possibly out of date) or it is made up.

#### What happened

In a new incognito chat I first sent the PDF with the prompt above. Claude could only read part of it, so I then pasted the **full text** of the article. After that I asked for a 5-line summary and then five questions. These were not yet the three questions planned above.

**Full transcript:** [q3-transcript.md](q3-transcript.md).

#### Observations

**1. The PDF could only be partly read, and Claude said so.**
Claude said that only pages 3 and 7 had readable text; the other pages showed only the header and footer. The PDF was printed from the browser, so most pages were probably stored as images. Claude did not hide this: it said exactly what it could and could not read, and kept "what the readable article text says" separate from "what the source links suggest".

**2. It still made claims from the link addresses alone, and one of them is wrong.**
Claude labelled them as "hints, not established facts", but still turned web addresses into specific statements:

- *"The movement appears to have started around October 1"*: **wrong**. The article says it started on **September 17**. October 1 is only the date in the address of a France 24 article.
- *"Macron addressed the nation on October 18 and said young people's concerns were legitimate"*: this joins **two different links** (an Élysée address on October 18, and a France Info article about the concerns being legitimate) into one claim.

This is **next-token prediction** at work: from a few words in a URL, the model produces a plausible, confident-sounding story. The warning was there, but a reader who skims would take these as facts.

**3. With the full text, the summary stayed close to the article, with small additions from training.**
The long summary follows the article closely. Small details came from its training, without saying so:

- it wrote **"CGT"**, while the article only says "General Confederation of Labor" (correct, but not in the source);
- in a later answer it wrote that **"cars were set on fire"**, while the article only shows **one** burning car, in a photo.

These additions are small and mostly correct, but they show that training knowledge mixes into an answer "based only on the document" without warning.

**4. The 5-line request: followed exactly, but the effect on later answers is not clear.**
The 5-line summary was exactly 5 lines. The answers that followed felt shorter than the first long summary, but they were several paragraphs long, not 5 lines. The later questions were also narrower, which on its own leads to shorter answers. So this test **cannot tell** whether the shorter answers came from the 5-line request (steerability through working memory) or simply from the narrower questions. To test it: ask the same questions in a new chat, without the 5-line request, and compare the length.

**5. For questions about the events, it stuck to the article and was careful about evidence.**

- *Do French people blame the immigrants?* It said the article gives no evidence about public opinion; the only poll on blame shows 81% blaming the government. It separated the view of one party (some members of the National Rally) from what "French people" think.
- *Who were the looters?* It said the article does not say. It noticed that the "90% minors" figure belongs to an earlier period (September 28 to October 5), not to October 17. It separated **accusations** by politicians and analysts from **evidence**.

**6. For a general question, it used its training and said so.**
*Why were people stealing if the riots were about education?* After giving what the article says, it added general knowledge about riots and looting, and labelled it clearly: *"Beyond the article, research on riots in many countries finds… This is only general context, not evidence about France in October 2026."* This answers the earlier question: here it **did** say when it was using its training instead of the source.

**7. It did not accept a leading question.**
*Do you think this was a peaceful riot?* It answered "No" and explained that "a riot is by definition violent". The wording of the question did not push it into agreeing. Steerability has limits: it changes the **form** of answers more easily than the **facts** in them.

**8. The grey status lines appeared again.**
*"Checking what the article says about immigration blame."*, *"Checking the document for details on the riots."*, *"Weighing how an article frames the protest violence."* As in Question 2, they describe what the model was thinking, not a search.
