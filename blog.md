---
layout: default
title: Blog
permalink: /blog/
---

<section class="section container">
  <div class="section-heading">
    <h1>Blog</h1>
    <p>All posts.</p>
  </div>

  <div class="post-grid">
    {% for post in site.posts %}
      <article class="post-card">
        <div class="post-card-content">
          <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.excerpt %}
            <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
          {% endif %}
          <a class="read-more" href="{{ post.url | relative_url }}">Read more →</a>
        </div>
      </article>
    {% endfor %}
  </div>
</section>