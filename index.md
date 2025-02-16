---
layout: default
title: Strona Główna
---

<div class="home">
  <section class="intro">
    <h1>{{ site.title }}</h1>
    <p>{{ site.description }}</p>
  </section>

  <section class="content">
    {% for post in site.posts %}
      <article class="post-item">
        <h2>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
        {% if post.description %}
          <p>{{ post.description }}</p>
        {% endif %}
      </article>
    {% endfor %}
  </section>
</div>
