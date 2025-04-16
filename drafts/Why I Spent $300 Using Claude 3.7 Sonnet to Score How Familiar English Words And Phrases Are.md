I needed a way to measure how familiar or well-known English words and phrases actually are. To tackle this, I tested several models that were top-ranked on the Chatbot Arena Leaderboard at the time, and Claude 3.7 Sonnet consistently gave the most plausible results, distinguishing everyday language from jargon more effectively than others.

Using the Batch API, I ended up spending about $300 USD to generate these scores for roughly 1 million Wiktionary entries. The specific metric I aimed for was an estimate of the percentage of Americans aged 10+ who would know the most common meaning of each word or phrase.

The dataset and the code used to generate it are both open-source. You could take the code and adapt the approach for other languages.

While Claude 3.7 Sonnet performed best in my tests for this task, the $300 cost for this Wiktionary dataset makes scaling up to score Wikipedia titles seem prohibitively expensive. It might take Anthropic several major versions to bring the price down.... But hey, if they finally do, I'll be on Claude Nine.

So, I'd appreciate any thoughts for doing large-scale data generation without breaking the bank.
