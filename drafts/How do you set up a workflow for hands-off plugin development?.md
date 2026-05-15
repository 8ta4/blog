My last plugin was a pain. I began with Fennel but ended up [switching over to ClojureScript](https://old.reddit.com/r/Clojure/comments/1swrj3t/why_i_rewrote_my_neovim_plugin_from_fennel_to). The remote plugin's async model kept fighting me.

u/velrok7 [suggested](https://old.reddit.com/r/neovim/comments/1pq47fc/looking_for_a_neovim_plugin_for/nuu69r9) using an LLM to build a plugin. Claude 4.7 Opus or Gemini 3.1 Pro as pair programmers hasn't worked out for me. I find myself micromanaging them. So for this next plugin, I want to treat the agent as an abstraction layer and just let it play fast and Lua.

Does anyone have a solid setup for this kind of automated development?

I'm particularly interested in suggestions on how to:

- Set up a feedback loop that allows an agent to jump into a Neovim instance to test its own code.

- Provide an agent with access to Neovim documentation.

- Determine the right depth for an initial specification.

I've laid out the project details here.
