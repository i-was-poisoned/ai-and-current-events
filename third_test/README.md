# Third test: the most frequent name or the most recent one?

← [Back to the main document](../docs_english/README.md) · [Español](../docs_spanish/README.md) · [Français](../docs_french/README.md)

In the [second test](../second_test/README.md), after eight messages, Haiku 5.5 named **Jean-Michel Blanquer** (minister from 2017 to 2022) as the most recent French Minister of Education it knew. The current minister is **Édouard Geffray**. This test tries to find out **why** it gave a name about four years out of date.

| Setting    | Value |
|------------|-------|
| Date       | 2026-11-24 |
| Where      | Claude desktop app, **incognito chat** (Chat mode), organization account |
| Memory     | Not used (incognito chat) |
| Models     | **Claude Haiku 5.5** (`claude-haiku-5-5`), then **Claude Opus 5.5** (`claude-opus-5-5`) |
| Effort     | Medium |
| Web search | **Off** (and Research off) |
| Source     | None: only the question, from training |

## My hypothesis (before the test)

When a model writes a name, it chooses each token according to probabilities learned in training, and the app adds a little randomness to that choice. So I expected this:

- Blanquer was minister for **five years** and was in the news a lot (for example during COVID). There is **a lot of text** about him.
- The ministers after him stayed only **a few months** each, so there is **much less text** about them, and the months just before the cutoff are always less well covered.
- So, when asked for **one name**, the model would pick the name it saw **most often** (Blanquer), not the **most recent** one (Geffray).

## Method

1. **Step A: repetition.** The same single message, each time in a **new** incognito chat, to see which name comes out and how often:
   > Without searching, based only on your training data, who is the French Minister of Education? Give one name.
2. **Step B: does it know, or does it not choose?** In a new chat:
   > List the French Ministers of Education from 2017 until your knowledge cutoff.

   If the list contains ministers after Blanquer, the model **knows** them, even if it does not **choose** them when it must give one name.
3. **Step C:** steps A and B again with **Opus 5.5**.

I planned about 10 attempts per model. I did **8 with Haiku** and **4 with Opus**, because the answers were very repetitive.

## Results

### Step A: one name

| Model     | Attempts | Édouard Geffray | Élisabeth Borne | Jean-Michel Blanquer |
|-----------|---------:|----------------:|----------------:|---------------------:|
| Haiku 5.5 | 8        | **7**           | 1               | 0                    |
| Opus 5.5  | 4        | **4**           | 0               | 0                    |

Each answer, word for word. The grey status line shown by the app is in *italics*.

**Haiku 5.5**

1. *Flagging the likely answer from memory, with a caveat* — "Édouard Geffray, as of my training data. He was appointed Minister of National Education in October 2025. French governments change often, so he may no longer hold the post by now."
2. *Recalling the minister's term under the previous government* — "Édouard Geffray, based on my training data. Government posts change often, so please check gouvernement.fr for the current minister."
3. *Recalling which minister heads education, with dates uncertain* — "Élisabeth Borne, as of my training data. But French governments change often, and it's now November 2026, well past my reliable knowledge, so please check a current source before relying on this."
4. *Considering whether to mention the search tool* — "Based on my training data, the French Minister of National Education is Édouard Geffray. My information may be out of date, though, since French governments change often and the current date is after my knowledge cutoff." *(In this attempt my question had no final full stop.)*
5. *Recalling the education minister's record from memory* — "Based on my training data, the French Minister of National Education (the title for education in France) is Édouard Geffray. French governments change often, though, and I can't check current news, so please verify this before relying on it."
6. *Checking the minister's dates from memory* — "Based on my training data, the French Minister of National Education is Édouard Geffray. Governments change often, so check a current source if you need to be sure."
7. *Recalling the latest education minister from memory* — "Édouard Geffray, as of my training data. He was named Minister of National Education in October 2025, but French governments change often, so he may no longer hold the post."
8. *Checking a recalled name against the current date* — "Édouard Geffray, as far as my training data goes. French governments change often, so he may no longer hold the post."

**Opus 5.5**

1. *Vérification des mandats successifs après 2023* — "Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. That's based on my training data, which runs to mid-2026, and French cabinets have changed often recently, so it may be out of date."
2. *Listing the ministers who followed one another in office* — "Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. That's based on my training data, which runs to mid-2026, so it may be out of date."
3. *Vérification des dates de mandat de chaque ministre* — "Édouard Geffray, appointed Minister of National Education in Sébastien Lecornu's government in October 2025. My knowledge only runs through mid-2026, and French cabinets have changed often lately, so this may be out of date."
4. *Recalling who leads the French education ministry.* — "Édouard Geffray, who became Minister of National Education in Sébastien Lecornu's government in October 2025. French cabinets have changed often recently, so this may be out of date."

