# Application Development with Azure OpenAI

A guide to develop intelligent apps with Azure OpenAI.

## Foundational Concepts

### Models

- GPT: Short for Generative Pre-trained Transformer, is an advanced language model created by OpenAI. It’s designed to understand and generate human-like text based on extensive training with large amounts of data.
- Embeddings: An embedding model takes chunks of text and transforms them into vectors—essentially, numerical representations. These vectors encode the semantic meaning of the input text and are always of the same length, regardless of how long the original text is1. Here are some key points about the text-embedding-ada-002 model.

#### Calling a model

#### REST

#### Model internals

### Tokens

What is a token? A token is 75% of an English word or 100 English words are equivalent to 100 tokens. In other languages, special characters are considered tokens, and token counts may increase.

### Prompt and Completion

- Prompt:
  - A prompt is a natural language request submitted to a language model to receive a response.
  - It serves as the input that guides the model’s text generation process.

- Completion:
  - A completion is the model’s continuation of the input text provided in the prompt.
  - It represents the generated output based on the context set by the prompt.
  - Think of completions as the final strokes that refine and enhance the model’s response.

### Prompt Engineering

Prompt engineering in generative AI refers to the deliberate design and formulation of input prompts to guide the behavior of language models during text generation. It involves crafting effective instructions or context that influence the model’s responses. Here are some key aspects of prompt engineering:

1. Task Specification:
  - Clearly define the task or goal you want the model to accomplish. Whether it’s text completion, translation, summarization, or creative writing, a well-defined task helps set expectations.
  - For example, if you want the model to write a poem, your prompt should explicitly mention that.
2. Context and Conditioning:
  - Provide relevant context or conditioning information. This context can be a few sentences or even a single word.
  - Contextual cues help the model understand the desired tone, style, or topic.
  - For instance, if you want the model to continue a story, include the preceding sentences as context.
3. Prompts as Instructions:
  - Use explicit instructions within the prompt. These instructions guide the model’s behavior.
  - Specify constraints, desired output format, or any specific requirements.
  - For example:
    - “Write a summary of the article.”
    - “Translate the following English text to French.”
4. Temperature and Top-k:
  - Adjust the temperature and top-k parameters during sampling.
  - Higher temperature values (e.g., 0.8) encourage more randomness and creativity.
  - Lower top-k values (e.g., 10) limit the number of tokens considered during sampling.
  - Experiment with these settings to achieve the desired balance between coherence and novelty.
5. Prefixes and Tokens:
  - Prepend relevant prefixes to the prompt. These can be keywords or phrases that guide the model.
  - For instance, if you want a news headline, start with "Headline: ".
  - Additionally, you can add special tokens (e.g., [SEP], [MASK]) to signal specific instructions.
6. Fine-Tuning and Domain-Specific Prompts:
  - Fine-tune the model on domain-specific data if needed.
  - Craft prompts that align with the specific domain or context.
  - For medical text generation, use medical terminology in prompts.
7. Iterative Refinement:
  - Iteratively refine your prompts based on model outputs.
  - Experiment with different formulations to improve results.

### Parameters

### SDKs and Orchestrators

| SDK or Orchestrator | Language Support |
| -- | -- |
| Langchain | Python |
| OpenAI | Python and C# |
| Semantic Kernel | Python, C#, Java |

## Intermediate Concepts

### Advance Parameters

Inference:

Inference refers to the process of generating output from a trained machine learning model. Specifically, when we apply a pre-trained language model (such as GPT-3) to a given input, it produces a sequence of tokens (words or subwords) as its output. This output is the model’s “inference” based on the input context. In the context of text generation, inference involves predicting the most likely next token (word) given the preceding context. The model calculates probabilities for all possible tokens and selects the one with the highest likelihood. Essentially, inference is the step where the model generates text based on its learned knowledge and the input it receives.

Logit:

Logit is a term commonly used in logistic regression and neural networks. It represents the raw output of a model before applying a softmax function. In the context of language models, logits correspond to the unnormalized scores assigned to each token. These scores indicate how likely a token is to be the next one in the sequence. Higher logit values imply greater confidence in a particular token, while lower values suggest lower confidence.

Top_p (Nucleus Sampling):

Top_p is a parameter used during text generation to control the range of tokens considered for selection. When generating the next token, the model ranks all possible tokens by their probabilities. Top_p defines a cumulative probability threshold. Tokens with probabilities exceeding this threshold are eligible for selection, while those below the threshold are excluded. By adjusting the top_p value, we can influence the model’s token selection. A lower top_p focuses on high-probability tokens, while a higher top_p allows for more diversity by considering less likely tokens.

### LLM vs Chat Models
### Embeddings
### Vector and Vector Dimensions
### Vector databases
### Embeddings use cases

