I'm here to personally assist you in automating your Chrome extension installation and configuration. If your configuration is hosted online, I can even contribute some pull requests for you.

I've developed a new tool called [extension](https://github.com/8ta4/extension). This handy tool automates the installation and configuration of Chrome extensions on macOS.

You might wonder, "Why this tool?" Chrome has a decent built-in syncing option, and its extension update mechanism is so smooth that you'll hardly notice it (even when it's stealing your data! 😅). But I believe in striving for more than just "good enough". I wanted to do better, to have more control over my extensions. That's why I developed `extension`.

For example, if you use the [Video Speed Controller](https://chrome.google.com/webstore/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk) extension on Chrome and want to automate its setup, you can use this command:

```sh
extension install chrome nffaoalbilbmmfgbnbgppjihopabppdk config.js
```

The `config.js` file can contain JavaScript code to enable specific features:

```javascript
chrome.storage.sync.set({ audioBoolean: true });
```

Don't worry if you're not comfortable with JavaScript. `extension` has a listen mode that generates the code for you.

Share your extension list with me, and I'll help create an installation script. If you provide a screenshot of your extension settings, I can help create a configuration script too.
