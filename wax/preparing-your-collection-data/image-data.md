---
layout: default
title: Directory of image files
nav_order: 2
parent: Preparing your collection data
grand_parent: Wax
permalink: /wax/preparing-your-collection-data/image-data/
---

# Directory of Image Files

Wax accepts `.tiff`, `.jpeg`, `.png`, and `.pdf` files and assumes relatively high resolution. For best results, resolution should be as standard as possible across the collection.

## Requirements

For Wax to work, __each source image file must be named to match its__ `pid` __in the metadata exactly.__ (See: the [Metadata guide]({{ '/wax/preparing-your-collection-data/metadata/' | absolute_url }})).

For example, say the `pid` for your record in the metadata is `obj45` and that it represents a single jpeg image. You'd name your source image `obj45.jpeg`.

If another item, e.g., `obj46` represents a pdf document, you'd name its source file `obj46.pdf`. And lastly, if theres an item `obj47` representing a group of images, you'd make a sub directory called `obj47` and fill it with source images, e.g., `recto.jpg` and `verso.jpg`.


<img src="{{ '/assets/image-files.png' | absolute_url }}" style="border: 1px grey solid;margin: 1rem 0 1rem 0;" alt="image files"/>
