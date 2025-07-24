---
layout: default
title: Blog
---

<h1>Blog</h1>

<style>
.blog-list {
  list-style: none;
  padding: 0;
}

.blog-list li {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  margin-bottom: 10px;
  padding: 5px 0;
}

.blog-list a {
  text-decoration: none;
  color: inherit;
}

.blog-list a:hover {
  text-decoration: underline;
}

.blog-date {
  color: #666;
  font-size: 0.9em;
}
</style>

<ul class="blog-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span class="blog-date">{{ post.date | date: "%b %d %Y" }}</span>
    </li>
  {% endfor %}
</ul>



