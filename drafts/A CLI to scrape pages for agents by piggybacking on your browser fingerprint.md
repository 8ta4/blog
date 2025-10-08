I keep hitting a wall with bot detection when trying to get live web data for agents.

So I built [a CLI](https://github.com/8ta4/see) that tells a companion extension to fetch a page. The whole idea was to control my day-to-day browser to piggyback on its static fingerprint.

This isn't for serious scraping. Forget residential proxies or Clay. I designed this for developers who are just scraping by.

My ideal outcome is for someone to point me to an existing open-source project that does this better, so I can abandon this. If nothing better exists, maybe this solution is useful to someone else facing the same problem.

The tool is limited, by design.

- It doesn't scale. It's built for grabbing one page at a time.

- It's dumb. It just gets the `innerText`.

- The behavioral fingerprint is sterile. It doesn't fake any mouse or keyboard activity.

Is a tool that just grabs text about to be subsumed by agents that can interact with pages?
