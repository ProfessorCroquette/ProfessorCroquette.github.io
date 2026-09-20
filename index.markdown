---
layout: default
---

<div class="hero">
  <h1>Hi, I'm Professor Croquette</h1>
  <p>Engineering notes, code, and research from my studies and thesis work.</p>
</div>

<div class="content">
  <h2>Projects</h2>
  <ul class="post-list">
    {% for project in site.projects %}
    <li>
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
      <div class="date">{{ project.tech }}</div>
      {% if project.summary %}<p>{{ project.summary }}</p>{% endif %}
    </li>
    {% endfor %}
  </ul>
</div>

<div class="content">
  <h2>Latest posts</h2>
  <ul class="post-list">
    {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div class="date">{{ post.date | date: "%B %-d, %Y" }}</div>
    </li>
    {% endfor %}
  </ul>
</div>
