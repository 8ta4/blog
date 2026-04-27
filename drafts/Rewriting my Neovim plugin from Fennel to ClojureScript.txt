I built [a Neovim plugin](https://github.com/8ta4/sentence) that provides text motions designed for prose. My goal was to bypass blank lines and handle punctuation edge cases. Because it's Neovim, the default Lisp path is Fennel. I started there, but rewrote it as a ClojureScript Node.js remote plugin using [`shadow-cljs`](https://github.com/thheller/shadow-cljs).

To be fair, Fennel has upsides:

- There's almost zero ceremony between Fennel and Lua.

- You avoid the async overhead of remote plugins.

But the friction started with the standard library. I was using [`nfnl`](https://github.com/Olical/nfnl), which comes with [its own Clojure-inspired functions](https://github.com/Olical/nfnl/tree/837daee35e5b3eaffba0153b9a73716a2135dc06/docs/api/nfnl). The problem is they are not comprehensive enough. I found myself manually implementing things like [`difference`](https://github.com/8ta4/sentence/blob/747d088a5b17b2d6af2891a1601cb92d2770507c/fnl/core.fnl#L28-L29) just to process text bounds. Since Fennel's [`fn`](https://fennel-lang.org/reference#fn-function) doesn't support multi-arity functions [the way Clojure does](https://clojure.org/guides/learn/functions#_multi_arity_functions), I decided to write some macros to implement it myself. Naturally, this devolved into yak shaving. The dealbreaker hit when I ran into [a bug](https://github.com/Olical/conjure/issues/728) in [Conjure](https://github.com/olical/conjure). When the REPL failed on the macros I was trying to build just to make the language usable, that was the straw that broke the yak's back.

So I switched to a ClojureScript remote plugin. But I traded the macro REPL issues of Fennel for a different kind of REPL headache in ClojureScript.

Specifically, I'm having a bizarre issue where [`println`](https://clojuredocs.org/clojure.core/println) fails inside my async code. It feels nondeterministic. Sometimes the output prints perfectly fine. But other times, `println` disappears into the void. To see the value, I resort to a hack: I create a fake atom and [`reset!`](https://clojuredocs.org/clojure.core/reset!) the value into it. That works. But if I try to [add a watch](https://clojuredocs.org/clojure.core/add-watch) to that fake atom to print the updated value, that doesn't print either!

Does anyone have any idea why `println` is getting swallowed in this async Neovim context?

If anyone has any other feedback, I'd be happy to hear it.
