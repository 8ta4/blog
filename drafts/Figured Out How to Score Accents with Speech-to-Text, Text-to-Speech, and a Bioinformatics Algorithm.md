I've stumbled upon a method for evaluating pronunciation, and I'm excited to share it with you. This method gives you a word-by-word breakdown of understandability against a target accent. I'd love to hear what you think about this approach!

1. Use a speech-to-text API to turn the user's speech into text, complete with word-level probabilities.

2. Use a text-to-speech API to whip up a reference pronunciation of that transcribed text.

3. Use the speech-to-text API again to transcribe this generated reference speech, getting another transcript with word-level probabilities.

4. Apply the Needleman-Wunsch algorithm to align the two transcripts.

5. Check out the differences in word probabilities to spot where your pronunciation might be tricky for listeners of the target accent.

If you've got a Mac, you can give it a whirl.

While working on this, I told a friend I was looking for a speech pathologist to consult. He said, "Oh, you want to get your tongue checked?" I said, "No, but you might want to get your brain checked. It could be empty."

I haven't managed to corner a speech expert yet. That's where you guys come in! I'd love to hear your thoughts if you've got some language expertise. Even if you don't, your feedback is gold. I'm terrible at checking DMs, so if you have questions or feedback, drop them here in the thread.
