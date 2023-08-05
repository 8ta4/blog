I am seeking a tool or method to monitor plist changes on macOS and generate the corresponding `PlistBuddy` commands when preferences are changed in the system or within applications. I have decided to use `PlistBuddy` instead of `defaults write` because it handles nested preference values more effectively (Plists are like onions, they have layers upon layers, and just when you think you've peeled them all, another one appears to make you cry.).

I found these repositories, but they don't quite meet my requirements:

- [macos-defaults](https://github.com/kevinSuttle/macos-defaults)
- [plistwatch](https://github.com/catilac/plistwatch)


My ideal workflow:

1. Start the monitoring tool.
2. Change preferences in macOS or applications.
3. The tool displays `PlistBuddy` commands.
4. Copy and paste the commands into my setup script.

This is similar to how [Karabiner-EventViewer](https://karabiner-elements.pqrs.org/docs/manual/misc/configuration-file-path/) works for a different problem.

Do you have any suggestions for achieving this workflow or know of existing tools that can assist me with this task?

I've already posted a related question on [Stack Overflow](https://stackoverflow.com/questions/76207155/monitoring-defaults-read-output-and-generating-corresponding-defaults-write) but decided to switch to using `PlistBuddy` instead of `defaults write`.

[Discovering macOS Settings with PlistWatch](https://developer.okta.com/blog/2021/07/19/discover-macos-settings-with-plistwatch) provides information on the `plistwatch` tool, which monitors plist files for changes and displays the executed `defaults` commands. However, I am looking for a solution that generates `PlistBuddy` commands instead.
