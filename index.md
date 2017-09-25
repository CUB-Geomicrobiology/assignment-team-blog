---
layout: default
permalink: /
---

{% for p in site.pages %}
{% if p.title and p.url <> "/" %}
## [{{ p.title }}]({{ site.baseurl }}{{ p.url }})
{% endif %}
{% endfor %}
