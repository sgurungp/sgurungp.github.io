---
title: "LaTeX for Word users - part 2"
tags: [ tech, productivity ]
mathjax: true
layout: post
---

# LaTeX for Word users - Part 2
(in development)

Let's look at some common scenarios that Word users hit when using LaTeX. If you missed the intro to LaTeX for Word users in Part 1, see [here](LaTeX-for-Word-users-part-1.html).

## Formatting words
```
\textbf{This text will be in boldface}
\textit{This will be in italics}
\underline{These words will be underlined}
```

```math
\textbf{This text will be in boldface}
\textit{This will be in italics}
\underline{These words will be underlined}
```

$a^2$ is a squared

The `ulem` package provides even more options e.g., double-underline (`\uuline`) and strikethrough (`\sout`).

## Formatting paragraphs
LaTeX fully-justifies paragraphs by default, and handles all the breaks and hyphenation for you. It takes great pains to flow paragraphs in a coherent and visually-pleasing way, so, be cautious about attempting to manually override its choices. That said, you might choose to set some of the following options: `flushleft`, `flushright`, `centered`. For example:


```
\begin{flushleft}
  some text that will be left-aligned...
\end{flushleft}
```

The `ragged2e` package provides additional control.
 
## Lists
Use the `enumerate` package, i.e. `\usepackage{enumerate}`.

### Bulleted lists
A bulleted list in Word maps to an itemized list in LaTeX:
```
\begin{itemize}
  \item this is the first bullet item
  \item this is another bullet item
\end{itemize}
```

### Numbered lists
@@@todo

### Nested lists
@@@todo

## Common symbols
Most symbols on the (US) keyboard are typed as-is. Notable exceptions, that need to be escaped (see [Part 1](https://sgurungp.github.io/2024/08/14/LaTeX-for-Word-users-part-1.html) are the ones on the number row of the (US) keyboard (`~`, `!`, `@`, `#`, ..., `_`), `\`,
 and `{}`. If in doubt, try it out!

Currency and other commercially useful symbols such as a trademark indicator can be found in the `textcomp` and `marvosym` packages. For example:

```
\usepackage{marvosym}
In Spain, this orange once cost \EUR 1, while in the US, it was \$ 2.50.
```

If you know what your symbol should look like, but you don't know what package it is in, use [Detexify search](https://detexify.kirelabs.org/classify.html) lets you 'draw' an approximation, and finds the best match for you.

## TODO
@@@ todo
styles
normal
nospacing
heading 1, 2, 3
title
change the symbol for bullets
multilayer lists
hyperlinks (hyperref pkg)
widow/orphan control 
inserting graphics
tables
footnotes
ToC
index
margins (geometry)
page numbers (lastpage, cfoot)
typeface (fa, sffamily)
