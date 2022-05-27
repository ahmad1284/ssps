---
layout: base.html
title: Suza Student Project Showcase
metaDescription:
  Suza Student Project Showcase is a place for sharing projects and inspiring the next generation of students.
templateEngineOverride: njk
---

<ul>
  {% for key, profile in profiles %}
    <li>
      <div>
        <h2>{{ profile.name }}</h2>
        <p>{{ profile.bio }}</p>
        <a href="https://twitter.com/{{ profile.twitterUsername }}" target="_blank">TWITTER</a>
        <a href="https://github.com/{{ profile.githubUsername }}" target="_blank">GITHUB</a>
        <a href="{{ profile.website }}" target="_blank">WEBSITE</a>
      </div>
    </li>
    {% endfor %}
</ul>