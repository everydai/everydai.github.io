---
layout: page
title: "Everydai"
subtitle: Automobiles
css: "/css/index.css"
bigimg:
  - "/imgs/daytona.jpg" : "Daytona Fury"
  - "/imgs/onyx.jpg" : "Onyx 1 Goldcubes"
  - "/imgs/patek.jpg" : "Patek Painting"
---

<div class="list-filters">
  <a href="/festivals" class="list-filter">Festivals</a>

  <a href="/watches" class="list-filter">Watches</a>

  <a href="/automobiles" class="list-filter">Automobiles</a>
  
  <a href="/sports" class="list-filter">Sports</a>

  <a href="/amsterdam" class="list-filter">Amsterdam</a>

  <a href="/random" class="list-filter">Random mix</a>

  <a href="/customjobs" class="list-filter">Something else</a>

</div>

<div class="posts-list">
  {% for post in site.tags.watches %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>

	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>

![alt text](/imgs/festival.jpg)
