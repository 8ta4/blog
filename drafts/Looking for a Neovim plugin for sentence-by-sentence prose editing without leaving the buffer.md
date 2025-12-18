I spend a lot of time in the refinement phase of my writing. I'm frustrated by the inefficiency of writing assistants, which force disruptions like copy-pasting, using a mouse, or shifting focus between windows.

I get my initial drafts using my [transcription system](). The hard work starts next: going through every single sentence until I'm confident I've made it as good as I reasonably can. You might wonder why this post is bad. You didn't see the first draft.

Voice input becomes inefficient for precise edits. Any web-based solution is out because it pulls me out of Neovim. Plugins like [`avante.nvim`]() are focused on code editing. [`dante.nvim`]() seems to offer only a single rephrasing option.

I've come up with my ideal requirements:

- The workflow is a loop: I edit the sentence in place, use the command to get LLM feedback, edit the sentence again, and use the command again to critique the new revision.

- I use the same key to ask for suggestions, refresh them, or close the panel.

- The LLM checks against my rules and provides multiple alternative rephrasings.

- Suggestions appear in a panel at the bottom of the screen. I can select a suggested option without moving my cursor to that panel.

- The plugin highlights reviewed sentences to track my progress, even after closing and reopening the file.

If you know of a plugin that achieves most of these requirements, I'd love to try it out.

Does a plugin with this workflow exist?
