I'm thinking about building a pun generator. The challenge isn't just making puns; it's making sure they're understandable. Nobody wants a pun that uses some ridiculously obscure word.

That's where this whole LLM-as-survey thing comes in. Instead of doing time-consuming surveys to figure out which words people know, I'm exploring using an LLM to pre-calculate "recognizability scores".

The bigger picture here is that this isn't just about puns. This is about using LLMs to estimate subjective qualities as a substitute for large-scale surveys. This technique seems applicable to other situations.

Right now, this is all theoretical. I haven't written any production code yet.

I'm especially interested in improving both [the prompt itself](https://github.com/8ta4/pun/blob/1ddf70b8b355e5ed3f7f142fc67340238c461837/prompt.txt) and [the normalization technique](https://github.com/8ta4/pun/blob/1ddf70b8b355e5ed3f7f142fc67340238c461837/DONTREADME.md?plain=1#L109-L147).

Are there any blind spots I'm overlooking? I appreciate any feedback!
