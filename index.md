---
layout: page
title: Sketchboard.Me latest features and thoughts
---
{% include JB/setup %}

[@SketchboardMe](http://twitter.com/#!/sketchboardme)

<div class="row">
	<div class="span7">
		{% for post in site.posts %}
		<h1><a href="{{post.url}}">{{post.title}}</a></h1>
		{{post.content}}
		{% endfor %}
	</div>
	<div class="span4">
		<ul class="unstyled posts">
		  {% for post in site.posts %}
		    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
		  {% endfor %}
		</ul>
	</div>	
</div>
