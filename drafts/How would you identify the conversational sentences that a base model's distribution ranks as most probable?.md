Extracting common conversational sentences is difficult because most datasets are either too small or collected in artificial settings. I'm looking into mining these sentences from a base model's probability distribution instead. The plan is to prime the model with an informal opening and then rank the results by their log-likelihood to find what it considers most probable. I'm using the model's distribution as a proxy, even though the probabilities won't match real-world frequencies.

When a guy asked why I wasn't mining something useful like business data instead of this, I told him to mine his own business.

I haven't built the pipeline yet, but I've detailed [the strategies](https://github.com/8ta4/cue/blob/0942e7fe5013b3dc2ab72852b7751acbcc7e806d/DONTREADME.md).

How would you go about identifying the conversational sentences that a model's distribution considers most probable?
