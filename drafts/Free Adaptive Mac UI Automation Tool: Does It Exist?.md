Do you know of any tool that can automate the ever-changing UI of a Mac app and doesn't cost a dime?

This question came to me when a user wanted to [automate Apple Maps settings using plist](https://github.com/8ta4/plist/issues/24#issuecomment-1931474720). I thought it was a reasonable request, until I hit a roadblock. The setting they wanted to automate was nowhere to be found in plist, so my tool was useless.

I was tempted to say, "Just use Google Maps." But I knew they'd say, "That's not the answer I need." It's a typical XY problem, so I skipped to Z: "Forget Maps. Just get lost."

But then, it hit me. Maybe I'm the one stuck in the XY problem. I was limited by plist management. I wondered if I could try UI automation instead. Imagine being able to automate any setting, not just for Apple Maps but for any app, without relying on plist files or default commands.

Take, for instance, changing the "Use Large Labels" setting in Apple Maps. A robust tool should be able to adapt to an additional step, a reorganized menu, or even a renamed setting. It should do this without any manual intervention.

This is not just about tweaking settings. Generic AI-driven automation would let the user teach the AI how to do something, and then repeat it a hundred times.

Here are my requirements:

- Adaptability: The tool should be able to handle software whose UI might change over time due to app or Mac OS updates.
- Free: The tool should be free, maybe using a venture capital model where the initial user cost is subsidized, or running locally on my machine.
- Minimal Hardware Requirement: The tool should run smoothly on a recent base model Mac.

I've considered some tools like Automator, Apple Script, SikuliX, Selenium, Puppeteer, and Playright. But they all have the same problem: they break when the UI changes. I need a tool that can adjust to UI updates automatically.

Are there any existing tools that meet these requirements?
