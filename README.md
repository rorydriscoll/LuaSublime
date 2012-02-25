Description
===========

These are a collection of various different support files useful for developing Lua using Sublime Text 2.

Installation
============

These files should be placed into the Lua package directory. For those on OS X, this can be found at:

/Users/[USERNAME]/Library/Application Support/Sublime Text 2/Packages/Lua

For Windows, this directory is here:

C:\\Users\\[USERNAME]\\AppData\\Roaming\\Sublime Text 2\\Packages\\Lua

Contents
========

Lua.tmLanguage
Lua.JSON-tmLanguage

These are new language grammar files for syntax highlighting. Compared to the one that ships with Sublime Text, you get the following:

- More tokens: Things like function calls and variables are now tagged, so they will show up correctly colored.
- Better scopes: Most blocks now have some nested scoping support. This means that if you're in an if-block inside a function inside another function, then it knows this. Visually there's no difference, but if you use the expand-scope command then you will find that you'll get far better matches now.

Lua.sublime-build

This is a build system that runs the current lua file

ParseLua.py

This is a plugin that continually parses the current lua file and highlights any errors by placing a dot in the margin. Lua appears to stop at the first error, so you should only ever see one dot. The error message will be shown in the status bar.
