My last plugin was a pain. I began with Fennel but ended up switching over to ClojureScript. Dealing with the friction between the remote plugin's async model and REPL glitches was exhausting.

u/velrok7 suggested I try using an LLM to build a plugin. Using models like Claude 4.7 Opus or Gemini 3.1 Pro as pair programmers hasn't worked out for me yet. I find myself micromanaging them. So for this next plugin, I want to treat the agent as an abstraction layer and just let it play fast and Lua.

Does anyone have a solid setup for this kind of automated development?

I'm particularly interested in suggestions on how to:

- Set up a feedback loop that allows an agent to jump into a Neovim instance to test its own code.

- Provide an agent with access to Neovim documentation.

- Determine the right depth for an initial specification.

I've laid out the project details here.
