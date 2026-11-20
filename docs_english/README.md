# The project (English)

This is a research project about how an AI model behaves when it is asked about events that happened **after** its training: the protests and riots in France in autumn 2026.

It is also a way of learning: I am using AI to understand AI better.

## What I want to understand

- **Next-token prediction**: the model writes its answer one small piece (a *token*) at a time, each time choosing a likely continuation based on patterns learned during training. What happens when the topic is something it never saw?
- **Knowledge**: what the model learned during training, which stops at a *knowledge cutoff*. Claude Opus 5.5's cutoff is June 2026, so these events are not in its training.
- **Working memory**: what the model can see in the current conversation (my questions, its own previous answers, and any search results or files). This is the *context window*, and it is separate from what it learned in training.
- **Steerability**: how much the way I ask (the wording, the instructions, the framing) changes the answer.

## The first test

In the Claude desktop app, in an **incognito chat** (Chat mode, no memory of other conversations), with the model **Claude Opus 5.5** (model id `claude-opus-5-5`), effort **Medium**, and **web search turned off**, I will ask questions about the protests in France. Without search, Claude can only answer from what it learned in training.

The questions, the answers and what I observe will be recorded in the [first_test](../first_test/) folder.

## First finding: "web search off" does not mean "training data only"

Before the test, I checked the setup by asking about today's weather in Paris, with web search turned off. Claude still answered with live weather data ("Weather data from Google"), using a built-in weather tool that the Web search switch does not control.

So turning off web search does not stop Claude from using other tools that bring in information that is not in its training data. Every answer has to be checked for signs of a tool (widgets, cards, sources, links). Details and screenshot in [first_test](../first_test/README.md#checks-before-the-test).
