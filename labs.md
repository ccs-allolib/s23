---
layout: page
title: Labs
nav_order: 9
description: Lab Assignments
---

# Labs


{% for lab in site.labs %}
* [{{lab.num}}]({{ lab.url | relative_url}})&mdash;{{lab.desc}}
{% endfor %}

