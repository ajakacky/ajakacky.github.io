---
layout: archive
permalink: /development/
title: "Developer Work"
author_profile: true
categories: ['development', 'software']
---

This page will contain all of the posts for my development projects over the years

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% if page.categories contains post.category %}
        {% include archive-single.html %}
    {% endif %}
  {% endfor %}
{% endfor %}