I have scored over a million English entries from Wiktionary for recognizability. I built this for a pun tool. But I want to use the data for a new language project.

The dataset is way too bloated right now because it's full of inflected forms. Even if I set the recognizability threshold at 50 percent, I'm still looking at 100K words and 100K phrases. Going through a list that size is a waste of time. I need to filter the data through the English lemmas category from Wiktionary and split the single words from the multi-word phrases into separate lists.

Since the hard part of scoring is done, the rest should be easy peasy lemma squeezy. I just want to avoid reinventing the wheel if I can.

Before I spin up a separate repository to handle this, I'm checking if a similar dataset already exists. Has anyone seen a project that offers this?
