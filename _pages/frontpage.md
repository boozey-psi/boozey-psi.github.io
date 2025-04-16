---
permalink: /
layout: home
title: Welcome
list_title: My blog posts
---


        <h2>Recent Posts</h2>
        {% for post in site.posts limit:3 %}
          <article>
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
            {% if post.excerpt %}
              {{ post.excerpt }}
            {% else %}
              {{ post.content | truncatewords: 50 }}
            {% endif %}
            <a href="{{ post.url }}" class="read-more">Read More</a>
          </article>
        {% endfor %}
