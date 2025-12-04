I wanted to use Temporal with Clojure.

The community Clojure SDK was the obvious choice. But a requirement forced me to use the `google-spreadsheet` Node.js library. Thinking outside the box, I looked into using GraalVM to run the Clojure SDK and call the Node library from there, but Temporal doesn't officially support GraalVM.

This left one option: ClojureScript and the official TypeScript SDK.

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

The code for this setup is public.

I hope this saves someone else the headache of figuring this out from scratch.
