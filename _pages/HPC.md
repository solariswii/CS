---
layout: archive
permalink: /hpc/
title: "High Performance Computing by Tags"
author_profile: true
header:
    image: "/images/.png"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
    {% assign posts = group_items[forloop.index0] %}
    <h2 id="{{ tag | slugify }}" class="archive_subtitle">{{ tag }}</h2>
    {% for post in posts %}
        {% includs archive-single.html %}
    {% endfor %}
{% endfor %}
