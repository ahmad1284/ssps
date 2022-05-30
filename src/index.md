---
layout: base.html
title: SuzaStudent Project Showcase
metaDescription:
  Suza Project Showcase is a place for sharing projects and inspiring the next generation of students.
templateEngineOverride: njk
---
<section class="hero">
  <div class=""hero__content>
    <h1 class="hero__contentHeadline">Suza Project Showcase</h1>
    <p class="hero__contentByLine">Inspiring the next generation of students by being catalysts for social change
    </p>
    <div class="hero__buttons">
      <a href="https://github.com/ahmad1284/ssps#readme" target="_blank"
      class="hero__button"
      >Add your profile</a>
      <a href="https://suza.ac.tz" target="_blank" class="hero__button hero__button--alt">Visit suza</a>
    </div>
  </div>
</section>

<section>
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
</section>