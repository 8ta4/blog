Are there any speech-to-text APIs that can give word-level probabilities, match or beat Deepgram in accuracy, and have low latency for short audio?

Here's what I need from a speech-to-text API, in order of importance:

1. Word-level confidence: I need a probability score for each word in the transcript.

1. Accuracy: The API must be accurate, especially for common words in clear audio, finalizing the transcription only after the user finishes a sentence to make sure full context is considered.

1. Latency: The API needs to be fast, ideally under 0.25 seconds per call, so the whole process finishes in under a second.

1. Cost: It should be affordable, aiming for under $100 a month for heavy use.

1. Cross-origin resource sharing (CORS): This isn't a must-have, but it would be nice if the API supports CORS for direct use from the browser.

Deepgram claims to be the most accurate, fastest, and cheapest API, but I ran into two issues:

1. Latency: Deepgram usually takes about 0.5 seconds to return a transcript for a single sentence. Most of this time is spent on TCP slow start, making the network the bottleneck.

1. CORS: Deepgram doesn't support CORS, which is a bummer for browser-based apps.

I've tested several APIs mentioned in Deepgram's blog post "Best Speech-to-Text APIs in 2024." Only Deepgram and Whisper met my latency requirement of under 1 second. However, Whisper doesn't provide word-level probabilities, which is a dealbreaker for my project.

Comparing speech-to-text API accuracy has been so fruitful just like comparing apples to oranges, as many providers claim their solution is the best. This self-serving marketing makes it hard to determine the true accuracy of each API.

To give you a bit more context, I'm designing an app that checks pronunciation. The goal is for the whole process to take less than a second. This involves three API calls: two for speech-to-text and one for text-to-speech. The text-to-speech call takes about 0.5 seconds, so each speech-to-text call needs to be around 0.25 seconds. I'm still figuring out if this is even possible.  If you want to give me some feedback on the design, here's the link!

Given all these requirements and challenges, I'm looking for recommendations for speech-to-text APIs.