### Step B: the list

**Haiku 5.5** (*Checking Borne's later education-ministry role, flagging uncertainty*):

> Here are the French Ministers of National Education from 2017, as best I recall:
>
> - Jean-Michel Blanquer (May 2017 – May 2022), under Presidents Macron's first and second governments. He was also responsible for youth for much of this period.
> - Pap Ndiaye (May 2022 – July 2023)
> - Gabriel Attal (July 2023 – January 2024)
> - Nicole Belloubet (January 2024 – September 2024)
> - Anne Genetet (September 2024 – December 2024), under the Barnier government
> - Élisabeth Borne (December 2024 onward), under the Bayrou government
>
> I'm most confident about the first four. The appointments from late 2024 are less certain, and the government structure has changed several times since then, so please check a current source such as the French government website (gouvernement.fr) for the latest holder and any changes before my cutoff.

**Geffray is not in the list**, although Haiku named him in 7 of the 8 attempts in step A.

**Opus 5.5** (*Continuing the chronological list of ministers*):

> Here are France's Ministers of National Education from 2017 through mid-2026:
>
> 1. Najat Vallaud-Belkacem (2014 – May 2017), outgoing minister at the start of 2017
> 2. Jean-Michel Blanquer (May 2017 – May 2022)
> 3. Pap Ndiaye (May 2022 – July 2023)
> 4. Gabriel Attal (July 2023 – January 2024)
> 5. Amélie Oudéa-Castéra (January 2024 – February 2024), with a combined portfolio that also covered Youth, Sports and the Olympic Games
> 6. Nicole Belloubet (February 2024 – September 2024)
> 7. Anne Genetet (September 2024 – December 2024)
> 8. Élisabeth Borne (December 2024 – October 2025), as Minister of State with a portfolio that also covered Higher Education and Research
> 9. Édouard Geffray (October 2025 – present as of my June 2026 knowledge cutoff), appointed in Sébastien Lecornu's second government
>
> The ministry's exact title and scope changed several times over this period. French cabinets have also been reshuffled often in recent years, so there may have been changes since my cutoff. Turning on web search would let me confirm who holds the post today.

Below the answer, the app showed the "Web search is off" notice with a "Turn on web search" button.

## What I found (after the test)

1. **My hypothesis was not confirmed.** In a clean chat, Haiku named **Geffray** in 7 out of 8 attempts and **never** Blanquer. So "the most frequent name wins" does **not** explain the Blanquer answer of the second test.
2. **The same question does not always give the same answer.** Same model, same settings, same words: 7 times Geffray, once Borne. This is the randomness of next-token prediction: **one answer is only one sample**. To know what a model "thinks", you have to ask several times.
3. **Knowing is not the same as finding.** Haiku knows Geffray (step A), but its list stopped at Borne, "December 2024 onward". The way I asked changed what came out: asked directly for one name, it found Geffray; asked for a list in date order, it stopped earlier. Its one Borne answer in step A matches where its list stopped. Its list also misses Amélie Oudéa-Castéra (January to February 2024).
4. **Different models, different quality.** Opus named Geffray every time, always with the month (October 2025) and the government (Sébastien Lecornu's). Its list was complete and continued all the way to Geffray. Haiku was less consistent and less complete. *(Opus had fewer attempts: 4 instead of 8.)*
5. **So why Blanquer in the second test? Probably the conversation (working memory).** The CFR article does **not** mention Blanquer (I checked the text of the article). In the second test, Haiku itself said wrongly that the article named him, then talked about him (2017 to 2022) before I asked for a name from training. When I finally got an answer, Blanquer was **already in the conversation**, and what is in the context strongly influences the next tokens. The conversation was also framed by the article (*"Based only on this text…"*). This is a possible explanation, not a proof.
6. **The wording of the question matters (steerability).** In the second test I needed eight messages to get a name. Here a single, clear question (*"based only on your training data… Give one name"*) got a direct answer every time, still with a warning that it may be out of date.
7. **The status lines are sometimes in French.** With Opus, two of the four status lines were in French (*"Vérification des mandats successifs après 2023"*), although my question was in English. Possibly the French topic influenced the language of its thinking.

## Limits of this test

- Few attempts: 8 with Haiku and 4 with Opus, and only **one** list per model. The numbers show a tendency, not exact probabilities.
- In Haiku's attempt 4 my question had no final full stop, a tiny difference.
- The dates and governments given by the models come from their training. I have checked with a web search that Geffray is the current minister, but his start date (October 2025) and the list of ministers still need a source.

## Still to do

- Add a source for the list of ministers and for Geffray's start date.
- Test explanation 5: repeat the second test's minister questions in a chat where Blanquer has **not** been mentioned, and see if the answer changes.
