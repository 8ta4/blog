I'm thinking about building a pun generator. The challenge isn't just making puns; it's making sure they're understandable. Nobody wants a pun that uses some ridiculously obscure word.

That's where this whole LLM-as-survey thing comes in. Instead of doing time-consuming surveys to figure out which words people know, I'm exploring using an LLM to pre-calculate "recognizability scores".

The bigger picture here is that this isn't just about puns. This is about using LLMs to estimate subjective qualities as a substitute for large-scale surveys. This technique seems applicable to other situations.

Are there any blind spots I'm overlooking? I'm especially interested in improving both [the prompt itself](https://github.com/8ta4/pun/blob/e11d663b987880c94b3165e55d42bd1545fb178d/prompt.txt) and [the normalization technique](https://github.com/8ta4/pun/blob/e11d663b987880c94b3165e55d42bd1545fb178d/DONTREADME.md?plain=1#L107-L155).

I figured it'd be smarter to get some advice from you all first. But I'm tempted to just jump the pun and start building already! 
