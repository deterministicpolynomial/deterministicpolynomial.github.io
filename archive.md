---
layout: page
title: Blog Archive
---

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

<h1>Posts by Tag</h1>

{% assign all_tags = site.tags | sort %}
{% for tag in all_tags %}
  <h2 id="{{ tag[0] }}">{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span>({{ post.date | date: "%Y-%m-%d" }})</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
