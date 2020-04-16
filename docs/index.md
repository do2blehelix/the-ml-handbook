---
layout: default
title: Home
nav_order: 1
description: "Just the Docs is a responsive Jekyll theme with built-in search that is easily customizable and hosted on GitHub Pages."
permalink: /
---

# Welcome to The Machine Learning Handbook!


[Statistics]({{ site.baseurl }}{% link docs/statistics/statistics.md %}){: .btn .btn-purple }


Thank you for reading this. The Machine Learning Handbook was created to provide an overall glimpse of the Machine Learning and Statistical Algorithms. This Handbook connects the complex understanding with simple structures and lucid terminology.

Feel free to reach out to me in case you have and queries or suggestions.


<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>
