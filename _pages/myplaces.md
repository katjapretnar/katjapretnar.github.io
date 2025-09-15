---
title: myplaces
layout: archive
permalink: /myplaces/
entries_layout: grid
---

Sample post listing for the places.

{% assign entries_layout = page.entries_layout | default: 'list' %}
{% for place in site.data.places %}
    {% assign filtered_posts = site.posts | where: 'place', {{place.name}} %}
        {% for post in filtered_posts %}
            <a href="{{post.url}}">{{post.title}}</a>
        {% endfor %}
{% endfor %}
