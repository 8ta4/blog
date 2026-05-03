I'm thinking about building a tool to discover backronyms for initialisms, like Married But Available for MBA. Since the potential search space for these word combinations follows V^n, where V is the vocabulary size, finding funny sequences is a discovery challenge.

I've mapped out a workflow:

1. Seeding. Extract over 10,000 English initialisms from Wiktionary.

2. Filtering. Use a recognizability dataset to reduce the list to a recognizable subset that most people would know.

3. Mining. Match these seeds against the Google Ngram dataset for all 2- to 5-gram sequences.

4. Ranking. Categorize the resulting phrases by their initialism and sort them by frequency, capping the count per bucket to keep the volume manageable.

5. Judging. Use a large language model as a judge to scan the lists for funny expansions, since models are good at recognizing a joke even if they're bad at inventing one.

My biggest concern with this approach is the frequency distribution. "Married But Available" does appear in the Google Ngram dataset. But it's roughly a million times rarer than a sequence like "may be a". If the funny candidates are buried too deep in the tail, they might be dropped before the model sees them.

Does any systematic solution or dataset for this problem already exist? Any other feedback is welcome.
