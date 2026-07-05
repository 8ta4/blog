I need a huge collection of common English words and phrases that pretty much includes all the standard dictionary entries, for example a complete Wiktionary dump.

I want each entry assigned a numeric score that shows how negative the concept is.

| entry         | score |
| ---           | ---   |
| serial killer | 0.98  |
| fraud         | 0.85  |
| office desk   | 0.10  |
| sunshine      | 0.02  |

I know about the dataset from that paper, ["Using large language models to estimate features of multi-word expressions: Concreteness, valence, arousal".](https://arxiv.org/abs/2408.16012) It's the closest thing I've found so far. But it's missing a lot of common Wiktionary phrases that I actually need.

I could grab a Wiktionary dump of common words and phrases, then run them through an LLM to get the numeric scores myself. But I wanted to check if I could skip the effort before I waste time and API credits.

Has anyone already put out a valence dataset like this?
