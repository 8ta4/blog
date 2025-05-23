They say puns are the lowest form of humor. When I say I'm building a tool to generate puns, they make pun of me!

My goal is straightforward: create word-swapping puns that are easy to understand and relevant to the input. u/thepartners's [idealy](https://idealy.app) is the closest thing to what I'm aiming for, but it's not for me.

Let me walk through a quick example. Say I wanted to create puns for this Reddit post:

1. [Relevant Word Identification](https://github.com/8ta4/pun/blob/a745263dc93952a0f6f8c754ea28f64ea747a49a/DONTREADME.md#relevant-phrase-identification): Based on cosine similarity between input text and each word in [the vocabulary](https://github.com/8ta4/pun/blob/a745263dc93952a0f6f8c754ea28f64ea747a49a/DONTREADME.md#vocabulary), words like "pun", "phonetic", or "similarity" might pop up as relevant.

2. [Phonetic Similarity Analysis](https://github.com/8ta4/pun/blob/a745263dc93952a0f6f8c754ea28f64ea747a49a/DONTREADME.md#phonetic-similarity-analysis): "pun" would match as phonetically similar to "fun" using Levenshtein distance between IPA representations.

3. [Substitution](https://github.com/8ta4/pun/blob/a745263dc93952a0f6f8c754ea28f64ea747a49a/DONTREADME.md#substitution): The word "fun" is swapped out for "pun" within the phrase "make fun of", resulting in "make pun of".

Are there any major flaws I'm missing? I haven't started writing the production code yet. I'm looking for feedback before diving in.
