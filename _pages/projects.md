---
layout: splash
permalink: /projects/
title: "Projects"
excerpt: ""
header:
  overlay_image: /assets/images/japan.jpg
---

Selected open-source work and personal projects. The list below is refreshed
automatically from my public [GitHub profile](https://github.com/aobeysekara) —
see there for the full set.

{% if site.data.github_repos %}
<ul class="taxonomy__index">
{% for repo in site.data.github_repos %}
  <li>
    <a href="{{ repo.url }}">
      <strong>{{ repo.name }}</strong>
      {% if repo.language %}<span class="taxonomy__count">{{ repo.language }}</span>{% endif %}
    </a>
    {% if repo.description %}<br>{{ repo.description }}{% endif %}
    {% if repo.stars and repo.stars > 0 %} · ★ {{ repo.stars }}{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
Projects list is being refreshed. In the meantime, browse my work directly on
[GitHub](https://github.com/aobeysekara).
{% endif %}
