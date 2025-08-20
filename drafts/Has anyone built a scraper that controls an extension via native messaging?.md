I'm exploring a scraping idea that sacrifices scalability to leverage my day-to-day browser's fingerprint.

My working hypothesis for this niche is to skip automation frameworks entirely. The architecture connects two parts:

- A CLI tool on my local machine.

- A companion browser extension running in my day-to-day browser.

They communicate using Chrome's native messaging.

Now, I can already hear the objections:

- "Why not just use Playwright?"

- "Why not CDP?"

- "This will never scale!"

- "This is a huge security risk!"

- "The behavioral fingerprint will be your giveaway!"

And for most use cases, you'd be right.

But here's the context. The goal is to feed webpage context into the LLM pipeline I described in [a previous post](https://old.reddit.com/r/SaaS/comments/1msku4e/seeking_a_tool_to_automate_my_10_reply_rate) to automate personalized outreach. That requires programmatic access, which is why I've opted for a CLI. It's a low-frequency task. The extension's scope is just returning the title and `innerText` for the LLM. I already work in VMs with separate browser instances.

With a scope this narrow, you might not even call it "scraping," and maybe this is the wrong sub.

I've detailed my thought process and the limitations in [this write-up](https://github.com/8ta4/see/blob/853eb1c28936ba59c2837aaf07b07ccc6c836655/DONTREADME.md).

I'm posting to find out if a tool with this architecture already exists. The closest I've found is [`single-file-cli`](https://github.com/gildas-lormeau/single-file-cli). But it relies on CDP and gets flagged by Cloudflare. I'd much rather use an existing open-source project than reinvent this.

If you know of one, may I have your extension, please?
