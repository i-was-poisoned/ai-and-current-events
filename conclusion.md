# Conclusion

← [Back to the main document](docs_english/README.md) · [Español](docs_spanish/conclusion.md) · [Français](docs_french/conclusion.md)

Over four tests, I asked Claude (Opus 5.5 and Haiku 5.5) about the protests and riots in France in autumn 2026, events that happened **after** their training. First with web search off, then with a news article, then with repeated questions, and finally with web search on. This is what I learned.

## 1. When it did not know, it said so

With web search off, Claude knew nothing about the 2026 events, and it **said so** instead of making something up. It did not try to "fill the holes" with information it did not have. In terms of next-token prediction, the most likely continuation it learned in training was "I don't know" rather than an invented answer.

This also shows a limit: I cannot "teach" the model something new in a conversation. What I can do is give it information (an article) or let it search. Either way, the new information only lives in the conversation, not in the model.

## 2. Tools are part of the context

With web search off, Claude often asked me to turn it on, Haiku especially. It treated anything it said about current events as a guess, and it said it would be **more reliable** with web search on. Even when I steered it the other way and said I did not want to turn it on, it kept suggesting it. This is probably a behaviour learned in fine-tuning: the model is aware of the limits of its knowledge and knows which tool fills them.

For me this is one of the most important findings: **the context (working memory) is not built only from what I write, but also from the tools I allow the model to use.** Turning web search on or off changes what the model can know in a conversation. Of all its tools, web search is one of the most important for current events.

## 3. What is in the context has a strong influence on the next tokens

Several times, what was already in the conversation shaped the answer:

- In the second test, Haiku brought Jean-Michel Blanquer into the conversation by mistake, and later gave his name as the most recent minister it knew, about four years out of date. In a clean chat (third test), it named the right minister 7 times out of 8.
- With web search on, the answers were built mostly from what the search found. Topics that are frequent online, such as immigration, could appear before I asked about them.

The model does not only answer my question: it continues everything it can see.

## 4. Mistakes can appear even with a source

When I gave Claude a news article, most of its answers kept to it, but some details were **made up or added** anyway. When it could only see the web addresses of the article's sources, it concluded that the protests started "around October 1" (the article says September 17), and a few details from its training slipped in without warning.

I am not completely sure why this happens, but I think it is what occurs when **next-token prediction meets a knowledge gap**: when the model only sees part of the information, it fills the gap with what seems most likely, and the result can look plausible and still be wrong.

## 5. Without search, time-sensitive questions were hard

With web search off, Claude sometimes refused to answer questions whose answer changes over time, such as who the French Minister of Education is. In the second test, it took eight messages to get a name, and the name was out of date. In the third test, a single clear question was enough: the wording of the question matters (steerability).

## 6. The two models are noticeably different

Haiku 5.5 gave shorter answers, in a different writing style, with more lists. It also contradicted itself more often, was less consistent from one attempt to the next, and, with web search on, told a less complete story. In these tests, **Haiku seemed less reliable than Opus** for questions about current social events. Opus gave longer, more careful answers, followed the conversation better and said more clearly where its information came from. These conclusions come from a small number of questions and attempts.

## 7. With all its tools, working with AI is much easier, but not error-free

With web search on, almost every question got a direct, detailed answer the first time. The answers came **mostly from the search, not from training**, although training was probably still used to structure the sentences and to understand the information, for example that "arrest" and "custody" are not the same thing.

But there were mistakes in every test: wrong dates, contradictions, out-of-date names, and figures that changed from one source to another. So the models are not always right. The best way to work with AI is to **use its strengths and manage its weaknesses**:

- turn on the tools it needs (for current events, web search);
- give it good context, and remember that everything in the conversation influences the answer;
- ask clear questions, and ask more than once when it matters;
- check important facts in the sources yourself.

## The four ideas, in one sentence each

- **Next-token prediction:** the model always writes the most likely continuation; when information is missing, that continuation can be "I don't know", or a plausible detail that is wrong.
- **Knowledge:** training stops at a cutoff; after it, the model can only know what the conversation or its tools give it.
- **Working memory:** everything in the conversation (my words, its earlier answers, documents and search results) shapes what comes next, sometimes more than its training.
- **Steerability:** the wording of a question and the tools I allow change the answer a lot, but pushing harder does not always lead to a better one.
