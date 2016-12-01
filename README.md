# vimcheatsheet

### Buffers, Windows, Tabs

1. A _buffer_ in Vim is an open instance of a file, that may not necessarily be visible on the screen.
2. A _window_ in Vim is a viewport onto a single buffer. When you open a new window with *:split* or *:vsplit* and include a filename, it opens that file in a new buffer and then opens a window onto that buffer.
3. A _tab_ is a collection of one or more windows. Think of a tab as a layout for a specific group of windows. You could achieve the same thing using a terminal multiplexer like [tmux](https://tmux.github.io/), which would preserve your collection of windows and allow you to flick back and forth.

### Buffers

|Cmd|Description|
|---|---|
|**:ls**|show buffer list|
|**:edit**|open file in buffer to edit|
|**:bn**, **:bp**|open next/prev buffer in current window|
|**:bfirst**, **:blast**|open first/last buffer in current window|
|**:sb**|split window and edit buffer by num or name|
|**:bunload|unload the buffer|

### Edit file under cursor

- **gf** - edit the file under the cursor

### Find file recursively to edit

- **:e \*\*/test/foo.js**

See [wildmode](http://vimdoc.sourceforge.net/htmldoc/options.html#'wildmode') for tab completion with wildcards.

### Scrolling the screen

- **zz** - move current line to the middle of the screen
- **zt** - move current line to the top of the screen
- **zb** - move current line to the bottom of the screen

|Cmd|Description|
|---|---|
|Ctrl-y|moves screen up one line|
|Ctrl-e|moves screen down one line|
|Ctrl-u|move screen up half a page|
|Ctrl-d|moves screen down half a page|
|Ctrl-b|moves screen up one page|
|Ctrl-f|moves screen down one page|

### File Explorer

- **:Sex** to split and open file explorer (horizontal split)
- **:Sex!** to split file explorer vertically
- **o** or **O** to open it in a new buffer (horizontal or vertical split)
- **p** to preview file (**:pedit fname**). use **:pclose** to close window.

## Visual Mode

See also [Visual Mode](http://vimdoc.sourceforge.net/htmldoc/visual.html).

### Visual Line Mode: Remove block of text

Use [Visual Line Mode](https://vimhelp.appspot.com/visual.txt.html).

1. Press **V** (shift + v)
2. Move cursor to select block of text.
3. Press **d**

### Visual Block Mode: Insert text

Use [Blockwise Visual Mode](http://usevim.com/2012/05/18/vim101-visual-mode-2/).

Use **Ctrl+V** (while in normal mode) to activate visual block mode. After selecting the block, you can press **Shift+i** (capital I) to start inserting before every line of the block.
