---
layout: category
permalink: /categories/Development/
taxonomy: Development
title: "Developer Work"
author_profile: true
---

This page will contain all of the posts for my development projects over the years

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}