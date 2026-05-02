I'm looking for a way to filter large buffers in-place while keeping the data editable. It's like an Excel spreadsheet: you filter the rows to hide the noise and continue to work on the data within the sheet itself.

Telescope doesn't work for this. I want to navigate and edit within the filtered results in the main window.

Here are the features I'm looking for:

- Regex search: The input must support regular expressions so I can search and evaluate complex patterns across the buffer.

- Conceal-based masking: Non-matching lines are hidden using Neovim extmarks and the conceal attribute.

- Async interruption logic: Typing triggers a background regex scan. The logic is async so the editor doesn't freeze while processing 1M+ lines. Too big? That's what Sheet said. If I type a new character before the previous scan finishes, the old job must be killed.

- 1-row input bar: The UI is a 1-row floating bar that pops up when a filter is active. It stays open while I swap focus between the bar and the buffer. If I clear the filter, the bar goes away.

Does anyone know of an existing plugin that handles this type of interactive masking?
