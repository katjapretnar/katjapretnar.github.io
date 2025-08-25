---
title: "and more trial"
date: 2025-08-20
header:
  teaser: ../assets/2025_t/tri.png
categories:
  - sport
tags:
  - time autumn
  - place austria
  - sport climbing
---

{% capture fig_img %}
![Foo]({{ '../assets/2025_t/tri.png' | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Photo from Unsplash.</figcaption>
</figure>
