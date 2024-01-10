## Proposed changes

I want to make the connection last longer when using the prerecorded API and a readable stream.

## Context

I'm building an open-source project called [`say`](https://github.com/8ta4/say). It transcribes voice 24/7.

I want to cut down the latency as much as possible, but keep the accuracy of the prerecorded API.

I tried using a readable stream to send audio data with Deepgram's Node SDK. I thought it would keep the connection open as more audio gets recorded. But it doesn't work.

I told my partner about this. I said, "It won't listen for more than a few seconds!" She said, "That's just you." I said, "Huh? Sorry, I wasn't listening."

## Other information

You can check out the full discussion [here](https://github.com/orgs/deepgram/discussions/518).
