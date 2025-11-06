I made a post about Why I Use Firefox to Develop Chrome Extensions with ClojureScript. In that post, I talked about how I was using Firefox to get around Chrome's Manifest V3 restrictions for REPL-driven development.

But I said one thing in that post that was plain wrong:

> REPL: The REPL works fine in content scripts, but it's a no-go in background scripts.

You can get a ClojureScript REPL running in the background script.

The solution is one line in your `shadow-cljs.edn` for your background script:

```clojure
:devtools {:use-document-host false}
```

I put a working example up in my new project repo.

Hopefully this helps get a few more people building extensions with ClojureScript. And who knows, maybe this is finally the Year of Firefox. That would be the REPL effect.
