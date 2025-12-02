The part of building a business I dread most is sales outreach. It's a repetitive grind that can take the wind out of your sales.

So I built a CLI tool to automate it.

You point it at a Google Sheet of contacts, run one command, and get personalized drafts written back into the sheet.

The main challenge is getting context, especially from social media platforms that block access from most LLMs. My tool gets around that by using your browser to pull data from the URLs you give it.

Once it has that context, it runs a tournament where different AI agents rewrite and critique the message in a loop. The goal is to refine the draft until the quality plateaus.

The code is on GitHub. I'd love to get feedback from other devs.
