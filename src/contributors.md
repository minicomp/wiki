---
layout: default
title: Contributors
nav_order: 2
---

# Contributors

The following list is pulled from the GitHub API and collects contributions from across the [Minicomp](https://github.com/minicomp) repositories. It takes a village to care for an open source project, and the whole village deserves credit!


<style>
  .contributors {
    display: flex;
    flex-wrap: wrap;
  }
  .contributor  {
    flex: auto;
    max-width: 12.5%;
    margin-right: 2rem;
    margin-bottom: 2rem;
  }
  .contributor p.info {
    font-size: .7em;
    line-height: 1em;
    padding: 0;
    margin: 0;
  }
  .contributor img {
    margin: 0 auto;
  }
</style>

<div class="contributors">
  {% for c in site.data.contributors %}
  {% assign user  =  c[0] %}
  {% assign img   = c[1].avatar_url %}
  {% assign count = c[1].contributions %}
  <div class="contributor">
    <a href="https://github.com/{{ user }}">
      <img src="{{ img }}?v=3?s=100" width="100px;" alt="github avatar for @{{ user }}"/><br>
      <p class="info">
        @{{ user }}<br>
        commits: {{ count }}
      </p>
    </a>
  </div>
  {% endfor %}
</div>
