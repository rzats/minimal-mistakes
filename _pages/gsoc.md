---
title: "Google Summer of Code"
layout: archive
type: posts
author_profile: true
excerpt: "Google Summer of Code participation archive."
sitemap: false
permalink: /gsoc/
---

{% for post in site.categories.gsoc %}
    {% include archive-single.html %}
{% endfor %}

{% include paginator.html %}
