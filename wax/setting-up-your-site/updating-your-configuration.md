---
layout: default
title: Updating your configuration
nav_order: 3
parent: Setting up your site
grand_parent: Wax
permalink: /wax/setting-up-your-site/updating-your-configuration/
---

# Updating your configuration

Below you'll find explanations for the wax demo site configuration and instructions for you to update it for your own exhibition site.

## Main settings

The main settings are direct from Jekyll. You can learn more through their [configuration guides](https://jekyllrb.com/docs/configuration/).

```yml

title:            'Minicomp/Wax'
description:      'Minimal Exhibitions with Jekyll'
url:              ''
baseurl:          '/wax'
copyright:        'Example copyright org, 2018'

```

## Collection settings

Wax leverages [Jekyll collections](https://jekyllrb.com/docs/collections/) for much of its
functionality, therefore some of the keys below are from
Jekyll while others are Wax-specific.

Below, two collections `exhibits` and `qatar` are configured. They control files in `_exhibits` and `_qatar` respectively. `exhibits` contains regular Markdown essays, so it only needs `output: true` in its config. But `qatar` is a Wax image collection and needs more info to be processed:

```yml
collections:
  exhibits:
    output: true
  qatar:
    output: true
    layout: 'qatar_item'
    metadata:
      source: 'qatar.csv' # path to the metadata file within `_data`
    images:
      source: 'raw_images/qatar' # path to the directory of images within `_data`

```

| variable | type accepted | description | used by  |
|:---------|:--------------|:------------|:---------|
| `collections` | hash | the site collections | wax and jekyll |
| `output` | true/false | whether or not to output the collection to HTML. | jekyll |
| `layout` | string | which layout in `_layouts` the collection pages should use. you should create this file in `_layouts` and it should use the `wax/collection_item` layout. __note:__ you do not add the `.html` extension at the end; this is a Jekyll convention. | wax and jekyll |
| `metadata:source` | string | path to the collection's metadata file within the `_data` directory | wax |
| `images:source` | string | path to the collection's directory of images within the `_data` directory  | wax |

There are more configuration variables for collections within `metadata` and `images` for [advanced use cases]({{ '/wax/advanced/' | absolute_url }}).

# Search settings

The `lunr_index` variable can create multiple indexes (the dash represents an item in a list in YAML), though one is recommended. For Wax to use search it needs two files: a JSON search index and a javascript search UI to search for and display results. Both can be created by Wax using the [lunr task]({{ '/wax/running-the-tasks/lunr/' | absolute_url }}) and the information below.

```yml

lunr_index:
  - file: 'js/lunr-index.json' # file the index will get written to
    ui:   'js/lunr-ui.js' # path to the search UI file
    collections:
      qatar:
        content: false # whether or not to index page content
        fields: # the metadata fields to index
          - artist
          - location
          - label
          - _date
          - object_type
          - current_location
```

| variable      | type accepted | description | used by  |
|:--------------|:--------------|:------------|:---------|
| `lunr_index`  | list | list of search indexes | wax |
| `file`        | string | the path (within the root of the site) to write the index to | wax |
| `ui`          | string | the path (within the root of the site) to write the UI to | wax |
| `collections` | hash   | which collections (as defined in `collections` above) to index | wax |
| `content`     | true/false | within a collection: whether or not to index the page content in addition to the metadata in the front matter | wax |
| `fields`      | list | within a collection: the metadata fields to index | wax |

## Menu settings

The `menu` defined in `_config.yml` is used by the theme's header and can accept nested / dropdown menus.

```yml
menu:
  - label: 'About'
    sub:
      - label: 'Wax'
        link: '/about/'
      - label: 'Documentation'
        link: 'https://minicomp.github.io/wiki/#/wax/'
      - label: 'Credits'
        link: '/credits/'
  - label: 'Exhibits'
    sub:
      - label: 'Local and Remote IIIF Manifests'
        link: '/exhibits/a/'
      - label: 'Inline Parallax Image'
        link: '/exhibits/b/'
      - label: 'Inline Image References'
        link: '/exhibits/c/'
  - label: 'Browse'
    link: '/collection/'
  - label: 'Search'
    link: '/search/'
  - label: 'Reuse'
    link: '/reuse/'
```

| variable      | type accepted | description | used by  |
|:--------------|:--------------|:------------|:---------|
| `menu` | list | list of menu items | wax |
| `label` | string | the human-readable label for the link or dropdown | wax |
| `link` | string | the relative (internal) or absolute (external) link | wax |
| `sub` | list | a list of sub items for a dropdown | wax |

## Footer settings

The theme's footer uses the site's title, description, and copyright by default and optionally takes a list of navigation links and logos from the variables below.

```yml
footer:
  links:
    - label: 'GitHub'
      link: 'https://github.com/minicomp/wax'
    - label: 'Credits'
      link: '/credits'
    - label: 'Contact'
      link: 'https://gitter.im/minicomp/wax/'
  logos:
    - img: '/assets/logo.png'
    - img: 'https://example.com/logo.png'
      link: 'https://example.com'
```
