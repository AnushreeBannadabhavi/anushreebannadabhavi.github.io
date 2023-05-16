---
layout: default
title: Hikes
---

<style>
    .hike-list {
      display: flex;
      flex-wrap: wrap;
    }

    .hike {
      width: 50%;
      padding: 10px;
    }

    .hike-image {
      width: 100%;
    }

    .hike-image img {
      width: 100%;
      height: auto;
    }

    .hike-details {
      padding: 10px;
    }
</style>

<div class="hike-list">
  {% for hike in site.data.hikes %}
  <div class="hike">
    <a href="{{ hike.url }}">
      <div class="hike-image">
          <img src="{{ hike.image | absolute_url }}" alt="hike Image">
      </div>
      <div class="hike-details">
        <h2>{{ hike.name }}</h2>
        <p>{{ hike.description }}</p>
      </div>
    </a>
  </div>
  {% endfor %}
</div>
