---
layout: page
title: Linux Kategorisi
permalink: /kategori/linux
sitemap: false
---


{% assign categories = "Linux" %}



{% for category in categories %}
<a name="{{ category }}"></a>
{% assign sorted_posts = site.posts | sort: 'title' %}
{% for post in sorted_posts %}
{%if post.categories contains category %}

<h3><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.date |  date: "%B %e, %Y" }} - {{ post.title }} <p class="date"></p></a></h3>
<p>{{ post.excerpt | strip_html | truncate: 160 }}</p>

{%endif%}
{% endfor %}

{% endfor %}
