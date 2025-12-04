I have the classic developer problem: I'm terrible at getting the word out. I was looking at SaaS options to help with outreach, but they felt like black boxes that one-shot a message. I wanted an explicit process, like a tournament where multiple drafts compete to ensure quality.

Relying on SaaS for this felt like I'd be doing myself a disservice, and that would make me SaaD. So I built [my own system](https://github.com/8ta4/spam) using a self-hosted [Temporal](https://github.com/temporalio/temporal) workflow engine.

A local Temporal server orchestrates the message generation workflow. The `config.cljs` file lets me define the prompts as code. The workflow reads from and writes to a Google Sheet. It's a compromise.

I'm curious if anyone else is using workflow engines like Temporal in a self-hosted capacity. What has your experience been?
