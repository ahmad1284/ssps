---
layout: base.html
title: SuzaStudent Project Showcase
metaDescription:
  Suza Student Project Showcase is a place for sharing projects and inspiring the next generation of students.
templateEngineOverride: njk
---

<ul class="profiles">
 {% for key, profile in profiles %}
    <li class="profiles__item">
      <span class="profiles__itemImgWrapper">
        <img src="/images/{{ key }}.jpeg" alt="{{ profile.name }}" />
      </span>
      <span class="profiles__itemTextWrapper">
        <h2 class="profiles__itemName">{{ profile.name }}</h2>
        <p class="profiles__itemBio">{{ profile.bio }}</p>
        <p class="profiles__itemCourse">{{ profile.course}}</p>
        <span class="profiles__itemSocials">
          {% if profile.twitterUsername.length > 0 %}
            <a href="https://twitter.com/{{ profile.twitterUsername }}" 
              target="_blank" 
              title="{{ profile.name }} on Twitter">
              {% include "svg/twitter.svg" %}
            </a>
          {% endif %}
          {% if profile.githubUsername.length > 0 %}
            <a href="https://github.com/{{ profile.githubUsername }}" 
            target="_blank"
            title="{{ profile.name }} on Github">
               {% include "svg/github.svg" %}
            </a>
          {% endif %}
          {% if profile.website.length > 0 %}
            <a href="{{ profile.website }}" 
              target="_blank" title="{{ profile.name }}'s Website">
               {% include "svg/globe.svg" %}
            </a>
          {% endif %}
        </span>
      </span>
    </li>
  {% endfor %}
</ul>