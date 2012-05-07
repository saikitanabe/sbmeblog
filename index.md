---
layout: page
title: Blog Posts!
---
{% include JB/setup %}

[@SketchboarMe](http://twitter.com/#!/sketchboardme)

{% for post in site.posts %}
<h1><a href="{{post.url}}">{{post.title}}</a></h1>
{{post.content}}
{% endfor %}

