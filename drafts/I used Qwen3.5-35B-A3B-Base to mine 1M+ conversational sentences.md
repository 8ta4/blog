I [posted](https://old.reddit.com/r/LanguageTechnology/comments/1q3g3tx/looking_for_a_systematically_built_dataset_of/) on r/LanguageTechnology looking for a frequency-ranked dataset for small talk. What I wanted was something like test prep for conversation.

I couldn't find anything like that, so I built it myself.

This wasn't a matter of sampling a bunch of outputs and keeping the good ones. Instead, it was closer to an exhaustive search over one-sentence conversational completions above a likelihood threshold. If a sentence had conditional probability greater than 1 in 100 million, it was in scope.

Even with that setup, the run on [Qwen3.5-35B-A3B-Base](https://huggingface.co/Qwen/Qwen3.5-35B-A3B-Base) finished in under 10 hours. The model fit on an [H100](https://www.nvidia.com/en-us/data-center/h100/). But I used an [H200](https://www.nvidia.com/en-us/data-center/h200/) to push batch size higher. I ran it on [Nebius](https://nebius.com/), where it cost [a few dollars per hour](https://nebius.com/prices#:~:text=200-,%243.50,-NVIDIA%20HGX%20H100).

The result was [a gzipped CSV](https://github.com/8ta4/cues/blob/8914d9815a706950528d5512a931ec9e253b3e1e/cues.csv.gz) with 1M+ candidate sentences. To give a feel for the output, here are a few examples from different parts of the ranking:

1: No.

10: Why?

100: Why not?

1,000: You don't know.

10,000: What do I get?

100,000: You should not do that.

1,000,000: I'm not calling 911.

[The docs](https://github.com/8ta4/cue/blob/main/DONTREADME.md) already explain the implementation, so I'll leave that part out.

This doesn't feel like a typical use of a base model. Open models make this kind of thing possible. I'm curious what other unconventional uses people have found.
