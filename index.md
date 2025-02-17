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
    {% for project in site.projects %}
      <article class="project-item">
        <h2>
          <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
        </h2>
        <p class="project-meta">{{ project.date | date: "%B %-d, %Y" }}</p>
        {% if project.description %}
          <p>{{ project.description }}</p>
        {% endif %}
      </article>
    {% endfor %}
  </section>
</div>

