---
layout: default
title: Contributors
nav_order: 2
---

# Contributors

The following list is a start towards the [all-contributors specification](https://github.com/kentcdodds/all-contributors) using  [emoji key](https://github.com/kentcdodds/all-contributors#emoji-key).


<div class='contributors'>
  {% for contributor in site.data.contributors %}
    {% assign user = contributor.github_username %}
    <div class='contributor'>
      <a href="https://github.com/{{ user }}">
        <img src="https://github.com/{{ user }}.png"/>
        <p>
          {{ user }}<br>
          {{ contributor.icons }}
        </p>
      </a>
    </div>
  {% endfor %}
</div>

### Contribute

Check back for forthcoming contributing guides.
