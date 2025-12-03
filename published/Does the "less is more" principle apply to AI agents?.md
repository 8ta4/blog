I'm sketching out an idea for a project. I'm wrestling with this idea: whether "less is more" applies to AI agents.

You see all these demos with agents that can browse the web, use tools, call functions, and all that. But my gut reaction is that it's all function and games until an agent decides to call some tool it doesn't need, poisons its context with irrelevant info, and makes the final output worse.

This is making me lean into constraining the agents for my project. I'm documenting my thinking [here](https://github.com/8ta4/spam/blob/68dec24c6096a4c2b4070131827e10f65f6ed09e/DONTREADME.md):

- They don't search the web.

- They don't call functions to get more data.

- Each agent has just one job, so a `judge` agent only judges and doesn't edit.

I feel like this will make the whole system more predictable.

But then I can't shake the feeling that this is a shortsighted move. I worry I'm building something that's going to be obsolete the moment a smarter model drops.

With how fast everything is moving, is this constrained approach a form of premature optimization?
