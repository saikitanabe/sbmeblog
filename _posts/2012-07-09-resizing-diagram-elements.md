---
layout: post
title: "Element Auto Resize Helps Sketching"
description: ""
category: 
tags: []
---
{% include JB/setup %}

Sketchboard.Me changed slightly the way diagram elements are resized on the board. Now resize handle is more visible and it is shown only when the element is selected. This is to keep the board visually clean. It might make learning to resize slightly more difficult, but at the same time it is more visible when you click the element and diagram looks better as a whole. 

In the end Sketchboard.Me tries to give clever choices for each element how it behaves to enable quick sketching in agile projects. When element is autoresized you can concentrate on the content and Sketchboard.Me supports you to draw your thoughts without a hassle.

There are three types of resize behaviours: 
* **Element auto resizes the height**. You can change the width and element auto resizes the height. Note and text elements implement this kind of behaviour. This is to implement automatic word wrapping. 
* **Element auto resizes widht and height based on the text**. You can change the width and the height, but resize is effective only until you next time change the text.
* **No autoresize**. Container elements keep the width and the height as the user wants. It will always stay as resized. Container elements can contain something inside.

Rules seems to be complex, but those are meant to be working in a way that you don't need to even think about how resizing works. This post is just to clarify why this kind of approach has been selected.


Figure 1. Note element auto resizes the height and word wraps word
![Note Auto Resize](/images/note-auto-resize.png)

Figure 2. Class diagram can be resized, but restores the widht and height after typing a text.
![Class Element Auto Resize](/images/classdiagram-resize.png)

Figure 3. Container elements do not autoresize.
![Container Element Resize](/images/container-element-resize.png)

These behaviours have been added by thinking elements usages. Mostly you just want to draft something out and auto resize makes your life easier, most of the time...

It might be that in the future auto resize is an option for an element, to give user power to control which elements should be auto resized and which not.
