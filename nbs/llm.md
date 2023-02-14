# Large Language Models

## Theory

### Resources

- [Primer on Transformers](https://aman.ai/primers/ai/transformers/)
- [Study guide on Transformers](https://github.com/dair-ai/Transformers-Recipe)
- [Stanford CS224N - NLP with Deep Learning](https://www.youtube.com/playlist?list=PLoROMvodv4rOSH4v6133s9LFPRHjEmbmJ)
- [Stanford CS25 - Tranformers United](https://www.youtube.com/playlist?list=PLoROMvodv4rNiJRchCzutFw5ItR_Z27CM)
- [Papers with Code - Language Models](https://paperswithcode.com/methods/category/language-models)

## Techniques

### Zero Shot Prompting

This is regular prompting.  Downside being hallucination and confubulation.  The model can only rely on its training data and not react to current events.

### In-Context Learning

In-Context Learning is the remarkable capability for a LLM to construct new predictors from sequences of labeled examples in its prompt without the need for fine-tuning.

- [Paper - What learning algorithm is in-context learning? Investigations with linear models](https://arxiv.org/abs/2211.15661) and a [summary on 42 papers](https://42papers.com/p/what-learning-algorithm-is-in-context-learning-investigations-with-linear-models) talks about how similar In-Context Learning is to a trained model.

### Chain-of-Thought prompting ("CoT")

Introduced in the [Paper - Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/abs/2201.11903)

In your prompt you include explicit reasoning and this gets the model to do the same. This increases accuracy.  It is however not grounded to external environments to obtain and update knowledge, and has to rely on limited internal knowledge.  

The simplest form of this is to add "let's think step by step" to your prompt.  ("Zero shot CoT")

### HyDE: Hypothetical Document Embeddings

Introduced in the [Paper - Precise Zero-Shot Dense Retrieval without Relevance Labels](https://arxiv.org/abs/2212.10496).

The idea here is that instead of encoding the user's query to retrieve relevant documents, you can generate a "hypothetical" (hallucinated) answer and encode that. Documents with right answers are more similar to wrong answers than to questions.

### ReAct: combining chain-of-thought and action-prompting interleaved

See [Paper - ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) and the [associated ReAct website](https://react-lm.github.io/)

### Resources

[Prompt Engineering Guide](https://github.com/dair-ai/Prompt-Engineering-Guide)

## Optimizations

### Use a smaller model

- [Blog post by Alistair Pullen](https://www.buildt.ai/blog/incorrectusage) explains that latency significantly goes up as you use larger models like Da Vinci.  He explains an approacht to reduce price by a factor 40 while reducing latency 4 to 5 times at the trade-off of getting 90% similar results to Da Vinci.  The approach generates a corpus of completions using Da Vinci.  Then use that corpus to train Babbage.

