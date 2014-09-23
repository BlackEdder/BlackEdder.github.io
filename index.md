---
layout: page
title: Posts
---
{% include JB/setup %}

{% for post in site.posts limit: 10 %}

## [{{ post.title }}]( {{ post.url }} )

#### {{ post.date | date_to_long_string }}

{{ post.content }}

[Post a comment]( {{ post.url }} )

{% endfor %}
