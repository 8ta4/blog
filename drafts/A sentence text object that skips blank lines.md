I posted here a while back asking if there was a sentence text object that didn't stop at blank lines. Who needs to read between the lines?

u/Biggybi told me, "[[Y]ou can write your own. It's not too complex.](https://old.reddit.com/r/neovim/comments/1qim6dt/is_there_a_sentence_text_object_that_doesnt_stop/o0vae02)" So I went ahead and built it.

Here is what the tool solves:

- Bypasses dead space: The `)` and `(` motions skip over blank lines.

- `is` selection from gaps: When the cursor is on a blank line, the `is` text object selects the next available sentence instead of doing nothing.

- Prose-aware boundaries: The plugin knows that abbreviations like `Mr.`, `Dr.`, `Mrs.`, `Ms.` and numbered list markers like `1.` or `2.` don't mark the end of a sentence.

- Lua API: `sentence.get` returns the row and column coordinates of a sentence.

Check it out [here](https://github.com/8ta4/sentence).

I built this with ClojureScript because I didn't want to write the logic in Lua or Fennel. If someone writes a similar plugin in pure Lua, I'd be happy to try it.
