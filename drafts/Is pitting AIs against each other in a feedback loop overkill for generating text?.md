I'm trying to design a system for text generation.

My core idea is a refinement loop where AIs compete to improve a piece of text. Here's the process:

1. The process starts with a baseline draft.

1. One AI rewrites that draft to improve it.

1. A different AI compares the new version to the original and picks the winner.

1. The winning draft becomes the new baseline for the next round.

This process repeats until the baseline draft wins a round, which signals that the rewritten version is no longer an improvement.

I've documented my thinking on GitHub [here](https://github.com/8ta4/spam).

The success hinges on the subjective call of the AI that picks the winner. Beauty is in the AI of the beholder.

There are probably practical reasons why this isn't a more common approach.

What are the superior alternatives to this approach?
