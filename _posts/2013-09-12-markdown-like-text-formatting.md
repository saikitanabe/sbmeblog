---
layout: post
title: "Markdown Like Text Formatting"
description: ""
category: 
tags: []
---
{% include JB/setup %}

_Highlight important topics on your board using text formatting._

Sketchboard users have requested a possibility to format text.
For starters __Note__ and __Just Text__ elements implement simple text formatting.
Formatting is based on __Markdown__, initially following text formatting rules
are used.

There are some differences for Markdown. One of the biggest difference is that 
line breaks are obeyed. Other is that Sketchboard legacy \*bold\* makes text bold
and not emphasized. In the future another probable exception might be that two underscores 
are used for \__underlined text\__ and not for text bolding.

Headings
========

Note Element
![Heading Syntax (Notes)](/images/note-heading-markdown.png)

Just Text Element
![Heading Just Text](/images/just-text-heading.png)

Bullets
=======

![Notes Bullets Syntax](/images/note-bullets-markdown2.png)
![Just Text Bullets](/images/just-text-bullets.png)

You can use either - or * characters for bullet point.

\- First Level 1

\-- Second Level 1

\--- Third Level 1

__Note__, Sketchboard syntax differs from Markdown, nested bullet list does not use 
spaces before the bullet point. E.g. tab would focus browser address bar by default and 
at least for now that functionality is not overridden.

Bold and Italics
================

![Bold and Italic](/images/note-bold-italic.png)

Escaping
========
When you want to show characters used in formatting, those needs to be
escaped with \\.
![Note Escaping](/images/note-escaping.png)

Thanks
======
Thanks to this excellent markdown library [Marked](https://github.com/chjj/marked).