What killer features would you want in your ideal pronunciation grading app?

Over a month back, I [asked](https://old.reddit.com/r/languagelearning/comments/1cd0b5c/seeking_a_pronunciation_grader_that_allows_any/) if anyone knew of a pronunciation grading app that could provide feedback on how close you are to a target accent. I didn't find what I was looking for, so I thought, "Why not build it myself?"

I got [this suggestion](https://old.reddit.com/r/languagelearning/comments/1cd0b5c/seeking_a_pronunciation_grader_that_allows_any/l19l2i1/) from u/Antoine-Antoinette in that thread. They said the app should let you evaluate multi-word phrases and sentences without having to pause or hit any keys between words. So I implemented it to encourage a more natural flow. They also mentioned that they were using Google Translate for pronunciation practice as a DIY solution, which got me thinking.

I decided to compare different speech recognition providers, including Google's offering. I felt like [Deepgram](https://deepgram.com/) was more accurate than Google Translate. Plus, I found some benchmarks that suggested [Google's speech-to-text has a pretty high word error rate](https://github.com/Picovoice/speech-to-text-benchmark?tab=readme-ov-file#word-error-rate-wer:~:text=to%2DText%20Enhanced-,6.2%25,-13.0%25) compared to some of its competitors. That's why my app is using Deepgram for speech recognition.

At first, I was planning to make it a web app so it'd be easy for everyone to access. But I ended up making [a desktop version](https://github.com/8ta4/accent) for Mac because I was lazy. The tool does require a bit of technical knowledge to run, but it's at a point where it could be useful for learners if they are comfortable with technology. I wanted to share this update to wrap up the previous discussion and let you all know that this tool is out there.

So, my accent coach asked me, "What do you hope to achieve with this app?" I said, "I want to perfect my accent so there's no room for misinterpretation when I say, 'You're fired.'"

Anyway, if you have any other suggestions, I'm all ears.
