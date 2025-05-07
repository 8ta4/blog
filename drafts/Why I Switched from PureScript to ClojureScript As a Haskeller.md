Blame the Foreign Friction Interface (FFI).

Imagine a chain: PureScript calls JavaScript, which calls PureScript, which calls JavaScript... Not only do these PureScript and JavaScript functions live in separate files, but the JavaScript function's implementation and its FFI type signature also live in separate files! There's a special place in callback hell for PureScript.

I chose PureScript to avoid writing JavaScript, but then the FFI had me writing JavaScript anyway!

If JavaScript wasn't in the picture, I'd enjoy PureScript. But if JavaScript wasn't in the picture, I'd just reach for Haskell.

But this tool is designed to install and configure Chrome extensions programmatically. Playwright permeates the core logic. For this, the ease of interop in ClojureScript wins out for me.

You can see the PureScript version here and the ongoing ClojureScript rewrite here though it's nowhere near feature parity yet.

What does your ideal interop experience look like?

Let me know your thoughts!
