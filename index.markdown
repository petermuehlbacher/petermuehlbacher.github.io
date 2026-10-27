---
bigheader: true
---

<div class="home">
<div markdown="1">
  {%- if page.title -%}
    <h1 class="page-heading">{{ page.title }}</h1>
  {%- endif -%}

I build and evaluate AI agents that forecast and do research at [FutureSearch](https://futuresearch.ai). Before that, I did forecasting research at [Metaculus](https://www.metaculus.com) and a PhD in probability theory.

For further details, see my [CV](CV.pdf) or [contact me via email](mailto:peter@muehlbacher.me).

<div>
    {%- include social.html -%}
</div>
</div>

  <!--{%- if site.posts.size > 0 -%}
    <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2>
    <ul class="post-list">
      {%- for post in site.posts -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
  {%- endif -%}-->

<!-- {% assign categories = "maths|languages|programming|forecasting" | split: "|" %}
{%- for category in categories -%}
    {%- if site.category.size > 0 -%}
        lol
    {%- endif -%}
{%- endfor -%} -->

<div class="level0">
 <!--MATHS-->
  {%- if site.maths.size > 0 -%}
  <section class="level1">
  <h2 class="post-list-heading">{{ page.list_title | default: "Mathematics" }}</h2> 
  <ul class="post-list">
    {%- for page in site.maths -%}
    {%- unless page.draft -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <!--<span class="post-meta">{{ page.updated | date: date_format }}</span>-->
      <h3>
        <a class="post-link" href="{{ page.url | relative_url }}">
          {{ page.title | escape }}
        </a>
      </h3>
        {{ page.about }}
    </li>
    {%- endunless -%}
    {%- endfor -%}
  </ul>
  </section>
  {%- endif -%}

<!--FORECASTING-->
  {%- if site.forecasting.size > 0 -%}
  <section class="level1">
  <h2 class="post-list-heading">{{ page.list_title | default: "Forecasting" }}</h2> 
  <ul class="post-list">
    {%- for page in site.forecasting -%}
    {%- unless page.draft -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <!--<span class="post-meta">{{ page.updated | date: date_format }}</span>-->
      <h3>
        <a class="post-link" href="{{ page.url | relative_url }}">
          {{ page.title | escape }}
        </a>
      </h3>
        {{ page.about }}
    </li>
    {%- endunless -%}
    {%- endfor -%}
  </ul>
  </section>

  {%- endif -%}

<!--PROGRAMMING-->
  {%- if site.programming.size > 0 -%}
  <section class="level1">
  <h2 class="post-list-heading">{{ page.list_title | default: "Programming" }}</h2> 
  <ul class="post-list">
    {%- for page in site.programming -%}
    {%- unless page.draft -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <!--<span class="post-meta">{{ page.updated | date: date_format }}</span>-->
      <h3>
        <a class="post-link" href="{{ page.url | relative_url }}">
          {{ page.title | escape }}
        </a>
      </h3>
        {{ page.about }}
    </li>
    {%- endunless -%}
    {%- endfor -%}
  </ul>
  </section>

  {%- endif -%}

<!--LANGUAGES-->
  {%- if site.languages.size > 0 -%}
  <section class="level1">
  <h2 class="post-list-heading">{{ page.list_title | default: "Languages" }}</h2> 
  <ul class="post-list">
    {%- for page in site.languages -%}
    {%- unless page.draft -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <!--<span class="post-meta">{{ page.updated | date: date_format }}</span>-->
      <h3>
        <a class="post-link" href="{{ page.url | relative_url }}">
          {{ page.title | escape }}
        </a>
      </h3>
        {{ page.about }}
    </li>
    {%- endunless -%}
    {%- endfor -%}
  </ul>
  </section>

  {%- endif -%}

</div>
</div>