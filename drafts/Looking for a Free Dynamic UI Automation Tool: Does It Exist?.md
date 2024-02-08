Do you know of any tool that can automate the UI interaction of an app that changes frequently and also costs nothing?

This question popped into my head when I was messing with Apple Maps. [Someone wanted](https://github.com/8ta4/plist/issues/24#issuecomment-1931474720) to automate Apple Maps settings using plist. I thought, "Why bother? Just use Google Maps." But I knew they would say, "That's not the answer I need." It's a typical XY problem, so I skipped to Z: "Forget Maps. Just get lost."

That made me think more about the limitations of plist management. It made me wonder if I could try UI automation instead. Imagine being able to automate any setting, not just for Apple Maps but for any app, without relying on plist files or default commands.

This is not just about tweaking settings. Generic AI-driven automation would let the user teach the AI how to do something, and then repeat it a hundred times.

Here are my requirements:

- Adaptation: The tool should be able to interact with software whose UI might change over time due to app or OS updates.
- Zero Cost: The tool should be either free, using maybe a venture capital model where the initial user cost is subsidized, or, if the tool runs locally, it should work on a recent Mac's base model.

I've considered some tools like Automator, Apple Script, SikuliX, Selenium, Puppeteer, and Playright. But they all have the same flaw: they can't cope with minor UI changes. I need a tool that can react to UI updates automatically.

Are there any existing tools that meet these requirements?
