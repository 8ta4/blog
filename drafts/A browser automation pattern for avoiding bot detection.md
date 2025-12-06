Browser automation feels like an arms race. A framework like Playwright can leave a fingerprint that bot detectors are built to catch. So I started playing with a different approach: controlling your day-to-day browser.

[What I built](https://github.com/8ta4/see) is a CLI that talks to a browser extension. It uses my browser's fingerprint. The goal is a clean bill of stealth.

But this approach has its downsides.

- It relies on a companion extension, which adds setup friction. I yak-shaved [a tool](https://github.com/8ta4/extension) to automate installing extensions, so this is a solvable problem.

- It's not built to run at a massive scale. You could spin up a bunch of browsers, but that's not a feature out of the box.

- It lacks the interactivity of other frameworks. As u/Chromix_ pointed out in [another post](https://old.reddit.com/r/LocalLLaMA/comments/1o1u9ia/a_cli_to_scrape_pages_for_agents_by_piggybacking), not moving the mouse or typing could look suspicious. If you want to add that stuff, you have to change the extension's code yourself. That said, it hasn't been a problem in small-scale use so far.

- A script gets access to your logged-in browser. That comes with a whole different set of risks, especially if you hook an LLM up to it.

I put my thinking on this stuff into [a brain dump](https://github.com/8ta4/see/blob/81137f1139d5451cc3a2699f5bf05c804a176860/DONTREADME.md).

What other approaches have you found effective for stealthy browser automation?
