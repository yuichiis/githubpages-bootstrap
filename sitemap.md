---
layout: page
title: "Sitemap"
permalink: /sitemap/
---

{% for page in site.pages %}
  {% if page.title %}* [{{ page.title }}]({{ page.url | prepend: site.baseurl }}){% endif %}
{% endfor %}
{% for collection in site.collections %}
  {% if collection[1].title %}* [{{ collection[1].title }}]({{ collection[0] | append: "/" | prepend: "/" | prepend: site.baseurl }}){% endif %}
{% endfor %}
