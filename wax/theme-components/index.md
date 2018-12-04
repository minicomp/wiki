---
layout: default
title: Using theme components
permalink: /wax/using-theme-components/
nav_order: 7
parent: Wax
---

# Using theme components

In the parlance of Jekyll, components are called `includes` and live in the `_includes` folder. They are just like __shortcodes__ in WordPress in that they're quick, reusable blocks.

__Wax__ comes with a lot of `includes` that you can browse on Github [here](https://github.com/minicomp/wax/tree/gh-pages/_includes/wax). The easiest way to get started using Wax `includes` is by seeing how they're used in the [Wax demo site](https://github.com/minicomp/wax/tree/gh-pages/) and trying them out on your own.

## includes

[wax/footer.html](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/footer.html), [wax/head.html](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/head.html), and [wax/header.html](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/header.html) are used by the `wax/default.html` layout, so you likely won't need to use them on your own. The rest are covered below.

### wax/inline-image.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/inline_image.html)


#### Usage:

{% raw %}
  `{% include wax/inline_image.html collection=[item collection key] pid=[item pid] %}`
{% endraw %}

### wax/mirador_compare.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/mirador_compare.html)

#### Usage:

{% raw %}
  `{% include wax/mirador_compare.html m1=[link to manifest 1] m2=[link to manifest 2] %}`
{% endraw %}

### wax/parallax.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/parallax.html)

#### Usage:

{% raw %}
  `{% include wax/parallax.html collection=[item collection key] pid=[item pid] %}`
{% endraw %}

---

### wax/collection/gallery.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/collection/gallery.html)

#### Usage:

{% raw %}
  `{% include wax/collection/gallery.html collection=[collection key] facet_by=[key to group items by] %}`
{% endraw %}

### wax/collection/interactive_metadata.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/collection/interactive_metadata.html)

#### Usage:

{% raw %}
  `{% include wax/collection/interactive_metadata.html collection=[collection key] %}`
{% endraw %}

---


### wax/image_viewer/leaflet.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/image_viewer/leaflet.html)

#### Usage:

{% raw %}
  `{% include wax/image_viewer/leaflet.html collection=[item collection key] pid=[item pid] %}`
{% endraw %}

### wax/image_viewer/mirador.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/image_viewer/mirador.html)

#### Usage:

{% raw %}
  `{% include wax/image_viewer/mirador.html collection=[item collection key] pid=[item pid] %}`
{% endraw %}

### wax/image_viewer/simple.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/image_viewer/simple.html)

#### Usage:

{% raw %}
  `{% include wax/image_viewer/simple.html collection=[item collection key] pid=[item pid] %}`
{% endraw %}

---


### wax/item/metadata.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/item/metadata.html)

#### Usage:

{% raw %}
  `{% include item/metadata.html %}`
{% endraw %}

### wax/item/pagination.html [→](https://github.com/minicomp/wax/blob/gh-pages/_includes/wax/item/pagination.html)

#### Usage:

{% raw %}
  `{% include wax/item/pagination.html meta=[metadata structure label/value] %}`
{% endraw %}
