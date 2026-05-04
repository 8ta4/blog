I asked on r/datasets about frequency-based datasets for small talk questions but didn't get anywhere. I'm still looking for a resource like this, though I've refined what I'm after.

I want this data because I treat social skills training like test prep. I want to practice with the questions most likely to appear in a conversation.

I have a few requirements for the data:

- The questions should be sampled broadly from the entire space of small talk.

- The list should have at least a thousand items.

- It needs a vetted likelihood score for how typical a question is. This lets me prioritize the most common stuff. For example, "How was your weekend?" should score higher than "What is your favorite period of architecture?".

- Every question should be in its simplest form. Instead of "If you could go anywhere in the world for a vacation, where would you choose?", it should just be "Where do you want to travel?".

There are existing resources like the book Compelling Conversations and online lists. The problem with these is they seem based on subjective opinions rather than systematic sampling.

There are two main ways to build a dataset like this. One is extracting questions from real conversation datasets, though that requires a lot of cleaning. The other way is generating a synthetic dataset by prompting an LLM to create common questions, which would likely result in a higher signal-to-noise ratio.

To handle the likelihood scoring, an LLM could act as a judge to rank how typical each question is. Using an LLM just replaces human bias with training bias, but I'd rather have a score based on an LLM's training data than a random author's opinion.

To get to the simplest form, an LLM could be used to standardize the phrasing. From there, you could group similar questions into connected components based on cosine similarity and pick the one with the highest likelihood score as the representative for that group.

I'm open to suggestions on the approach.

I'm starting with questions, but I'd eventually want to do this for statements too.

I'd rather not build this pipeline myself if I can skip that hassle.

Has anyone built or seen anything like this?
