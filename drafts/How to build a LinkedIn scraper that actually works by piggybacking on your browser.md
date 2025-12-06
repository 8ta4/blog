u/itsalidoe's post laid out a checklist for building scrapers.

Here's the setup I've been using: a CLI that controls my daily browser through a companion extension. Let's see how it stacks up against the original rules.

> avoid headless browsers.

This setup uses my daily browser. So it's not headless. It also sidesteps automation frameworks like Playwright, which helps minimize the signals bot detectors look for.

> slow things down.

Since it's a CLI, I can add sleep calls between scrapes to control the pace. The extension itself adds human-like delays by waiting for the page to visually stabilize and closing the tab on a timer modeled after statistical browsing patterns.

> act human.

This approach avoids faking clicks. Bot detectors can check the `event.isTrusted` property, which is `false` for synthetic clicks.

> rotate proxies often.

The extension uses the browser's network. So if I need a proxy, I set it up in the browser.

> set realistic user-agents.

The extension uses the same user agent and headers I use for my daily browsing.

> parse data carefully.

This approach sidesteps parsing the DOM. The extension grabs `innerText`. Then, an LLM extracts the data. Feeding an LLM the full DOM burns tokens. You can't see the text for the trees.

The code for the CLI using this approach is on GitHub. Let me know what you think in the comments.
