---
layout: page
permalink: /research/
---


<h2>Research Interests</h2>
<p>I work on AI agents that forecast and do research: building them, and measuring whether they are any good. Before that, I worked on probability theory and statistical mechanics, in particular quantum spin systems, sampling algorithms, couplings, and cluster expansion methods.</p>


<section>
<h2>Forecasting and AI</h2>
<ul>
{%- for item in site.data.forecasting_ai -%}
<li>
<strong>"{{ item.title }}"</strong>&nbsp;{%- if item.authors -%}with {{ item.authors | replace: ". ", ".&nbsp;" }},&nbsp;{%- endif -%}{{ item.year }}&nbsp;(<a href="{{ item.url }}">{{ item.where }}</a>)
<ul>
<li>{{ item.summary }}</li>
</ul>
</li>
{%- endfor -%}
</ul>
</section>


<section>
{%- if site.papers.size > 0 -%}
<h2>{{ page.list_title | default: "Mathematics" }}</h2>
<ul>
{%- for paper in site.papers -%}
<li>
<strong>"{{ paper.title }}"</strong>&nbsp;{%- unless paper.DOI -%}—pending publication&nbsp;{%- endunless -%}
{%- if paper.authors -%} with {{ paper.authors }}&nbsp;{%- endif -%}
{%- if paper.DOI -%}(<a href="{{paper.DOI}}">DOI</a>)&nbsp;{%- endif-%}
{%- if paper.arxiv -%}(<a href="{{paper.arxiv}}">arXiv</a>)&nbsp;{%- endif-%}
{%- if paper.video -%}(<a href="{{paper.video}}">video</a>)&nbsp;{%- endif-%}
<ul>
<li>{{ paper.abstract }}</li>
</ul>
<!--<p>Abstract: {{ paper.abstract }}</p>-->
</li>
{%- endfor -%}
</ul>

{%- endif -%}
</section>