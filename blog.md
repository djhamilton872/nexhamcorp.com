---
layout: default
title: Blog
---

<section style="padding-top: 8rem;">
  <div class="container">
    <div class="section-header">
      <h2>Blog</h2>
      <p>Thoughts on software, AI, and building things that matter.</p>
    </div>
    <div class="blog-list">
      {% for post in site.posts %}
      <div class="blog-post-preview">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %e, %Y" }}</time>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>{% endif %}
      </div>
      {% endfor %}
      {% if site.posts.size == 0 %}
      <p style="text-align: center; color: var(--slate); padding: 2rem 0;">Posts coming soon.</p>
      {% endif %}
    </div>
  </div>
</section>
