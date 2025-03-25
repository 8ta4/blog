I'm thinking about building a pun generator. The challenge isn't just making puns; it's making sure they're understandable. Nobody wants a pun that uses some ridiculously obscure word.

That's where this whole LLM-as-survey thing comes in. Instead of doing time-consuming surveys to figure out which words people know, I'm exploring using an LLM to pre-calculate "recognizability scores".

The bigger picture here is that this isn't just about puns. This is about using LLMs to estimate subjective qualities as a substitute for large-scale surveys. This technique seems applicable to other situations.

Are there any blind spots I'm overlooking? I'm especially interested in improving both [the prompt](https://github.com/8ta4/pun/blob/e347a17100d5339e6f2673e4eb8a9527f24134e0/system.txt) and [the normalization technique](https://github.com/8ta4/pun/blob/e347a17100d5339e6f2673e4eb8a9527f24134e0/DONTREADME.md?plain=1#L125-L181).

I figured it'd be smarter to get some advice from you all first. But I'm tempted to just jump the pun and start building already! 
