I have the classic developer problem: I'm terrible at getting the word out. I was looking at SaaS options to help with outreach, but they felt like black boxes that one-shot a message. I wanted an explicit process, like a tournament where multiple drafts compete to ensure quality.

Relying on SaaS for this felt like I'd be doing myself a disservice, and that would make me SaaD. So I built [my own system](https://github.com/8ta4/spam) using a self-hosted [Temporal](https://github.com/temporalio/temporal) workflow engine.

A local Temporal server orchestrates the message generation workflow. The [`config.cljs`](https://github.com/8ta4/spam/blob/8319eb00fb03796ea88683492454c45af5dd2aec/src/config.cljs) file lets me define the prompts as code. The workflow reads from and writes to a Google Sheet. It's a compromise.

I'm sure many of us have been there: you have a specific need, you check the market, and nothing quite fits the way you think.

What use case has you so frustrated with existing SaaS options that you've decided to build your self-hosted solution?
