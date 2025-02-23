I'm on the hunt for a dataset that tells me what percentage of British folks would actually recognize different words and phrases. Recognition means having heard a word or phrase before and understanding its meaning.

I need this for a couple of things.

- I'm building a pun generator to crack jokes like Jimmy Carr. Puns flop hard if people don't recognize the starting words or phrases.

- I wanna level up my British vocab. I'd rather learn stuff most Brits know instead of random obscure bits.

While my focus is on British English, a dataset like this could also work for general English.

I'm thinking of using language models to evaluate millions of words and phrases.

Here's exactly what I'm looking for:

- All the titles from Wiktionary should be in there so we've got all the basic language covered.

- All the titles from Wikipedia need to be included too for all the cultural stuff.

- Each word and phrase needs a score, like "80% of Brits know this."

- The prompt needs a benchmark word to normalize scores across multiple evaluation runs by adjusting everything else proportionally if the benchmark's score changes.

- The language model needs to give the same output for the same input every time so results can be verified before any model updates change the recognizability scores.

- It should get updated every year to keep up with language shifts like "Brexit."

- If I build this myself, I want to keep the total compute cost under $1,000 per year.

Regular frequency lists just don't cut it:

- They miss rare words people still know. "Pellucid" is just a rare word by itself, while "ungooglable" comes from "google" which everyone knows.

- With single words, it's doable but complicated. You need to count across all forms like "knock," "knocks," "knocked," "knocking."

- Phrases are trickier. With the phrase "knock up", you need to count across all the different objects like "knock my flatmate up," "knock her up."  She has a pun in the oven.

I'm curious if there's a smarter way to do it. Hit me with your feedback or any advice you've got! Have you seen anything like this?
