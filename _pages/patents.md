---
permalink: /patents/
title: "Patents Info"
excerpt: "This is a page not in the main menu"
author_profile: true
redirect_from: 
  - "/patents_info/"
  - "/patents.html"
---
{% include base_path %}

{% for post in site.patents reversed %}
  {% include archive-single.html %}
{% endfor %}
