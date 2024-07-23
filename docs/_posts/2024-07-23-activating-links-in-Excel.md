---
title: "TIL: A LinkedIn tip, and an Excel hack"
tags: [ tech, productivity ]
layout: post
---

I've been on LinkedIn for years, but TIL that you can export all your connections in one go to Excel,
giving to a spreadsheet of your connections' names, LinkedIn profile URLs, email address and current
position. Very handy if you want to do some pruning or targeted outreach.

## Exporting your connections from LinkedIn
1. Use a PC, and log in to LinkedIn. (If you try this on mobile, LinkedIn will indicate that you 
need to be on the desktop site).
2. Select "**Me**" on the top right, then *Settings & Privacy* > *Data Privacy*
3. Choose *Get a copy of your data*
4. Check the boxes labeled *Connections* and *Imported Contacts*, then, hit **Request Archive**

The process kicks off in the background, so you can exit here and LinkedIn will send you an email when
it is complete. As a rough guide, 1000 connections shows up in under a day and generates a small file that 
is easy to download and copy using the link in the email.

## Is that all there is to it?
Almost. The export file may have some oddities that you will want to clean up before analyzing in detail:
- blank lines
- two contacts might call the same company by different names, e.g. "ABC" and"ABC Corp." You might want to normalize the names.
- the export file makes a mess of some characters, such as those with accents, and especially non-Roman scripts. 
  If you have contacts in, say, Taiwan, you'll almost certainly need to do some work here.
- The LinkedIn URL for each contact is not "clickable" by default. Which leads me on to today's hack.

## Excel web links
Normally, when Excel sees a cell containing a URL, such as `https://www.linkedin.com/in/shriman`, it knows to treat it
as a clickable entity: if a user of the spreadsheet clicks (or Ctrl-clicks) the cell, they'll visit the link. 
Sometimes Excel needs a kick to remember this, which can be as simple as pretending to edit the cell (F2, as if you were editing 
the cell, then Enter). But that is tedious if you have hundreds or thousands of links. (As in, you've just 
exported all your LinkedIn contacts and realized the links are not clickable.)

You can record an Excel macro to fix this, something like this code:
```
Sub Macro1()
'
' Macro1 Macro to convert a URL into a clickable link.
'
    Dim Cell As Range
    ' We only want to change cells on the active sheet that have that have been chosen
    ' by the user, and that contain a value. We use the intersection of the used cells
    ' on the sheet and the user's selection, then only consider the cells that contain entries.
    For Each Cell In Intersect(Selection, ActiveSheet.UsedRange)
        If Cell <> "" Then
            ActiveSheet.Hyperlinks.Add Cell, Cell.Value
        End If
    Next
End Sub
```

Then, you select the cells you want to activate, run the macro, and you are done.

The hack is that this macro *does not need to be saved in your workbook*. Macros have a checkered reputation because
they can do almost anything your PC can be made to do, which means, create all kinds of mischief. You might not even want that
possibility around, in which case, you don't want any macro-enabled workbooks on your PC. But you can still still write and
run macros, just by turning on Developer mode in the Ribbon, and then deliberately choose not to save the macro.

## Sidebar - extending Excel and 365
The story of how to extend Excel and 365 in general is fascinating. Excel macros are written in Visual Basic for Applications, VBA.
VBA is the spiritual descendant of Microsoft's Visual Basic programming language, circa 1998, and, like the code from that era, 
allows you to do incredible things like create charts, reformat spreadsheets, manipulate data, ... without
worrying too much about security. (I personally knew someone who built an entire pricing and quoting system in VBA. I can perhaps best
describe it as a gold-and-jewel-encrusted chainsaw: one was left simultaneously terrified and in awe of the artistry.)

VBA support exists across 365 (Office). I suspect that Microsoft would like nothing more 
than to end it, but there's probably a bank or key part of our economy whose entire edifice is built on some analyst's 
code, and perhaps in an attempt not to accidentally destroy civilization, they have resisted.

Moreover, today's Excel is not your grand-pappy's. It runs on the Web and on phones. Maybe, Microsoft reasons, 
the developers would like some JavaScript with their Excel? Well, yes, 
[they do that too](https://learn.microsoft.com/office/dev/add-ins/excel/excel-add-ins-overview). 
You can do almost anything that (web) Excel can do in JavaScript (here, it's called OfficeScript), and it's 
much more broadly portable to non-PC platforms. VBA still wins in terms of raw capability, but the direction seems to be clear: 
the future is OfficeScript.

Then again, it could be Python. Microsoft has recently shown public previews of Python running in Excel 
(details [here](https://support.microsoft.com/office/get-started-with-python-in-excel-a33fbcbe-065b-41d3-82cf-23d05397f53d).
Python offers another way to extend Excel, this time by embedding a Python programming language interpreter into Excel and making it
easily consumable by anything that can call the `xl()` function and tell the code what to do. I see this more as a bridge between
the world of Excel (business, analysis, engineering formulas) and the world of data analytics (`numpy`, `pandas`, R). It'll probably
take a few months to shake out but this looks like a pretty important development for the next decade of Excel. And, if I'm honest, 
an important one for Microsoft to avoid Excel's pre-eminent position being eroded by Jupyter and similar tools.

