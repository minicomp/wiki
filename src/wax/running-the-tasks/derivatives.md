---
layout: default
title: 'wax:derivatives'
nav_order: 1
parent: Running the tasks
grand_parent: Wax
permalink: /wax/running-the-tasks/derivatives/
---

# wax:derivatives

There are two tasks namespaced under wax:derivatives, namely [wax:derivatives:simple](#waxderivativessimple) and [wax:derivatives:iiif](#waxderivativesiiif) which represent the two options for generating collection image derivatives. __You will only run one of these tasks per collection and you should only need to run it once.__

## wax:derivatives:simple

```sh
bundle exec rake wax:derivatives:simple YOUR_COLLECTION_NAME
```

When you run the line above for your collection, the task will:

1. Look for the directory of source images you specified in your `_config.yml` file under `collections` > `YOUR_COLLECTION_NAME` > `images` > `source` (See: [Updating your configuration]({{ '/wax/setting-up-your-site/updating-your-configuration/' | absolute_url }}))


2. Generate two copies of each image (full size and thumbnail, with 1140px and 250px widths, respectively) into the directory `img/derivatives/simple`


3. Automatically add two fields (`full` and `thumbnail`) to each of your metadata records with the relative paths to the image derivatives.


(e.g., `bundle exec rake wax:derivatives:simple qatar`)

## wax:derivatives:iiif

```sh
bundle exec rake wax:derivatives:iiif YOUR_COLLECTION_NAME
```

When you run the line above for your collection, the task will:

1. Look for the directory of source images you specified in your `_config.yml` file under `collections` > `YOUR_COLLECTION_NAME` > `images` > `source` (See: [Updating your configuration]({{ '/wax/setting-up-your-site/updating-your-configuration/' | absolute_url }}))


2. Generate many IIIF derivatives, image tiles, and JSON representations of the collection items into the directory `img/derivatives/iiif`.


3. Automatically add three fields (`full`, `thumbnail`, and `manifest`) to each of your metadata records with the relative paths to the full and thumbnail size image derivatives and the IIIF manifest.

(e.g., `bundle exec rake wax:derivatives:iiif qatar`)



## Which one should I use?

### Simple derivatives

| Pros | Cons   |
|:-----|:-------|
| Fewer files to create, manage, and host | Doesn't handle items with multiple images / pdf format |
| Loads faster on webpages | Lower quality images, no zooming |
| Users can copy/download full images | Users can copy/download full images |


### IIIF derivatives

| Pros | Cons   |
|:-----|:-------|
| Image content is __interoperable__, meaning it is standardized, (re)usable, and citable broadly (see: <https://iiif.io/community/faq/#what-is-iiif>)| Slow to generate |
| Image content can leverage embedded metadata   | Slower to load on the page than simple derivatives  |
| Can handle multiple images / paged content per collection item   | Requires the page to use a JS image viewer  |
| Offers deep zooming of full images with no loss; Images are loaded quickly relative to the high resolution offered   | Higher technical overhead, more complex |
