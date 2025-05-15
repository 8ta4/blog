Blame the Foreign Friction Interface (FFI).

Imagine a chain: PureScript calls JavaScript, which calls PureScript, which calls JavaScript... Not only do these PureScript and JavaScript functions live in separate files, but the JavaScript functions' implementations and their FFI type signatures also live in separate files! There's a special place in callback hell for PureScript.

I chose PureScript to avoid writing JavaScript, but then the FFI had me writing JavaScript anyway!

If JavaScript weren't in the picture, I'd enjoy PureScript. But if JavaScript weren't in the picture, I'd reach for Haskell.

But [this tool](https://github.com/8ta4/extension) is designed to install and configure Chrome extensions programmatically. Playwright permeates the core logic. For this, the ease of interop in ClojureScript wins out for me.

You can see [the PureScript version](https://github.com/8ta4/extension/tree/a5140b48494443a63189761f6cdfb0266ee2b27b) and [the ongoing ClojureScript rewrite](https://github.com/8ta4/extension/tree/adf06f1f090e264daa0f2242b301671a3acafca8) though it's nowhere near feature parity yet.

What does your ideal interop experience look like?

Let me know your thoughts!
