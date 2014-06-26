---
layout: page
title: Ralf's Blog
tagline: Coding
---
{% include JB/setup %}

## Articles about Java and distributed computing ##

{% for post in site.posts %}
  <hr>
  <h1>{{post.title}}</h1>  
  {{post.date|date: "%Y-%m-%d"}}

  {{post.description}}

  {% if post.figure %}
<a href="{{post.url}}"><img src="{{post.figure}}"/></a>
  {% endif %}

  [阅读全文]({{post.url}})
{% endfor %}


