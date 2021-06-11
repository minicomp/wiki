---
layout: default
title: Directory of image files
nav_order: 2
parent: Preparing your collection data
grand_parent: Wax
permalink: /wax/preparing-your-collection-data/image-data/
---

# {{ page.title }}
{: .no_toc }

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

Wax accepts `.tiff`, `.jpeg`, `.png`, and `.pdf` files and assumes relatively high resolution. For best results, resolution should be as standard as possible across the collection.

## Naming your files

For Wax to work, __each source image file must be named to match its__ `pid` __in the metadata exactly.__ (See: the [Metadata guide]({{ '/wax/preparing-your-collection-data/metadata/' | absolute_url }})).

<img src="{{ '/assets/image-files.png' | absolute_url }}" style="border: 1px grey solid;margin: 1rem 0 1rem 0;" alt="image files"/>

### Single image item

Say you have a collection item comprising one jpeg image that corresponds with the `pid` value `obj45` in your metadata file. You'd name this source image `obj45.jpeg`.

### PDF item

If another item with `pid` `obj46` in your metadata represents a pdf document, you'd name that source file `obj46.pdf`.


### Multi-image item

If you have an item with `pid` `obj47` representing a group of images, you'd make a sub folder called `obj47` and fill it with source images, e.g., `recto.jpg` and `verso.jpg`.

#### \***Note:** If the order of the images is important for your multi-image item, name each image in order, e.g., `00.jpg`, `01.jpg`, `02.jpg`, etc.
{: .no_toc }
