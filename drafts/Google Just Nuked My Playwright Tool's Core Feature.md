We built this command-line tool to install and configure extensions automatically. The tool used Playwright and the Chrome DevTools Protocol (CDP) connection to do its job. It was handy for setting up new environments.

Then a Chrome update basically killed that connection. It looks like Google disabled connecting over CDP for the default user profile.

This broke my tool. The whole reason I built it stopped working. I almost gave up on the tool.

My friend said, "Why not switch browsers if Chrome keeps breaking your stuff?"

I said, "Because there's no place like Chrome."

I managed to find a partial fix. I took out the code that needed the CDP connection. Now the tool just copies the extension files into the profile directory. This gets the extension installed, sort of. But the extension starts disabled. It is definitely not the ideal solution.

Here is the link to the updated tool if you want to see what I mean:

My workaround is okay, but it is not really what I wanted. Has anyone found a better way to programmatically manage or configure extensions?

I am open to any any suggestions or collaboration. Please let me know if you figured something out.
