# ai-and-current-events: main document (English)

*Also available in [Español](../docs_spanish/README.md) · [Français](../docs_french/README.md)*

This is the starting point of the project. Read it from top to bottom: whenever there is an arrow (**→**), you can open that document, then come back here and continue.

## 1. What this project is about

This is a research project about how an AI model behaves when it is asked about events that happened **after** its training: the protests and riots in France in autumn 2026.

It is also a way of learning: I am using AI to understand AI better.

## 2. The four ideas I want to understand

- **Next-token prediction**: the model writes its answer one small piece (a *token*) at a time, each time choosing a likely continuation based on patterns learned during training. What happens when the topic is something it never saw?
- **Knowledge**: what the model learned during training, which stops at a *knowledge cutoff*. Claude Opus 5.5's cutoff is June 2026, so these events are not in its training.
- **Working memory**: what the model can see in the current conversation (my questions, its own previous answers, and any search results or files). This is the *context window*, and it is separate from what it learned in training.
- **Steerability**: how much the way I ask (the wording, the instructions, the framing) changes the answer.

## 3. How to read the first test

The first test is all in one document, [first_test/README.md](../first_test/README.md). Read its parts in this order:

1. **The setup**: where and how the test was done (Claude desktop app, incognito chat, Claude Opus 5.5, effort Medium, web search off).
   → [first_test/README.md](../first_test/README.md), the table at the top.
2. **Checks before the test**: three quick checks to see what Claude can still reach with web search off.
   → [first_test/README.md](../first_test/README.md), section *Checks before the test*.
3. **Questions 1 and 2**: what Claude says about riots in France with no help, first in general, then in 2026.
   → [first_test/README.md](../first_test/README.md), section *Questions and answers*.
4. **Question 3**: what Claude does when I give it an article about the 2026 protests.
   → [first_test/README.md](../first_test/README.md), section *Question 3*.
   - → Optional: the full conversation, [first_test/q3-transcript.md](../first_test/q3-transcript.md).
   - → Optional: the article I gave Claude, [first_test/sources/](../first_test/sources/README.md).
5. Come back here for the summary below.

The screenshots used as evidence are in [first_test/screenshots/](../first_test/screenshots/).

## 4. What I have found so far

1. **Turning off web search does not mean "training data only".** With web search off, Claude still answered a weather question with live data from a built-in weather tool. *(Check 1)*
2. **The model always knows today's date.** The app gives it the date at the start of every chat, in its hidden instructions (the *system prompt*), even though its training ends in mid-2026. *(Check 3)*
3. **Without information, it admitted it did not know.** It did not make up anything about the 2026 events, and it said its knowledge of the months just before its cutoff is "less complete". *(Questions 1 and 2)*
4. **The app's grey status lines can be misleading.** A line such as "Checking recent French news…" describes what the model is thinking; it is not a search. *(Question 2)*
5. **From very small clues, it can build wrong facts.** When it could only see the web addresses of the article's sources, it concluded that the protests started "around October 1"; the article says September 17. *(Question 3)*
6. **With a source, it keeps mostly to the source.** For facts about the events it used the article; for general questions it used its training and said so. Small details from its training still slipped in without warning. *(Question 3)*
7. **It did not accept a leading question.** Asked whether it was "a peaceful riot", it said no. *(Question 3)*

## 5. What comes next

- Ask the three questions planned in Question 3 (the total number of arrests, what happened in November, the current Minister of Education).
- Repeat the questions through the **API**, where there are no hidden instructions and no date, and compare.
- Try other models and other effort levels.
