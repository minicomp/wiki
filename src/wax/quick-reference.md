---
layout: default
title: Quick reference
nav_order: 11
parent: Wax
permalink: /wax/quick-reference/
---

# Quick reference
For folks who have done this before or are experienced devs:

1. Clone [the demo](https://github.com/minicomp/wax/).
2. Run `bundle install` to install dependencies.
3. Delete the demo-specific collection files and directories (i.e., `_data/raw_images/qatar`, `_data/qatar.csv`, `img/derivatives` and `_qatar`).
4. Change `_layouts/qatar-item.html` to a layout for your collection.
5. Swap in your own directory of images and metadata file for each collection.
6. Add your collection(s) to `_config.yml` (referencing your new layout), set up your `search` config, change site `title`, `url`, `baseurl`, etc.
7. Run `bundle exec rake wax:derivatives:iiif <collection-name>` OR `bundle exec rake wax:derivatives:simple <collection-name>` to generate image derivatives and add their paths to your metadata file.
8. Run `bundle exec rake wax:pages <collection-name>` to generate the collection item pages.
9. Run `bundle exec rake wax:search main` to generate the Elasticlunr.js search index.
10. Run `bundle exec jekyll serve` to preview your site in progress.
11. Adjust the menu settings in `_config.yml`, update the content on the pages, change the metadata for your collection pages, and so on until your site is ready.
12. Push the site to a new repository of your own and, if desired, enable GitHub pages.


## Links

- [Get help and/or chat on Gitter](https://gitter.im/minicomp/wax/)
- [Submit formal issues](https://github.com/minicomp/wax/issues/)
- [Jekyll documentation](https://jekyllrb.com/docs/)
