---
title: "LaTeX for Word users, pt.3"
tags: [ tech, productivity ]
layout: post
mathjax: true
---

*(If you missed the earlier posts, see [here](LaTeX-for-Word-users-part-1.html).)*

Welcome to Part 3! This series turned out to be quite a bit more popular than I anticipated, for which
I am grateful. In this post, we'll mop up a few loose ends and take on some more unusual and advanced topics
as well.

# Contents
 - [Typefaces and fonts](#typefaces)
 - [Paragraph indentation](#paragraph-indentation)
 - [Line spacing and numbering](#line-spacing-and-numbering)
 - [Footnotes](#footnotes)
 - [Spellcheck](#spellcheck)
 - [Summary](#summary)

## Typefaces and fonts
Word collapses the art and science of typography into a very small set of choices: 
pick the font family (Calibri, Times New Roman, etc.) from the drop-down, and 
then press the button to modify it to be bold or italic. Sometimes the font family
already includes variants in different weights as if, say, "bold" was already selected.
It's convenient, but it's not elegant, and I'm sure typography people wince at it.
*todo: sfffamily, and https://www.overleaf.com/learn/latex/Font_typefaces
suggest recs for Times for TNR, HElvetica for Arial, courier vs  Computer Modern Typewriter (cmtt) for Consolas*

```tex
\textbf{This text will be in boldface}
\textit{This will be in italics}
\underline{These words will be underlined}
```
The `ulem` package provides even more options e.g., double-underline (`\uuline`)
 and strikethrough (`\sout`), e.g. `\sout{strike me out}`.

![LaTeX sample: charformats]({{ '/assets/imgs/latex-sample-charformats.png' | relative_url }})



## Paragraph indentation
*\setlength{\parindent}{0pt}
 discuss how to indent a whole para
https://thelinuxcode.com/indent-latex/ \hspace{xem}, etc*

![LaTeX sample: paraformats]({{ '/assets/imgs/latex-sample-paraformats.png' | relative_url }})

## Line numbering
https://texblog.org/2012/02/08/adding-line-numbers-to-document
\usepackage{lineno}
\linenumbers

Spacing
https://kb.mit.edu/confluence/pages/viewpage.action?pageId=390709
\usepackage{setspace}
\doublespacing befoe the doc begins
\onehalfspacing
\begin{singlespace}...\end


```tex
\section{Executive overview}
  The section command marks a new section. Put the title in curly braces.
  Then, write the content.
  ...
\section{Background}
  You can start a new section at any time, and LaTeX will number them automatically.
  ...
  \subsection{Event timeline}
  You can include subsections, and subsubsections, to drill down further.
  ...
\section*{Risk assessment}
  A special feature is that by tagging a section with an asterisk, the section
  will not be included in any table of contents.
```

For the table of contents, simply invoke the `\tableofcontents` command.
Typically this is at the top of the document, of course.

```
\tableofcontents
```

## Footnotes
@@@tbd

## Spellcheck
There isn't one built in, but Overleaf has one and you can pipe to other tools eg ispell

A bulleted list in Word maps to an itemized list in LaTeX:
```tex
\begin{itemize}
  \item Operations
  \item Security
  \item Investor Relations
\end{itemize}
```


## Summary
These notes are not intended to represent the "best" or "only" way to use LaTeX 
if you come from Word. But I hope that I have been able to explain how LaTeX
thinks about documents, how it differs from Word, and how some of the most
common operations in Word might look in LaTeX. Got any comments? Let me know.
