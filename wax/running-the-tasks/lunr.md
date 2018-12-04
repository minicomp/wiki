---
layout: default
title: 'wax:lunr'
nav_order: 3
parent: Running the tasks
grand_parent: Wax
permalink: /wax/running-the-tasks/lunr/
---

# wax:lunr

Wax:lunr is the task responsible for generating a search index for your site to use.

You can run the task with:

```sh
bundle exec rake wax:lunr
```

This will:

1. Look for the `lunr_index` configuration you set up in your `_config.yml` file. (See: [Updating your configuration]({{ '/wax/setting-up-your-site/updating-your-configuration/' | absolute_url }}))

2. For each collection you gave the `lunr_index`, it will look for the markdown pages and add the `fields` and/or `content` from each page to the index.

3. It will write the index to the filename you gave (`file`).


## With default UI


Instead of manually writing your own search UI Javascript file, you can optionally tell `wax:lunr` to write one for you by running the task with `UI=true`:

```sh
bundle exec rake wax:lunr UI=true
```

This will:

1. Generate the search index (see above)

2. Genereate a default UI Javascript file to the filename you gave (`ui`) in your `lunr_index` config.
