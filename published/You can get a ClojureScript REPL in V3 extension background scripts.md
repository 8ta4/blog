I made a post about [Why I Use Firefox to Develop Chrome Extensions with ClojureScript](https://old.reddit.com/r/Clojure/comments/1frtvyz/why_i_use_firefox_to_develop_chrome_extensions/). In that post, I talked about how I was using Firefox to get around Chrome's Manifest V3 restrictions for REPL-driven development.

But I said one thing in that post that was plain wrong:

> [REPL: The REPL works fine in content scripts, but it's a no-go in background scripts.](https://old.reddit.com/r/Clojure/comments/1frtvyz/why_i_use_firefox_to_develop_chrome_extensions/#:~:text=REPL%3A%20The%20REPL%20works%20fine%20in%20content%20scripts%2C%20but%20it%27s%20a%20no%2Dgo%20in%20background%20scripts.)

You can get a ClojureScript REPL running in the background script.

The solution is [one line](https://github.com/8ta4/see/blob/81137f1139d5451cc3a2699f5bf05c804a176860/cljs/shadow-cljs.edn#L12) in your `shadow-cljs.edn` for your background script:

```clojure
:devtools {:use-document-host false}
```

I put a working example up in [my new project repo](https://github.com/8ta4/see).

Hopefully, this helps get a few more people building extensions with ClojureScript. And who knows, maybe this is finally the Year of Firefox. That would be the REPL effect.
