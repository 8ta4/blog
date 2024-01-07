I'm working on an open-source project called `say`, which transcribes voice 24/7.

How can I slash latency big time but still keep the accuracy of the prerecorded API intact?

Here's what I'm aiming for:
- [Accuracy](https://github.com/8ta4/say/blob/28276acd622fd2cd8d0f86568534361927ddf363/DONTREADME.md#accuracy): I want to match the accuracy of the prerecorded API.
- [Latency](https://github.com/8ta4/say/blob/28276acd622fd2cd8d0f86568534361927ddf363/DONTREADME.md#latency): I want to cut down Deepgram's latency to around [300 ms](https://deepgram.com/product/transcription#:~:text=time%20streaming%20lag-,%3C300%20ms,-Not%20available) to keep the overall process under a second..
- [Budget](https://github.com/8ta4/say/blob/28276acd622fd2cd8d0f86568534361927ddf363/DONTREADME.md#budget): Given that this is an open-source project, the solution needs to be cost-effective.

The streaming API doesn't quite hit the mark in terms of accuracy. And I suspect that the TCP slow start might be the culprit behind the latency issues with the prerecorded API. For reference, I'm using [Opus](https://github.com/8ta4/say/blob/28276acd622fd2cd8d0f86568534361927ddf363/DONTREADME.md?plain=1#L157) with [a 24kbps bitrate](https://github.com/8ta4/say/blob/28276acd622fd2cd8d0f86568534361927ddf363/DONTREADME.md?plain=1#L165) and [a gigabit connection in the continental US](https://github.com/8ta4/say/blob/28276acd622fd2cd8d0f86568534361927ddf363/DONTREADME.md?plain=1#L251).

Here are a couple of potential solutions I've thought of:
- Hybrid API: Deepgram could potentially offer an API that allows for real-time audio streaming to be temporarily stored and then processed using the prerecorded API once the streaming is complete. This could bypass the initial upload delay and maintain high accuracy.
- On-Premise Hosting: Deepgram has [an enterprise on-premise solution](https://deepgram.com/pricing). But maybe they can offer a cheaper on-premise hosting solution that open-source projects can use.

I realize that these solutions might require significant development on Deepgram's part. So, I'm open to any suggestions or alternative strategies.
