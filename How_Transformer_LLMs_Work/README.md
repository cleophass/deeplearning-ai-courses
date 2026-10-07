# How Transformer LLMs Work

Notes and code from the [DeepLearning.AI](https://www.deeplearning.ai/) course **How Transformer LLMs Work**, taught by Jay Alammar and Maarten Grootendorst, authors of the book *Hands-On Large Language Models*.

## What the course covers

A deep dive into the transformer architecture behind today's LLMs (introduced in *Attention Is All You Need*, 2017):

- **Language representation**: from Bag-of-Words and Word2Vec to contextual embeddings in transformers.
- **Tokenization**: how text is split into tokens before reaching the model, and how tokenizers differ between LLMs.
- **The three stages of a transformer**: tokenizer + embeddings, the stack of transformer blocks, and the language model head.
- **The transformer block**: self-attention (relevance scores between tokens) followed by the feedforward layer (knowledge stored during training).
- **Efficiency and modern improvements**: KV cache, multi-query attention, grouped-query attention, sparse attention.
- **Hands-on with Hugging Face Transformers**: looking at recent model implementations.

## Contents

| Notebook | Description |
|---|---|
| [`Comparing_Trained_LLM_Tokenizers.ipynb`](./Comparing_Trained_LLM_Tokenizers.ipynb) | Lesson 2. Uses `AutoTokenizer` to compare how BERT, GPT-2, GPT-4, Flan-T5, StarCoder 2, Phi-3 and Qwen2 tokenize the same text (casing, emojis, code, whitespace, numbers) and how vocabulary sizes differ. |
| [`Understand_Model_Architecture.ipynb`](./Understand_Model_Architecture.ipynb) | Lesson 6. Explores the decoder-only model `microsoft/Phi-3-mini-4k-instruct`: text generation with a `pipeline`, inspecting the architecture (embeddings, 32 transformer blocks, LM head), and generating a single token step by step (tokenizer → transformer blocks → LM head → `argmax`). |

More lessons will be added as I go through the course.
