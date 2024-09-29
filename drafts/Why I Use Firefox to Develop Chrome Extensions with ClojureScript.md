If you're developing a Chrome extension and trying to use the REPL, you might have noticed... it just doesn't work in Chrome because of the new Manifest V3 restrictions.

But here's a trick I found: Firefox doesn't have this restriction! You can actually develop your Chrome extension in Firefox and use the REPL.

I've set up a development environment that automates the workflow. I used [`web-ext`](https://github.com/mozilla/web-ext) to tweak Firefox's configuration for REPL compatibility and to launch the web extension. You can check it out in [my repo](https://github.com/8ta4/quest).

Now, there are a few caveats:

- Chrome vs. Firefox: The APIs are similar, but there are differences between the two browsers.

- REPL: The REPL works fine in content scripts, but not in the background scripts.

- Custom formatters: [Custom formatters for ClojureScript don't work](https://github.com/binaryage/cljs-devtools/issues/71) in Firefox.

Some folks have even gone as far as [building their own modified versions of Chromium](https://github.com/thheller/shadow-cljs/issues/902) to get around this issue. It would be amazing if someone released a version of Chromium with REPL support built in and updated automatically with each new release.

When I explained this setup to my girlfriend, she just rolled her eyes and said, "Do you enjoy making life complicated, or is using ClojureScript just some kind of hobby?"

To which I replied, "Yes. And that's exactly why I haven't dumped you."

If anyone has tips on optimizing the workflow, I'd love to hear them!
