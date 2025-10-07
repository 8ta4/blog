I needed a way to measure how well-known English words and phrases actually are. I was trying to nail down a score estimating the percentage of Americans aged 10+ who would know the most common meaning of each word or phrase.

So, I threw a bunch of the top models from the Chatbot Arena Leaderboard at the problem. Claude 3.7 Sonnet consistently gave me the most believable scores. It was better than the others at telling the difference between everyday words and niche jargon.

[The dataset](https://github.com/8ta4/pun-data/blob/c3c0f293ab7c18d9d356e817802ca16f35651ed6/normalized.edn.gz) and [the code](https://github.com/8ta4/pun/blob/28f7e988f0d244433f60d359661c22cf2d55ca95/src/core.clj) are both open-source.

You could mess with that code to do something similar for other languages.

Even though Claude 3.7 Sonnet rocked, dropping $300 just for Wiktionary makes trying to score all of Wikipedia's titles look crazy expensive. It might take Anthropic a few more major versions to bring the price down.... But hey, if they finally do, I'll be on Claude Nine.

Anyway, I'd appreciate any ideas for churning out datasets like this without needing to sell a kidney.
