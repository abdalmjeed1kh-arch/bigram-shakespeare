# Bigram Language Model from Scratch

Char-level bigram language model built from scratch on tinyshakespeare 
as part of a self-directed LLM research roadmap.

## What it does
Trains a single-layer neural network to predict the next character 
given the current one. Generates Shakespeare-flavored text after training.

## Pipeline
- Char-level tokenizer (encoder/decoder dicts)
- Train/val split
- Random batch sampling with block_size=8
- nn.Embedding-based bigram model
- Cross entropy loss + Adam optimizer
- Multinomial sampling for generation

## Result
Loss drops from ~3.14 → ~2.5 (random baseline = 4.17).
Output is gibberish but with recognizable Shakespeare structure: 
character names with colons, spacing, English-like patterns.

## Next
Replace the bigram with a transformer (attention + FFN + positional encoding).