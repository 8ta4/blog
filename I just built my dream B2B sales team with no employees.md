u/sirlifehacker posted a similar title. The top comment from u/loztb nailed the skepticism:

> A ChatGPT-written salespitch for tech that doesn't exist, and the suckers are already begging for DM's.

You do not need to DM me for the code because it's on GitHub.

I hate writing text so much that I built a system to automate it. Naturally, I'm too lazy to write a Reddit post, so I copy-pasted u/sirlifehacker's format to present it.

I hired a sales team.

Except, instead of hiring humans, I used code.

Here is the breakdown.

**Phase 1: Building My Sales Research Team**

First, I needed context. I built a scraping tool in Haskell that communicates with a ClojureScript browser extension. It uses my browser session to retrieve page content, which makes it more reliable than anonymous bots.

**Phase 2: CRM Integration & Outreach Generation**

Leads go into my CRM, which is Google Sheets, because who needs SalesFarce? My outreach tool feeds unstructured data to the LLM.

From there, a Temporal server runs a tournament between multiple agents. They refine the draft until the quality plateaus, and the result is written back to the sheet.

I'm happy to answer any questions in the comments.
