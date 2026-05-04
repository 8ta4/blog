[Cerebras](https://www.cerebras.ai) hosts [gpt-oss-120b](https://openai.com/index/introducing-gpt-oss) at [~3000 tokens/s](https://inference-docs.cerebras.ai/models/overview). But things can change once the buffer hits the load. Is there another production-ready model and provider combination that beats this setup for end-to-end response time while maintaining a similar level of reasoning?

I'm building [an in-place, sentence-by-sentence rephraser](https://github.com/8ta4/word) and need the full response back in the buffer in under one second.

Any other feedback on [the design](https://github.com/8ta4/word/blob/319a7cb1283e8b2f329567900afef4ddad9d127d/DONTREADME.md) is also welcome.
