---
permalink: /
title: "KAN4Met"
excerpt: "Kolmogorov-Arnold Networks with applications in weather forecasting (KAN4Met)"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

During the last year we have witnessed two ground-breaking contributions in mathematical aspects of Deep Learning and Deep Learning applied to weather forecasting:

1. Kolmogorov-Arnold Networks (original paper (Liu et al., 2024) published in the arXiv on April 30 2024, currently cited 564 times.)
2. GraphCast model for AI weather forecast (original paper (Lam et al. 2023) published in Science in Nov 14 2023, currently cited 557 times.)

This proposed project (KAN4Met) aims to explore the intersection between the two fields opened by these fundamental contributions. In addition, its goal is to produce a ready-to-use ML model for weather prediction on the Iberian peninsula, in collaboration with the Spanish Weather Agency (AEMET). The project also aims to apply enhanced weather prediction models to the problem of route optimization in maritime transport, continuing the research developed by the IP of this proposal in the past three years.

<!-- Style -->
{% include head.html %}

<!-- Add this section to display the latest papers in bulletpoints -->
<!--
<h2>Latest Papers</h2>
<ul class="latest-articles-container">
  {% assign sorted_papers = site.publications | sort: 'date' | reverse %}
  {% for paper in sorted_papers limit:3 %}
    <li><a href="{{ paper.url }}">{{ paper.title }}</a></li>
  {% endfor %}
</ul>
-->

<!-- Add this section to display the chosen papers in bulletpoints -->
{% assign trending_papers = "/publications/2025/hadad,/publications/2024/hybrid-search,/publications/2023/emissions" | split: "," %}

<h2>Latest Papers</h2>
<ul class="latest-articles-container">
  {% for permalink in trending_papers %}
    {% assign paper = site.publications | where: "permalink", permalink | first %}
    <li><a href="{{ paper.url }}">{{ paper.title }}</a></li>
  {% endfor %}
</ul>

<a href="{{ site.baseurl }}/publications/" class="button">See All Publications</a>

<!-- Add this section to display the latest talks in bulletpoints -->
<h2>Latest Talks</h2>
<ul class="latest-talks-container">
  {% assign sorted_talks = site.talks | sort: 'date' | reverse %}
  {% for talk in sorted_talks limit:3 %}
    <li><a href="{{ talk.url }}">{{ talk.title }}</a></li>
  {% endfor %}
</ul>

<a href="{{ site.baseurl }}/talks/" class="button">See All Talks</a>

<!-- Add this section to display the three latest news articles horizontally -->
<!-- <h2>Latest News</h2>
<div class="latest-news-container">
  {% for post in site.posts limit:3 %}
    <div class="news-item">
      <a href="{{ post.url }}">
        <img src="{{ post.featured_image }}" alt="{{ post.title }}" style="max-width: 100%; height: auto;">
        <h3>{{ post.title }}</h3>
      </a>
    </div>
  {% endfor %}
</div>
-->

<!-- Add this section to display three chosen news articles horizontally -->
{% assign trending_posts = "/news/2024/dubai,/news/2023/european-parliament,/news/2023/wimobo" | split: "," %}

<h2>Trending News</h2>
<div class="latest-news-container">
  {% for permalink in trending_posts %}
    {% assign post = site.posts | where: "permalink", permalink | first %}
    <div class="news-item" style="position: relative;">
      <a href="{{ post.url }}">
        <img src="{{ post.featured_image }}" alt="{{ post.title }}" style="max-width: 100%; height: auto;">
        <h3>
          {% if post.abbreviated_title %}
            {{ post.abbreviated_title }}
          {% else %}
            {{ post.title }}
          {% endif %}
        </h3>
      </a>
    </div>
  {% endfor %}
</div>

<a href="{{ site.baseurl }}/news/" class="button">See All News</a>
