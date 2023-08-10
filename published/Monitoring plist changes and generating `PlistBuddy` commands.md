I am looking for a tool or method to monitor plist changes on my Mac and generate the corresponding `PlistBuddy` commands when preferences are changed in macOS or apps. I want to avoid using `defaults write` since some preference values are nested. (Plists are like onions, they have layers upon layers, and just when you think you've peeled them all, another one appears to make you cry.)

I've found these repositories, but they don't exactly do what I want:

- [macos-defaults](https://github.com/yannbertrand/macos-defaults#how-to-discover-a-defaults-command)
- [plistwatch](https://github.com/catilac/plistwatch)

My ideal workflow is as follows:

1. Start the monitoring tool.
2. Change preferences in macOS or apps.
3. The tool shows `PlistBuddy` commands.
4. Copy and paste the commands into my setup script.

This would be similar to how [Karabiner-EventViewer](https://karabiner-elements.pqrs.org/docs/manual/operation/eventviewer/) works for a different problem.

Any suggestions on how to achieve this or existing tools that can help me with this workflow?
