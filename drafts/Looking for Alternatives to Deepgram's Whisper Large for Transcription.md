Are there any transcription APIs that can quickly transcribe audio recordings in multiple languages, without the reliability issues of [Deepgram's Whisper](https://deepgram.com/learn/improved-whisper-api) Large model?

Requirements:
- Language Support: A service that's strong in multiple languages at least on par with Deepgram's Whisper Large model.
- Speed and Reliability: Looking to transcribe [60-second audio recordings within a second](https://github.com/8ta4/say/blob/ec3f41851f22a5847ebcce4af14565fdede35547/DONTREADME.md#latency) or slightly more.
- Affordability: Competitively priced with Deepgram's [$0.0048 per minute](https://deepgram.com/pricing#:~:text=Whisper%20Large-,%240.0048/min,-%240.0048/min).

Considered Options:
- Self-Hosted Whisper: I want to avoid setting up something like Whisper by myself.
- Deepgram's Whisper Large: The varying speeds of Deepgram's Whisper Large, sometimes taking over 10 seconds for just a few seconds of audio, are problematic. I'm developing [this app](https://github.com/8ta4/say) to be an always-on transcription tool. But with these delays, it's more like it's always on a coffee break.
- [Deepgram's Nova-2 Model](https://deepgram.com/learn/nova-2-speech-to-text-api): I've been using Deepgram's Nova-2 model for transcribing English audio, and it's been great because of how fast and accurate it is. But now, I need something that can handle more languages.
