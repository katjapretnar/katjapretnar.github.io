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
        <section id="{{ place.name }}" class="taxonomy__section">
            <h2 class="archive__subtitle">{{ place.name }}</h2>
                <div class="entries-{{ entries_layout }}">
                    {% for post in filtered_posts %}
                        {% include archive-single.html type=entries_layout %}
                    {% endfor %}
                </div>
        </section>
    {% endfor %}
{% endfor %}
