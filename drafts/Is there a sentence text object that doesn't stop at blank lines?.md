I've hit a wall with Neovim's sentence text object.

I checked out [`vim-textobj-sentence`](https://github.com/preservim/vim-textobj-sentence). While it's great for stuff like `Mr.` and `Dr.`, it shares the same flaws as the defaults::

- When I'm trying to jump between sentences with `(` or `)`, it keeps stopping at empty lines.

- Using `is` or `as` on a blank line is where all hell breaks Lua. The result changes depending on factors like how many blank lines are in a row or if they contain any whitespace. It might select the single empty line, a block of them, or even grab the last character of the previous sentence.

- It thinks a `1.` in a Markdown list is the end of a sentence.

- There's no clean Lua function to get the sentence boundaries.

So, I wanted to ask if a plugin exists that works like the following specification.

First off, it'd have to treat any line with just whitespace as a gap:

- Jumping with `(` and `)` should skip over those gaps.

- Trying to select a sentence with `is` or `as` inside a gap should do nothing.

Also, the sentence detection needs to be a bit smarter:

- It shouldn't get confused by numeric list markers like `1. ` or `2. `.

- It should know that common abbreviations like `Mr.`, `Dr.`, `Mrs.`, and `Ms.` aren't the end of a sentence.

And it needs a Lua API so my other plugin can use it. I'm thinking of a function, something like `get({opts})`, that returns the start and end coordinates of a sentence. The behavior would depend on the offset:

- If `offset` is `0`, it'd check the current spot. If the cursor's in a gap, it'd return `nil`.

- If `offset` is something else (like `1` or `-1`), it'd find the next or previous sentence, only returning `nil` if it goes off the edge of the file.

The `opts` table for this function would look something like this:

- `bufnr` (number): The buffer to search in. Defaults to the current one.

- `pos` (table): The `{row, col}` position to start from. Defaults to the cursor.

- `offset` (integer): `0` for the current sentence, `1` for the next, `-1` for the previous, etc. Defaults to `0`.

So, does anything like this exist out there?

If not, it looks like I've got a project to work on. Thanks for any pointers.
