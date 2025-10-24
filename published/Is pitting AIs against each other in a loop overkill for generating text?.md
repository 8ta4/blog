I'm sketching out a system for text generation and wanted to get your take on the architecture.

The idea is an iterative refinement loop. You have two AIs competing to improve a draft. The process goes like this:

1. You start with a baseline text.

1. One AI takes a pass at rewriting it.

1. A different AI compares the new version to the original and picks the better one.

1. Whichever version wins becomes the new baseline for the next round.

You keep running that loop until the baseline draft wins, which means the latest rewrite wasn't an improvement.

I dumped my thoughts into a [repo](https://github.com/8ta4/spam).

The effectiveness hinges on the subjective call of the AI that picks the winner. Beauty is in the AI of the beholder.

There are probably practical reasons why this isn't a more common setup. What are the superior alternatives I'm not thinking of?
