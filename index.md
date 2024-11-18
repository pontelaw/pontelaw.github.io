---
layout: default
---
<link href="/css/override.css" rel="stylesheet" type="text/css">

<section class="blog-index">
  {% for post in site.posts %}
  <article class="post-summary h-entry" itemscope itemtype="http://schema.org/BlogPosting">
    <header class="post-header">
      <h2 class="post-title p-name" itemprop="name headline">
        <a href="{{ post.url | relative_url }}" class="u-url" itemprop="url">{{ post.title | escape }}</a>
      </h2>
      <p class="post-meta">
        <time class="dt-published" datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
          {{ post.date | date: date_format }}
        </time>
      </p>
    </header>

    <div class="post-excerpt" itemprop="description">
      {{ post.excerpt | strip_html | truncatewords: 30 }}
    </div>

    <a href="{{ post.url | relative_url }}" class="read-more">Read More</a>
  </article>
  {% endfor %}
</section>
