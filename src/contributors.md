---
layout: default
title: Contributors
nav_order: 2
---

# Contributors

The following list is a start towards the [all-contributors specification](https://github.com/kentcdodds/all-contributors) using  [emoji key](https://github.com/kentcdodds/all-contributors#emoji-key). __Want to be added to this list?__ Make a GitHub [issue](https://github.com/minicomp/wiki/issues)!


<div class='contributors'>
  {% for contributor in site.data.contributors %}
    {% assign user = contributor.github_username %}
    <div class='contributor'>
      <a href="https://github.com/{{ user }}">
        <img alt="github avatar for @{{ user }}" src="https://github.com/{{ user }}.png"/>
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
