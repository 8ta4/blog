I'm working on a project that allows you to install, configure, and detect changes in Chrome extensions programmatically. I'm using Playwright and the `chrome.*` API for extension management.

I'm looking for feedback. I even asked ChatGPT. It said, "Use your brain, you `{headless: true}`."

I haven't started coding yet, but you can see my progress on [GitHub](https://github.com/8ta4/extension).

Here's how it works:

1. To install an extension, it creates a preferences file and uses Playwright to enable the extension with the `chrome.management.setEnabled` method.
2. To configure an extension, it uses Playwright to set the configuration values with the `chrome.storage.sync.set` method and other methods as needed.
3. To detect changes in an extension, it uses Playwright to get the extension ID with the `chrome.management.getAll` method. Then, it uses Playwright to listen for changes with the `chrome.storage.sync.addListener` method and other methods as needed, generating JavaScript code based on the changes. Finally, it uses WebSocket to send the generated code to a logger.
