I'm exploring a scraping idea that sacrifices scalability to leverage my day-to-day browser's fingerprint.

My working hypothesis for this niche is to skip automation frameworks entirely. The architecture connects two parts:

- A CLI tool on my local machine.

- A companion browser extension running in my day-to-day browser.

They communicate using Chrome's native messaging.

Now, I can already hear the objections:

- "Why not just use Playwright Stealth?"

- "Why not CDP?"

- "This will never scale!"

- "This is a huge security risk!"

- "The behavioral fingerprint will be your giveaway!"

And for most use cases, you'd be 100% right.

But here's the context for the trade-offs I'm willing to make. This is for low-frequency, low-volume tasks. The bet is that the natural browser fingerprint is enough to fly under the radar when requests are sparse. The extension's job is just returning the page title and innerText, not running arbitrary logic. I also work within VMs and use separate Chrome instances for different tasks, so my primary work isn't tied up.

With a scope this narrow, you might not even call it "scraping," and maybe this is the wrong sub.

I've detailed my thought process and the limitations in this write-up: https://github.com/8ta4/see/blob/e1f9b88d171e56cf86b8be44ccd82084b8abb58e/DONTREADME.md

I'm posting to find out if a tool with this architecture already exists. The closest I've found is `single-file-cli`. But it relies on CDP and gets flagged by Cloudflare. I'd much rather use an existing open-source project than reinvent this.

If you know of one, may I have your extension, please?
