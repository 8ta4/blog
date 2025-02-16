You've heard this advice: [Split complex tasks into simpler subtasks](https://platform.openai.com/docs/guides/prompt-engineering#split-complex-tasks-into-simpler-subtasks).

This made sense when I started working with joke generation last year.

But the game has changed. With reasoning models, I'm finding that sometimes breaking down a task actually gets in the way. My approach to joke generation has evolved. You can see this evolution from [my prompt before reasoning models](https://github.com/8ta4/gag/blob/1f28bb9d2a1a5f45d838637e52e68f2dba6d1b39/README.md?plain=1#L11-L41) to [my prompt now](https://github.com/8ta4/gag/blob/25017ec6a95c2764d1a35d6e2063c5addf6f4e5b/README.md?plain=1#L11-L56).

I've started thinking about this in terms of horizontal versus vertical breakdown. When you break down horizontally, you're dealing with independent tasks like when I'm generating multiple different jokes, where each one stands alone. Each joke can be generated separately without losing anything.

But then there's vertical breakdown, where tasks are interdependent. You might start with a punchline and then craft the setup, but these parts influence each other. Comedians know this. They tweak both parts to make the joke land better. When you break it down, it breaks down.

So now, instead of breaking everything down, I ask myself whether the subtasks are independent or interdependent. For independent tasks, I divide horizontally. For interdependent tasks, I unite vertically.

I might sound like I've got this all figured out with my fancy "horizontal versus vertical" analysis, but the joke's on me. My generated jokes are still terrible! I'd love to hear about your approach to prompt structure. What's working for you?
