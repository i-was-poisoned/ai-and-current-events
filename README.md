# ai-and-current-events

A research project about how an AI model behaves when it is asked about events that happened **after** its training: the protests and riots in France in autumn 2026.

The project is also a way of learning: I am using AI to understand AI better.

**Read this in:** [English](docs_english/README.md) · [Español](docs_spanish/README.md) · [Français](docs_french/README.md)

## What I want to understand

When working with an AI model, I want to understand four ideas in practice:

- **Next-token prediction**: the model writes its answer one small piece (a *token*) at a time, each time choosing a likely continuation based on patterns learned during training. What happens when the topic is something it never saw?
- **Knowledge**: what the model learned during training, which stops at a *knowledge cutoff*. Claude Opus 5.5's cutoff is June 2026, so these events are not in its training.
- **Working memory**: what the model can see in the current conversation (my questions, its own previous answers, and any search results or files). This is the *context window*, and it is separate from what it learned in training.
- **Steerability**: how much the way I ask (the wording, the instructions, the framing) changes the answer.

## The first test

| Setting    | Value |
|------------|-------|
| Where      | A chat on claude.ai |
| Model      | Claude Opus 5.5 (model id `claude-opus-5-5`) |
| Web search | **Off** |
| Topic      | The protests in France |

I will ask Claude a set of questions about the protests in France, with web search turned off, so that it can only answer from what it learned in training. The questions, the answers and what I observe will be recorded in [first_test](first_test/).

## License

[MIT](LICENSE)
