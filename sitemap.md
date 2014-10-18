---
layout: page
title: "Sitemap"
permalink: /sitemap/
---

{% for p in site.pages %}
  {% if p.title and p != page and p.url != "/404.html" %}* [{{ p.title }}]({{ p.url | prepend: site.baseurl }}){% endif %}
{% endfor %}
{% for collection in site.collections %}
  {% if collection[1].output and collection[1].title %}* [{{ collection[1].title }}]({{ collection[0] | append: "/" | prepend: "/" | prepend: site.baseurl }}){% endif %}
{% endfor %}
