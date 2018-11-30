---
layout: default
title: 'wax:pagemaster'
nav_order: 2
parent: Running the tasks
grand_parent: Wax
permalink: /wax/running-the-tasks/pagemaster/
---

# wax:pagemaster

Wax:pagemaster is the task responsible for generating a page for each of your collection items and is the simplest task to configure and use.

You can run the task with:

```sh
bundle exec rake wax:pagemaster YOUR_COLLECTION_NAME
```

This will:

1. Look for the metadata file you specified in your `_config.yml` file under `collections` > `YOUR_COLLECTION_NAME` > `metadata` > `source` (See: [Updating your configuration]({{ '/setting-up-your-site/updating-your-configuration/' | absolute_url }}))

2. Generate a directory named after your collection prepended with an underscore (e.g., `_qatar` or `_your_collectio_name`)

3. Generate pages into that directory for each record named after its `pid` value
