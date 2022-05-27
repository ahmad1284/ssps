---
layout: base.html
title: Suza Student Project Showcase
metaDescription:
  Suza Student Project Showcase is a place for sharing projects and inspiring the next generation of students.
templateEngineOverride: njk
---

<ul class="grid">
  {% for key, profile in profiles %}
    <li class=""grid__item>
      <div class="grid__itemImgWrapper">
        <img src="/images/{{ key }}.jpeg" alt="{{ profile.name }}" />
      </div>
      <h2 class="grid__itemName">{{ profile.name }}</h2>
      <p class="grid__itemBio">{{ profile.bio }}</p>
      <div class="grid__itemSocials">
      {% if profile.twitterUsername.length > 0 %}
        <a href="https://twitter.com/{{ profile.twitterUsername }}" target="_blank">TWITTER</a>
      {% endif %}
      {% if profile.githubUsername.length > 0 %}
        <a href="https://github.com/{{ profile.githubUsername }}" target="_blank">GITHUB</a>
      {% endif %}
      {% if profile.website.length > 0 %}
        <a href="{{ profile.website }}" target="_blank">WEBSITE</a>
      {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>