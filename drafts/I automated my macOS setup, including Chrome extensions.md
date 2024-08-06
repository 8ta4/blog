Setting up a new Mac can be a real hassle. I put together [this script](https://github.com/8ta4/chezmoi/blob/60ab9d48c328362f72d6cd79bac0b1fa35a23eaa/install.sh) that does a bunch of stuff for me. Here's the gist:

- Homebrew: I've got a [Brewfile](https://github.com/8ta4/chezmoi/blob/60ab9d48c328362f72d6cd79bac0b1fa35a23eaa/Brewfile) that lists all the apps I install using Homebrew. They say there's an app for everything. If you need to research, there's an app for that. If you need to recharge, there's a nap for that!

- Chrome: I have [a file](https://github.com/8ta4/chezmoi/blob/60ab9d48c328362f72d6cd79bac0b1fa35a23eaa/extension.sh) that lists all my favorite Chrome extensions, and I've developed [a custom tool](https://github.com/8ta4/extension) that automatically installs and configures them for me.

- Visual Studio Code: I've also got [a separate file](https://github.com/8ta4/chezmoi/blob/60ab9d48c328362f72d6cd79bac0b1fa35a23eaa/code.sh) that lists all the Visual Studio Code extensions I use.

- PlistBuddy: For most macOS customizations, I use PlistBuddy. I have [a file](https://github.com/8ta4/chezmoi/blob/60ab9d48c328362f72d6cd79bac0b1fa35a23eaa/preferences.sh) that contains all the PlistBuddy commands needed for my customizations. I also created [a monitoring tool](https://github.com/8ta4/plist). When I adjust settings via the GUI, this tool generates the exact PlistBuddy commands that match those changes.

If you're interested, feel free to check out [my repository](https://github.com/8ta4/chezmoi) and use whatever you find useful.

I attempt to [livestream every single code commit I make on my open-source projects](https://www.youtube.com/@8ta4/streams). So if you're curious, you can actually see this whole setup in action!

How do you set up your Mac? I’d love to hear your thoughts!
