I recently needed a way to measure how familiar or well-known English words and phrases actually are for a project. Simple frequency lists weren't cutting it. For example, "pellucid" might appear more often in text than "ungoogleable," but far fewer people actually know "pellucid." Frequency also gets tricky with multi-word phrases.

To tackle this, I decided to generate familiarity scores using LLMs. I tested several models that were top-ranked on the Chatbot Arena Leaderboard at the time, and Claude 3.7 Sonnet consistently gave the most plausible results for this specific task, distinguishing everyday language from jargon more effectively than others.

Using the Batch API, I ended up spending about $300 USD to generate these scores for roughly 1 million Wiktionary entries. The specific metric I aimed for was an estimate of the percentage of Americans aged 10+ who would know the most common meaning of each word or phrase.

The dataset and the code used to generate it are both open-source. You could take the code and adapt the approach for other languages.

While Claude 3.7 Sonnet performed best in my tests for this nuanced task, the $300 cost for this Wiktionary dataset makes scaling up to score Wikipedia titles seem prohibitively expensive with the same approach. It might take them several major versions to bring the price down for this level of quality.... But hey, if they finally do, I'll be on Claude Nine.

So, I'd appreciate any thoughts for doing large-scale data generation like this with LLMs without breaking the bank.
