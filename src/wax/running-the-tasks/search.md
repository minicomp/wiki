---
layout: default
title: 'wax:search'
nav_order: 3
parent: Running the tasks
grand_parent: Wax
permalink: /wax/running-the-tasks/search/
---

# wax:search

Wax:search is the task responsible for generating a search index for your site to use.

You can run the task with:

```sh
bundle exec rake wax:search SEARCH_NAME
```

This will:

1. Look for the `search` configuration you set up in your `_config.yml` file. (See: [Updating your configuration]({{ '/wax/setting-up-your-site/updating-your-configuration/' | absolute_url }})), and find the one with `SEARCH_NAME`, .e.g. `main`.

2. For each collection you gave the `search`, it will look for the markdown pages and add the `fields` and/or `content` from each page to the index.

3. It will write the index as a JSON file to the filename you gave (`index`).
