A couple of months ago, I embarked on a journey to find the perfect 24/7 speech-to-text transcription tool. It all started with a simple [post](https://old.reddit.com/r/speechrecognition/comments/16b6kd4/247_speechtotext_transcription_tool_wanted/) on this subreddit. Now, I've got a question I'm hoping you can help with: **What's the ideal microphone for this task?** I'm all ears for feedback!

The biggest hurdle has been finding the right microphone. I have two main requirements: it needs to be **comfortable enough to wear all day** and **precise enough to isolate and transcribe my voice**. A wireless connection would be a bonus. Accuracy is key here, as it's important that the microphone can isolate my voice effectively. u/Economics-Regular [suggested an ear bone microphone](https://old.reddit.com/r/speechrecognition/comments/16b6kd4/247_speechtotext_transcription_tool_wanted/k5x2n8v/), which sounds fascinating. But it seems that most ear bone mics are designed for military use, and they require a radio system to connect. I'm not sure if there is a consumer-friendly option that offers the same convenience as a standard headset, such as Bluetooth connectivity to a computer or phone.

I've put more than a dozen microphones to the test, and the [Poly Voyager 5200](https://www.poly.com/us/en/products/headsets/voyager/voyager-5200) came out on top. However, it's not without its flaws:

1. **Insufficient Noise Cancellation**: It still picks up some background noise, especially loud announcements.
1. **Excessive Noise Cancellation**: It sometimes cancels out my voice when I'm in a small enclosed space.
1. **Connectivity**: There are occasional connectivity issues.
1. **Battery Life**: It only [lasts for 7 hours](https://www.poly.com/us/en/products/headsets/voyager/voyager-5200#:~:text=Talk%2Fstandby%20time-,up%20to%20seven%20hr).
1. **Charging Port**: It [uses an old Micro USB](https://www.poly.com/us/en/products/headsets/voyager/voyager-5200#2specifications) instead of USB-C.

I'm sure there's a better option out there.

Aside from the microphone hunt, I'm also exploring speaker verification. u/rdesh26 [recommended the pre-trained ECAPA-TDNN model from SpeechBrain](https://old.reddit.com/r/speechrecognition/comments/17j1w4r/speaker_recognition_model/kac6rq1/), which looks promising. However, this isn't a replacement for a high-quality microphone.

I've also created a proof of concept. I have two branches:

- [Main Branch](https://github.com/8ta4/say): You can try this software, but it's very buggy.
- [Develop Branch](https://github.com/8ta4/say/tree/c1df6ef494c9e87886115822d25386cd5b0ea3bf): This branch is my next rewrite and it's not working yet. Your feedback on this branch will help me improve this software.

My hope is that by sharing this early-stage concept, it might spark collaborative improvements. Whether it's refining this tool or exploring a completely new approach, I'd love to team up if you're working on something similar or have insights to share.
