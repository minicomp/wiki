---
layout: default
title: Running the tasks
nav_order: 5
has_children: true
parent: Wax
permalink: /wax/running-the-tasks/
---

# Running the main tasks

__The order in which you run the following rake tasks is important!__ For example, the  `derivatives` tasks give information to the metadata file, so it needs to be run before the `pages` task generates pages from the metadata. And the `search` task indexes the collection markdown pages, so those pages need to exist before it is run.

### Step 1: Make sure you have the tasks available.

You can check by running `bundle exec rake --tasks`. You should see a list of tasks printed in your shell window.

### Step 2: Generate the image derivatives for your collection from the source images.

You'll do this by running one of the [wax:derivatives tasks]({{ '/wax/running-the-tasks/derivatives/' | absolute_url }}).

### Step 3: Generate the collection pages from the metadata records.

You'll do this by running the [wax:pages task]({{ '/wax/running-the-tasks/pages/' | absolute_url }}).

### Step 4: Generate the search index.

You'll do this by running the [wax:search task]({{ '/wax/running-the-tasks/search/' | absolute_url }}).
