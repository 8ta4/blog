They say puns are the lowest form of humor. When I say I'm building a tool to automatically generate puns, they make pun of me!

My goal is straightforward: create word-swapping puns that are easy to understood and relevant to the input.

Let me walk through a quick example. Say I wanted to create puns for this Reddit post:

1. [Relevant Word Identification](https://github.com/8ta4/pun/blob/1ddf70b8b355e5ed3f7f142fc67340238c461837/DONTREADME.md?plain=1#L189-L211): Based on cosine similarity between input text and each word in [the vocabulary](https://github.com/8ta4/pun/blob/1ddf70b8b355e5ed3f7f142fc67340238c461837/DONTREADME.md?plain=1#L37-L187), words like "pun", "phonetic", or "similarity" might pop up as relevant.

2. [Phonetic Similarity Analysis](https://github.com/8ta4/pun/blob/1ddf70b8b355e5ed3f7f142fc67340238c461837/DONTREADME.md?plain=1#L213-L235): "pun" would match as phonetically similar to "fun" using Levenshtein distance between IPA representations.

3. [Substitution](https://github.com/8ta4/pun/blob/1ddf70b8b355e5ed3f7f142fc67340238c461837/DONTREADME.md?plain=1#L237-L261): The word "fun" is swapped out for "pun" within the phrase "make fun of", resulting in "make pun of".

Are there any major flaws I'm missing? haven't started writing the production code yet. I'm looking for feedback before diving in.
