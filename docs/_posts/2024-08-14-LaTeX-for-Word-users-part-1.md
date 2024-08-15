---
title: "LaTeX for Word users - part 1"
tags: [ tech, productivity ]
layout: post
---

LaTeX is the pre-eminent system for technical and academic publishing. 
However, it has a steep learning curve. Whole communities have sprung up to try and make sense of it. 
If you are coming from Word (Microsoft 365), the transition can be jarring. 
That said, LaTeX *is* worth the effort: it creates beautiful
documents, gives you fine-grained control over everything, and is the de facto standard for academic and technical publishing.
So here is an informal guide that addresses the most common things that you, a Word user, might need to do. 

## Where to get LaTeX
A good place to start is [Overleaf](https://www.overleaf.com), which provides a web-based LaTeX environment.
If you anticipate spending a lot of time in LaTeX, or need to be able to work largely 
offline, then install LaTeX locally on your PC. Popular choices are MikTeX and TeXLive. 
If you've never touched LaTeX before, MikTeX is slightly easier to get to grips with. 
However, if you really are going to be offline a lot, TeXLive installs everything you need 
right away, whereas MikTeX prefers to install pieces on demand, which is no use if you are on the road and disconnected.

## Getting oriented
LaTeX describes itself as a document preparation system, not a word processor. 
This is a polite way of saying that it pushes you strongly towards a content-first 
view of writing: focus on your words, and trust that LaTeX will make it look pretty.
You shouldn't be thinking, "does this header need to be in 10-point Calibri?" 
The closest equivalent in Word would be if you forced yourself to only ever use a pre-built template
and only ever apply formatting that is defined in the Styles Gallery on the ribbon. 
You might think of LaTeX applying the "styles" metaphor to every part of the document.

### What's with the `\ % } { $` stuff?
You'll see this all over LaTeX documents. Think of LaTeX a bit like a special language where your content (your words) is mingled with instructions on how to process those words (make them large, format them, etc.) The symbols are clues to the computer to stop
treating what it sees as just your words and start doing something with them. 

 - The percent sign `%` identifies comments in the document. These are comments internal to the document itself, e.g.
comments you might make about an imported package, and not in the Word sense, of material that the author wants
other collaborators to see and respond to concerning the content of the document.

 - Dollar sign `$` tells LaTeX to enter/leave "math mode", which produces better-looking 
results for mathematical equations and symbols.
 Even if you don't expect to use math in your document, you may still come across math mode from time to time, because the symbols
 creep into everyday usage and generally look better when formatted in math mode than in regular text. 

 - `\` precedes a command. For example, `\textbf`, to make what follows boldface. 
The curly braces enclose things that need to be operated on, and remove ambiguity, 
for example, `\textbf{one two}` compared to `\textbf one two` .

`\` also has another use: when you want to include a special character (like, "%") in your document text, without it being confused 
for a LaTeX command or comment, you can 'escape' it by preceding it with backslash: `\%` say. Use this technique when you need to write
symbols such as # (hash sign), $ (dollar sign), _ (underscore), and either of {} (curly braces).

```
The new model will be sold for under \$ 50.
``` 
 
## I want to create documents in a standard format
Approximate equivalent in Word: templates and styles.

### `documentclass`
For Word template, think LaTeX `documentclass`. The class gives you a bunch of prebuilt settings and styles 
that are tuned for that type of document. For example, `article` sets up for single-column, one-sided printing, 
and 10-point type, among other things, whereas `report` and `letter` handle things differently. 

Settings can be overridden. For example, maybe you need A4 paper instead of US Letter, 
or you want a different type size. No problem:

> `\documentclass[a4paper,12pt]{letter}`

### `usepackage`
Sometimes you need more than what a document class can give you by itself. Maybe you are writing an article, 
but need multiple levels of bullets, and advanced math symbols. Word has extensive functionality for common situations
but once you reach the limit of its capabilities, there is nowhere to go. By contrast, LaTeX is extensible. You can import
 functionality via packages. There are *thousands* of them. To import the capability of a package into your document, use 
the `\usepackage` command, for example:

``` 
\usepackage{enumitem}
\usepackage{fancyhdr}
\usepackage{lastpage}
\usepackage{hyperref}
```

### `newcommand`
If you can't find the package that does what you want, you can create your own shortcuts and functions. For example, 
imagine you are writing about sports teams, and you want every mention of the team name to be in small caps, 
and colored blue. You can create a shorthand, like this:

{% raw %}
```
\usepackage{xcolor}

\newcommand{\team}[1]{%
    \textsc{
        \color{blue}
        {#1}
        }%
    }
```

{% endraw %}

Then, you can write, say, `\team{Anytown College}` to get the style that you want.

### CLS files
Just as in the Word universe, eventually you'll get to a combination of documentclass, packages, and other settings that 
you like. At this point in Word you would create a `.dot` Word template file. In LaTeX, you create a "class file" (commonly, `.cls`).
Class files can import their own packages, define new commands, inherit and modify document class options, and can be referenced
in turn by your documents. For example:

```
%% snippet of a class file, CoverLetterClass.cls
%%
\ProvidesClass{CoverLetterClass}[2024/07/29 My custom Cover Letter class]

\LoadClass{article}

\RequirePackage{geometry}   % For page layout control
\RequirePackage{enumitem}   % for bulleted lists
\RequirePackage{fancyhdr}   % For the top-of-page header
\RequirePackage{hyperref}   % For live hyperlinks eg to make LinkedIn profiles clickable
```

```
%% snippet of a document that uses the class file
\documentclass{CoverLetterClass}
\begin{document}
  some text goes here
\end{document}
```  

Just as in Word, you are not restricted to the templates (class files) that you create yourself. There are numerous examples
online covering all kinds of use cases: resumes, business letters, presentations, etc. See for example, [latextemplates.com](https://www.latextemplates.com/).
 (If you are writing for publication it's very likely that your publisher will supply class files or packages for you 
 to use, so that submissions are in the right style.)

### What packages do I need? What class should I use?
There's no hard and fast rule here, but for a typical Word document, in a corporate environment, that has, say, bullets, numbered lists, page numbers, etc., a start would be to use the `article` class and the following packages:

```
\documentclass{article}
\usepackage{geometry}   % For page layout control
\usepackage{enumitem}   % for bulleted and itemized lists
\usepackage{fancyhdr}   % For headers and footers
\usepackage{hyperref}   % For live hyperlinks, i.e., to make URLs clickable
```

## OK, I'm ready to get started. 
LaTeX tries to keep out of your way. So, start a new document file, import your packages and/or class file, 
tell LaTeX what class of document it is, and away you go. Like so:

```
\documentclass{...}
\usepackage{...}
\usepackage{...}
\begin{document}
	Start typing here...
\end{document}	
```


In Part 2, we'll look at common requests from Word users and how to address them in LaTeX.

