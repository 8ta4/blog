Are there any speech-to-text APIs that can give word-level probabilities, match or beat [Deepgram](https://deepgram.com) in accuracy, and have low latency for short audio?

About a month ago, I shared [my experience](https://old.reddit.com/r/AskProgramming/comments/1btmazw/looking_for_alternatives_to_deepgrams_whisper) with Deepgram on this subreddit, and the response was incredible. Recently, u/111ewe111 asked me what specific issues I was having with Deepgram. So, I thought I'd make this new post to answer those questions and the feedback I got since my needs have changed.

Here's what I need from a speech-to-text API, in order of importance:

1. Word-level probability: I need a probability for each word in the transcript.

1. Accuracy: The API must be accurate, especially for common words in clear audio, finalizing the transcription only after the user finishes a sentence to make sure full context is considered.

1. Latency: The API needs to be fast, ideally under 0.25 seconds per call for a single sentence.

1. Cost: It should be affordable, aiming for under $1.215 per hour.

1. Cross-origin resource sharing (CORS): This isn't a must-have, but it would be nice if the API supports CORS for direct use from the browser.

Comparing speech-to-text API accuracy has been fruitful, like comparing apples to oranges, as many providers claim their solution is the best. This self-serving marketing makes it hard to determine the true accuracy of each API.

I checked out a bunch of APIs that Deepgram mentioned in their blog post "[Best Speech-to-Text APIs in 2024](https://deepgram.com/learn/best-speech-to-text-apis)." Only the [Nova-2](https://developers.deepgram.com/docs/models-languages-overview#nova-2) model from Deepgram and the [Whisper API](https://platform.openai.com/docs/guides/speech-to-text/speech-to-text) from OpenAI were able to return the API call within one second. But the Whisper API that OpenAI provides doesn't give you word-level probabilities. That's a dealbreaker.

Deepgram claims to be [the most accurate and fastest API](https://deepgram.com/learn/best-speech-to-text-apis#:~:text=Deepgram%20released%20Deepgram%20Nova%2D2%2C%20the%20fastest%2C%20most%20accurate%20STT%20model%20in%20the%20world.), but I ran into two issues:

1. Latency: Deepgram usually takes about 0.5 seconds to return a transcript for a single sentence. Most of this time is spent on TCP slow start, making the network the bottleneck.

1. CORS: Deepgram [doesn't support CORS](https://github.com/deepgram/deepgram-js-sdk/blob/bd51da7ce06c59b3dea55e4a915e802bd43a3754/README.md?plain=1#L148), which is a bummer for browser-based apps.

Most speech-to-text providers give you options like a streaming API and a prerecorded API. Take Deepgram, for example.

With [their streaming API](https://developers.deepgram.com/docs/getting-started-with-live-streaming-audio), you get low latency because it processes the audio bit by bit as it comes in. But it might end up finalizing the transcription in the middle of a sentence. When that happens, the API loses the context for the rest of what's being said, which can sacrifice accuracy.

Now, if you go with [their prerecorded API](https://developers.deepgram.com/docs/getting-started-with-pre-recorded-audio), you'll probably get better accuracy since it looks at the full context of the audio. However, you're sending the whole audio file over, which can run into TCP slow start issues.

There are a few potential solutions:

- A hybrid API that captures audio incrementally like streaming, but only finalizes transcriptions at the end of sentences.

- On-device transcription to eliminate network latency.

To give you a bit more context, I'm designing an app that checks pronunciation. The goal is for the whole process to take less than a second. This involves three API calls: two for speech-to-text and one for text-to-speech. The text-to-speech call takes about 0.5 seconds, so each speech-to-text call needs to be around 0.25 seconds. I'm still figuring out if this is even possible. If you want to give me some feedback on the design, here's the [link](https://github.com/8ta4/accent)!

All the latency numbers in this post were tested using [Google Colab](https://colab.research.google.com). It runs on Google's infrastructure, which helps minimize network latency. This way, I can be pretty sure that the network itself isn't the bottleneck during these tests.

Now, let’s talk about cost. I have a budget of $100 per month, assuming 30 hours of usage each month. That gives me:

$$\frac{\$100}{30 \text{ hours}} \approx \$3.33 \text{ per hour}$$

I have three API calls: two for speech-to-text and one for text-to-speech. Let's estimate the number of characters processed in an hour. Assuming a fast speaker at 200 words per minute and 5 characters per word, I get:

$$200 \text{ words/min} \times 60 \text{ min/hour} \times 5 \text{ characters/word} = 60,000 \text{ characters/hour}$$

I'll use OpenAI's text-to-speech API, which costs [$15 per million characters](https://openai.com/api/pricing/#:~:text=TTS-,%2415.00%20/,1M%20characters,-TTS%20HD). The cost per hour for text-to-speech is:

$$60,000 \text{ characters/hour} \times \frac{\$15}{1,000,000 \text{ characters}} = \$0.90 \text{ per hour}$$

Next, I subtract the text-to-speech cost from my total hourly budget:

$$\$3.33 - \$0.90 = \$2.43 \text{ per hour}$$

This $2.43 covers my two speech-to-text API calls:

$$\frac{\$2.43}{2} = \$1.215 \text{ per hour}$$

Given all these requirements and challenges, I'm looking for recommendations for speech-to-text APIs.
