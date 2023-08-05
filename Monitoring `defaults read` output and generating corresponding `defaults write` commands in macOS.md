I want to monitor the output of `defaults read` to detect changes in the preferences of macOS and apps without user interaction, and then show the corresponding `defaults write` commands that would have the same effect. I would like to improve my workflow for declaratively configuring my settings, as follows:

1. Start the monitoring tool.
2. Change preferences in macOS or apps.
3. The tool shows `defaults write` commands.
4. Copy and paste the commands into my setup script.
I found a script that could be used as a starting point: [macos-defaults](https://github.com/yannbertrand/macos-defaults#how-to-discover-a-defaults-command). However, it doesn't exactly do what I want as it prompts for pressing a key and doesn't show defaults write commands.

My ideal tool would be analogous to [Karabiner-EventViewer](https://karabiner-elements.pqrs.org/docs/manual/operation/eventviewer/), which solves a different problem but in a similar manner.

How can I create a macOS monitoring tool that detects preference changes and generates the appropriate defaults write commands? Any guidance, libraries, or existing solutions that could help me achieve this would be greatly appreciated.

By the way, `defaults read`? More like `defaults dread`, am I right?
