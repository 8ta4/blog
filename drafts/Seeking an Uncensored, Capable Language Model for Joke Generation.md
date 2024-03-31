Does anyone know of a language model that is uncensored but also has strong text generation capabilities?

I'm working on this project to automatically generate jokes using language models.

The idea is to generate edgy punchlines, then for each punchline, generate a corresponding setup to misdirect the audience. After that, I'll filter out the duds by comparing the full jokes to a professional reference joke.

Here's an example of the kind of joke I'm using as a reference, from comedian Jimmy Carr:

Setup: "I would think about adoption. I don't have kids. But if I had kids,"

Punchline: "I think I would have them adopted."

My process looks like this:

1. Come up with an edgy punchline related to a given topic (currently using [Dolphin 2.6 Mixtral 8x7b](https://huggingface.co/cognitivecomputations/dolphin-2.6-mixtral-8x7b))

2. Create an innocent-sounding setup to misdirect the audience (also using Dolphin 2.6 Mixtral 8x7b)

3. Compare the complete joke to a professional reference joke to see how it stacks up (using GPT-3.5 Turbo)

For more details on the goals of this project, check out my [project documentation](https://github.com/8ta4/gag/blob/bb2d1966eeb459f5f68576e2f0fcc2c499da9fba/DONTREADME.md).

Now, step number one is where I'm running into the most trouble. To generate a really edgy punchline, you need an uncensored model. And that's where most models fall short.

Dolphin 2.6 Mixtral 8x7b is sweet because it's uncensored and can generate the kind of envelope-pushing humor I need for the punchlines. But in terms of raw language generation ability, it falls a bit short. The punchlines it generates often lack edge.

If there are way too many jokes to evaluate, it starts getting pricey. And the evaluation step isn't foolproof either - there could be some false positives that slip through. So I need to keep the number of punchlines reasonable.

On the other hand, Claude Opus can generate some seriously high-quality text. But it's censored, even more than GPT-4. So it struggles with the darker topics that a lot of jokes revolve around.

What I'm after is the best of both worlds - the no-holds-barred style of Dolphin Mixtral with the general capability of Claude Opus.

If anyone has tips, I'm all ears!
