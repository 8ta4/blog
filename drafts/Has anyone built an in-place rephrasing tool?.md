I'm done with leaving my editor just to fix one sentence. I'm just trying to keep my prose clean without ever moving my cursor or switching contexts.

I haven't built the tool yet. But I've documented the design:

- https://github.com/8ta4/word/blob/9a1d26f5a42602dc6338961027d547a43ddae472/README.md

- https://github.com/8ta4/word/blob/9a1d26f5a42602dc6338961027d547a43ddae472/DONTREADME.md

By using [Groq](https://groq.com), I can pull suggestions from a model fast enough to keep the whole thing feeling snappy. I want to hit a keybind inside a sentence, check two alternatives in a bottom overlay, and hit another key to swap the text.

Has anyone here worked on something like this? I'd love to see how other people have tackled latency and caching before I commit to the implementation.
