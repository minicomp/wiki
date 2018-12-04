---
layout: default
title: Using theme layouts
permalink: /wax/using-theme-layouts/
nav_order: 6
parent: Wax
---

# Using theme layouts

Wax five layouts for you to use and/or expand on: `wax/default.html`, `wax/page.html`, `wax/exhibit.html`, `wax/collection_item.html`, and `wax/reuse_page.html`. (See the on [Github](https://github.com/minicomp/wax/tree/gh-pages/_layouts/wax).)

You can tell a page to use a layout by adding it to the page's [front-matter](https://jekyllrb.com/docs/front-matter/), for example:

__.__ `_exhibits/my-exhibit.md`

```markdown
---
title: 'My Exhibit'
layout: wax/exhibit
---
```

Or you can make your own layout file that *inherits* from a Wax layout, for example the `qatar_item.html` layout which inherits from `wax/collection_item`:

__.__ `_layouts/qatar_item.html`

```markdown
---
layout: wax/collection_item
image_viewer: 'leaflet'
pagination: true
meta:
  - label: 'Object Label'
    value: page.label
  - label: 'Artist'
    value: page.artist
  - label: 'Object Type'
    value: page.object_type
  - label: 'Location'
    value: page.location
  - label: 'Current Location'
    value: page.current_location
  - label: 'Date'
    value: page.\_date
  - label: 'Source'
    value: page.source
---
```
