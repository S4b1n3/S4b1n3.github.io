---
layout: archive
title: "News & Updates"
permalink: /news/
author_profile: true
---

{% include base_path %}

A running log of recent updates (papers, talks, code, etc.).

<div class="notice--info" style="margin-top: 1rem;">
  I keep these as short entries (1–2 lines) and link out to the paper/talk/code when relevant.
</div>

{% assign updates = site.data.updates | sort: "date" | reverse %}

{% for u in updates %}
### {{ u.title }}
<span style="opacity:0.75;">{{ u.date | date: "%B %-d, %Y" }}</span>

{{ u.text }}

{% if u.image %}
  <figure style="margin: 0.75rem 0 1rem 0;">
    <img src="{{ u.image | relative_url }}" alt="{{ u.alt | default: u.title }}" style="max-width: 100%; border-radius: 10px;">
    {% if u.caption %}<figcaption style="opacity:0.75;">{{ u.caption }}</figcaption>{% endif %}
  </figure>
{% endif %}


{% if u.links %}
<ul>
  {% for l in u.links %}
    <li><a href="{{ l.url }}">{{ l.label }}</a></li>
  {% endfor %}
</ul>
{% endif %}

{% if u.tags %}
<p style="margin-top:-0.5rem; opacity:0.75;">
  {% for t in u.tags %}
    <span style="display:inline-block; margin-right:0.35rem;">#{{ t }}</span>
  {% endfor %}
</p>
{% endif %}

<hr style="margin: 1.25rem 0;">
{% endfor %}
