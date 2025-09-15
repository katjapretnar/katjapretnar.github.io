---
title: myplaces
layout: archive
permalink: /myplaces/
entries_layout: grid
---

Sample post listing for the places.

{% for place in site.data.places %}
  {% for post in site.posts | where:"place",{{places.name}} %}
      <a href="{{post.url}}">{{post.title}}</a>
  {% endfor %}
{% endfor %}