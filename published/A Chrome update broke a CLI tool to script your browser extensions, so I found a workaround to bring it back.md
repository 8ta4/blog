I've been working on [extension](https://github.com/8ta4/extension), a command-line tool to make your browser extension setup as scriptable as your dotfiles. It lets you install and configure extensions for Chrome, Edge, and Arc from the terminal.

[A Chrome update](https://developer.chrome.com/blog/remote-debugging-port) broke it. The update killed the Chrome DevTools Protocol connection.

My first thought was to change the debugging port. I figured any port in a storm would do. But that did nothing.

The actual workaround was to wrap our original process by copying the user data directory to a temporary location, running the configuration on that copy, and then moving it back to replace the original.

This copy-and-replace method feels more complex and fragile than the original. But it gets the job done.

The tool is for macOS only. The source code is available on GitHub. If you've ever wanted to script your browser setup, I'd love for you to check it out.

Has anyone else here had a platform update break one of your favorite Mac apps?
