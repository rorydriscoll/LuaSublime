LuaSublime
==========

A collection of various different support files useful for use when programming in Lua using Sublime Text 2.

Installation
------------

These files should be placed into the Lua package directory. For those on OS X, this can be found at:

`/Users/[USERNAME]/Library/Application Support/Sublime Text 2/Packages/Lua`

For Windows, this directory is here:

`C:\\Users\\[USERNAME]\\AppData\\Roaming\\Sublime Text 2\\Packages\\Lua`

Contents
--------

### Syntax Coloring

`Lua.tmLanguage`
`Lua.JSON-tmLanguage`

These files define a language grammar for syntax highlighting lua files. Compared to the one that ships with Sublime Text, you get the following:

- _More tokens_: Things like function calls and variables are now tagged, so they will show up correctly colored.
- _Better scopes_: Most blocks now have some nested scoping support. This means that if the carat is on a variable in an if-block inside a function inside another function, then it knows this. This doesn't affect the coloring, but if you use the 'expand selection to scope' command then you will find that you'll get far better matches now.

For comparison, here's how the old syntax-highlighting looks with the Twilight color scheme:

![Old](https://github.com/rorydriscoll/LuaSublime/raw/master/OldHighlighting.png)

And here's the new one:

![New](https://github.com/rorydriscoll/LuaSublime/raw/master/NewHighlighting.png)

### Build System

`Lua.sublime-build`

This is a simple build system that compiles and runs the current lua file. You can jump between errors using F4.

### Live Parser

`ParseLua.py`

This is a small plugin that continually parses the current lua file and highlights any errors by placing a dot in the margin. 

![Syntax Error](https://github.com/rorydriscoll/LuaSublime/raw/master/SyntaxError.png)

Lua appears to stop at the first error, so you should only ever see one dot. The error message will be shown in the status bar.

![Status Bar](https://github.com/rorydriscoll/LuaSublime/raw/master/StatusBar.png)