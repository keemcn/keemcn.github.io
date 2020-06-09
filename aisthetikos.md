---
layout: page
title: αἰσθητικός
permalink: /aisthetikos/
---

{% for image in site.static_files %}
{% if image.path contains 'images/aisthetikos' %}
![]({{ site.baseurl }}{{ image.path }}){:height="400px" width="400px"}
{% endif %}
{% endfor %}