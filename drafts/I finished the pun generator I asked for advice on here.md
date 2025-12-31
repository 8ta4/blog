I've released a proof of concept for [a pun generator](https://github.com/8ta4/pun). This is a follow-up to these two previous discussions:

- [Looking for a tool that generates phonetically similar phrases for pun generation](https://old.reddit.com/r/LanguageTechnology/comments/1ir9v7c/looking_for_a_tool_that_generates_phonetically/)

- [Feedback wanted: a pun-generation algorithm, pre-coding stage](https://old.reddit.com/r/LanguageTechnology/comments/1jmzf2b/feedback_wanted_a_pungeneration_algorithm/)

u/SuitableDragonfly mentioned that using Levenshtein distance on IPA is a blunt instrument since ["it treats all replacements as equal"](https://old.reddit.com/r/LanguageTechnology/comments/1jmzf2b/feedback_wanted_a_pungeneration_algorithm/mki366o/#:~:text=it%20treats%20all%20replacements%20as%20equal). While certain swaps feel more natural for puns, quantifying those weights is easier said than pun. I checked out [PanPhon](https://github.com/dmort27/panphon), but it considers /pʌn/ and /pʊt/ to be more similar than /pʌn/ and /ɡʌn/. I decided to stick with unweighted Levenshtein for now.

u/AngledLuffa was worried about the tool trying to replace function ["words like 'the'"](https://old.reddit.com/r/LanguageTechnology/comments/1jmzf2b/feedback_wanted_a_pungeneration_algorithm/mkgrd12/#:~:text=position%20of%20replacing-,words%20like%20%22the%22,-or%20other%20irrelevant). By pivoting the tool to take keywords as input rather than parsing a whole article for context, I bypassed that problem.

I used Claude 3.7 Sonnet to calculate recognizability scores for the vocabulary ahead of time based on how familiar each phrase is to a general audience. You might wonder why I used such an old model. It was the latest model at the time. I put these pre-computed scores in the [pun-data](https://github.com/8ta4/pun-data) repository. They might be useful for other NLP tasks.

I built this with Clojure because I find it easier to handle data processing there than in Python. I'm calling Python libraries like Epitran through [libpython-clj](https://github.com/clj-python/libpython-clj). Since Clojure's JVM startup is slow, I used Haskell for the CLI to make the tool feel responsive.
