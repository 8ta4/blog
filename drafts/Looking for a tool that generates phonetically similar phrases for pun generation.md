I write jokes for a living. Well, I'm trying to anyway. And let me tell you, comedy isn't all pun and games. It takes a lot of systematic work. I've been thinking about how to make my life easier by automating some of the grunt work, especially when I'm writing articles and video scripts.

So here's what I'm trying to do:

1. Generate relevant phrases based on my content

2. Take these phrases and find phonetically similar variations

3. Filter out the ones that don't make sense

Let's use this post as an example:

Step 1 would generate phrases like "fun and games"

Step 2 would give me variations like "pun and games" or "gun and games"

Step 3 would keep "pun and games" but toss out "gun and games" because this post isn't about guns

I tried [using large language models to automate steps 1-3](https://github.com/8ta4/gag/blob/25017ec6a95c2764d1a35d6e2063c5addf6f4e5b/README.md#wordplay) end-to-end, but it just didn't work as well as I hoped. These models don't really explore enough options to find good puns. Plus, it burns through a ton of tokens.

Large language models are great at step 1 (coming up with phrases) and step 3 (filtering for meaning), but step 2 (finding and replacing words based on sound) needs a more systematic, combinatorial approach.

What I need is a tool that can handle step 2. It should:

2.1. Take phrases I give it

2.2. Find words that sound alike and swap them in

2.3. Sort them by how close they sound to the original

I've checked out [Rhymezone](https://www.rhymezone.com) and [Pun Generator](https://pungenerator.org), but they only work with one word at a time. I need something that can handle whole phrases and give me variations that sound similar.

Does something like this exist? I'd also love to hear possible ways to build something like this or if there's a better approach I haven't thought of.
