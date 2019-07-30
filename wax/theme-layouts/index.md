---
layout: default
title: Using theme layouts
permalink: /wax/using-theme-layouts/
nav_order: 6
parent: Wax
---

# Using theme layouts

Wax five layouts for you to use and/or expand on: `wax/default.html`, `wax/page.html`, `wax/exhibit.html`, `wax/collection_item.html`, and `wax/reuse_page.html`. (See them on [Github](https://github.com/minicomp/wax/tree/master/_layouts).)

You can tell a page to use a layout by adding it to the page's [front-matter](https://jekyllrb.com/docs/front-matter/), for example:

__.__ `_exhibits/my-exhibit.md`

```markdown
---
title: 'My Exhibit'
layout: wax/exhibit
---
```

Or you can make your own layout file that *inherits* from a Wax layout, for example the `qatar_item.html` layout which inherits from `generic_collection_item.html`:

__.__ `_layouts/qatar_item.html`

```markdown
---
layout: generic_collection_item.html
image_viewer: 'openseadragon'
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
