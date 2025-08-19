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

And for most use cases, you'd be right.

But here's the context. The goal is to feed webpage context into an LLM pipeline to automate personalized outreach. That requires programmatic access, which is why I've opted for a CLI. This also explains the other choices: it's a low-frequency task, so the behavioral fingerprint is less of a risk; the extension's scope is just returning the title and `innerText` for the LLM, limiting the security surface; and I already work in VMs with separate browser instances, so it doesn't tie up my machine.

With a scope this narrow, you might not even call it "scraping," and maybe this is the wrong sub.

I've detailed my thought process and the limitations in this write-up: https://github.com/8ta4/see/blob/e1f9b88d171e56cf86b8be44ccd82084b8abb58e/DONTREADME.md

I'm posting to find out if a tool with this architecture already exists. The closest I've found is `single-file-cli`. But it relies on CDP and gets flagged by Cloudflare. I'd much rather use an existing open-source project than reinvent this.

If you know of one, may I have your extension, please?
