---
layout: default
title: 'wax:pages'
nav_order: 2
parent: Running the tasks
grand_parent: Wax
permalink: /wax/running-the-tasks/pages/
---

# wax:pages

Wax:pages is the task responsible for generating a page for each of your collection items and is the simplest task to configure and use.

You can run the task with:

## Native installation

```sh
bundle exec rake wax:pages YOUR_COLLECTION_NAME
```

## Docker installation

```sh
docker run --rm -v $PWD:/app --name wax-demo wax:1.1.0-snapshot "bundle exec rake wax:pages YOUR_COLLECTION_NAME"
```

This will:

1. Look for the metadata file you specified in your `_config.yml` file under `collections` > `YOUR_COLLECTION_NAME` > `metadata` > `source` (See: [Updating your configuration]({{ '/wax/setting-up-your-site/updating-your-configuration/' | absolute_url }}))

2. Generate a directory named after your collection prepended with an underscore (e.g., `_qatar` or `_your_collection_name`)

3. Generate pages into that directory for each record named after its `pid` value
