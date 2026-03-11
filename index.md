---
layout: default
title: Home
---

<section class="hero">
  <div class="hero-overlay">
    <div class="container hero-content">
      <p class="hero-kicker">South America Travels</p>
      <h1>{{ site.title }}</h1>
      <p class="hero-text">
      Nossas aventuras estão só começando...
      </p>
      <a class="btn" href="{{ '/blog' | relative_url }}">Leia o blog</a>
    </div>
  </div>
</section>

<section class="section container">
  <div class="section-heading">
    <h2>Posts mais recentes</h2>
    <p>Recent writing from the blog.</p>
  </div>

  <div class="post-grid">
    {% for post in site.posts limit:6 %}
      <article class="post-card">
        <div class="post-card-content">
          <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.excerpt %}
            <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
          {% endif %}
          <a class="read-more" href="{{ post.url | relative_url }}">Read more →</a>
        </div>
      </article>
    {% endfor %}
  </div>
</section>