I wanted to use [Temporal](https://github.com/temporalio/temporal) with Clojure.

[The community Clojure SDK](https://github.com/manetu/temporal-clojure-sdk) was the obvious choice. But a requirement forced me to use the [`google-spreadsheet`](https://github.com/theoephraim/node-google-spreadsheet) Node.js library. Thinking outside the box, I looked into using GraalVM to run the Clojure SDK and call the Node library from there, but [Temporal doesn't officially support GraalVM](https://community.temporal.io/t/support-for-graalvm/9159/5#:~:text=I%20am%20afraid%20we%20don%E2%80%99t%20have%20official%20support%20for%20GraalVM%20at%20the%20moment.).

This left one option: ClojureScript and [the official TypeScript SDK](https://docs.temporal.io/develop/typescript).

There appeared to be no prior art for this combination. Using a development build from shadow-cljs resulted in critical dependency warnings, making the workflows incompatible with Temporal's sandbox.

Then I tried `shadow-cljs release`.

It worked.

Development builds from shadow-cljs inject `fs`, `path`, and `vm` modules, but the release build omits them. These modules violate Temporal's sandbox rules. The experience taught me a lesson: it's all about thinking inside the sandbox.

This solution comes with some costs:

- You lose the REPL for workflow development.

- Every activity call is asynchronous.

- Data conversion between ClojureScript and JavaScript is a pain.

I made this setup workable with a couple of strategies:

- I kept workflows minimal and moved logic into activities. Since activities are not sandboxed, I could use a REPL-driven process for them.

- I used `promesa` to make the asynchronous orchestration of activities cleaner.

[The code](https://github.com/8ta4/spam/tree/8319eb00fb03796ea88683492454c45af5dd2aec) for this setup is public.

I hope this saves someone else the headache of figuring this out from scratch.
