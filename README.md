# About this repository

`BYACC/J` is project that is an extension of the Berkeley v 1.8 YACC-compatible parser generator to produce C/C++ and Java parsers.

It was developed by Tomas Hurka, see more details ot its [web site](http://byaccj.sourceforge.net/).

## Why ressuscite an old project?

There is an annoying bug in its actual version, so I would like to provide a fix for it (as the original project does not seem to be active anymore).

The main problem was that the present code was corrupting the stack, so the parser was not correctly working. The modification requires to additionally implement `clone` method in the semantic class.

## Why still use `byacc/j`?

There are several reasons to do it:

- It still can be interesting to have a single executable for a Java parser generator (no templates directory, no additional configuration).
- There is a single generated file for the parser. This may look old-style, but it simplifies the life sometimes.

Putting altogether, this parser generator can be used for educational projects or for self-contained projects (shipping the byaccj binary). 