---
title: Home
layout: default
---

<h1 style="font-family: 'Georgia', sans-serif">{{ site.title }}.com</h1>

<p>{{ site.description }}</p>

<h2>Latest Posts</h2>

<ul class="feed">
    {% for post in site.posts limit:3 %}
    <li class="feed-item">
    	<p class="feed-item__date"><time>{{ post.date | date: "%Y-%m-%d"}}</time></p>
    	<h1 class="feed-item__title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h1>
    </li>
    {% endfor %}
    
    <p style="margin-top: 1.5rem;"><a id="all_posts" href="{{ '/posts' | relative_url }}">View all posts →</a></p>
</ul>