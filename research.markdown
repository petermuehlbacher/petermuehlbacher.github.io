---
layout: page
title: Research
permalink: /research/
---

{%- comment -%}
Each entry is an h3 title, a meta line (venue, year, co-authors, extra links), and a summary.
On narrow screens the title runs into the meta line, like the home page entries.
{%- endcomment -%}

<h2>Research Interests</h2>
<p>I work on AI agents that forecast and do research: building them, and measuring whether they are any good. Before that, I worked on probability theory and statistical mechanics, in particular quantum spin systems, sampling algorithms, couplings, and cluster expansion methods.</p>

<h2>Forecasting and AI</h2>
{% for item in site.data.forecasting_ai %}
<h3><a href="{{ item.url }}">{{ item.title }}</a></h3>
<p class="meta">{{ item.where }}, {{ item.year }}{% if item.authors %} · with {{ item.authors | replace: ". ", ".&nbsp;" }}{% endif %}</p>
<p>{{ item.summary }}</p>
{% endfor %}

{% if site.papers.size > 0 %}
<h2>Mathematics</h2>
{% for paper in site.papers %}
<h3><a href="{{ paper.DOI | default: paper.arxiv }}">{{ paper.title }}</a></h3>
<p class="meta">{{ paper.venue }}, {{ paper.year }}{% if paper.authors %} · with {{ paper.authors | replace: ". ", ".&nbsp;" }}{% endif %}{% if paper.arxiv %} · <a href="{{ paper.arxiv }}">arXiv</a>{% endif %}{% if paper.video %} · <a href="{{ paper.video }}">video</a>{% endif %}</p>
<p>{{ paper.abstract }}</p>
{% endfor %}
{% endif %}
