We built [this command-line tool](https://github.com/8ta4/extension) to install and configure extensions automatically. The tool used Playwright and the Chrome DevTools Protocol (CDP) connection to do its job. It was handy for setting up new environments.

Then a Chrome 136 update killed that connection. It looks like Google [disabled connecting over CDP for the default Chrome data directory](https://developer.chrome.com/blog/remote-debugging-port), which seems to be part of the same update that was messing with u/ppp258 in [this thread](https://old.reddit.com/r/Playwright/comments/1kce8t3/chrome_136_broke_playwright/) the other day.

I almost gave up on the tool.

My friend said, "Why not switch browsers if Chrome keeps breaking your stuff?"

I said, "Because there's no place like Chrome."

I managed to find a partial fix. I [took out the code that used the CDP connection](https://github.com/8ta4/extension/blob/a5140b48494443a63189761f6cdfb0266ee2b27b/src/Extension.purs#L27-L67). Now the tool just [copies the extension files into the profile directory](https://github.com/8ta4/extension/blob/a5140b48494443a63189761f6cdfb0266ee2b27b/src/Extension.purs#L69-L86). This gets the extension installed, sort of. But the extension starts disabled. It's not the ideal solution.

Has anyone found a better way to manage or configure extensions programmatically?

I'm open to any suggestions or collaboration. Please let me know if you figured something out.
