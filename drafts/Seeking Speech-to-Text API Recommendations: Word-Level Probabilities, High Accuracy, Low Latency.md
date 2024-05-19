Are there any speech-to-text APIs that can give word-level probabilities, match or beat Deepgram in accuracy, and have low latency for short audio?

Here's what I need from a speech-to-text API, in order of importance:

1. Word-level confidence: I need a probability score for each word in the transcript.

1. Accuracy: It has to be accurate, especially for common words in clear audio.

1. Latency: The API needs to be fast, ideally under 0.25 seconds per call, so the whole process finishes in under a second.

1. Cost: It should be affordable, aiming for under $100 a month for heavy use.

1. Cross-origin resource sharing (CORS): This isn't a must-have, but it would be nice if the API supports CORS for direct use from the browser.

Deepgram claims to be the most accurate, fastest, and cheapest API, but I ran into two issues:

1. Latency: Deepgram usually takes about 0.5 seconds to return a transcript for a single sentence. Most of this time is spent on TCP slow start, making the network the bottleneck.

1. CORS: Deepgram doesn't support CORS, which is a bummer for browser-based apps.

Most speech-to-text providers offer different types of transcription, like Deepgram's streaming API and prerecorded API. The streaming API gives low latency by processing audio as it comes in but sacrifice accuracy since it can't consider future context. The prerecorded API can be more accurate by taking more context into account but usually has higher latency. Ideally, I want a prerecorded API that can send data as it's captured to avoid TCP slow start issues and strike a good balance between latency and accuracy.

I've tested several APIs mentioned in Deepgram's blog post "Best Speech-to-Text APIs in 2024." Only Deepgram and Whisper met my latency requirement of under 1 second. However, Whisper doesn't provide word-level probabilities, which is a dealbreaker for my project.

Comparing speech-to-text API accuracy has been so fruitful just like comparing apples to oranges, as many providers claim their solution is the best. This self-serving marketing makes it hard to determine the true accuracy of each API.

Given all these requirements and challenges, I'm looking for recommendations for speech-to-text APIs.
