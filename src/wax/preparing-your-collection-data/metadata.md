---
layout: default
title: Metadata file
nav_order: 1
parent: Preparing your collection data
grand_parent: Wax
permalink: /wax/preparing-your-collection-data/metadata/
---

# Metadata file
{: .no_toc }

## Table of Contents
{: .no_toc }

1. TOC
{:toc}


#### \***Warning!** We highly discourage using Microsoft Excel for working with your metadata! It regularly causes encoding errors. Google Sheets is a good alternative for this work.
{: .no_toc }

## Example

Wax can work with __CSV__, __JSON__, and __YAML__ files, though CSVs are recommended. Below is the CSV spreadsheet that powers the `qatar` collection in the [Wax demo site](https://minicomp.github.io/wax/).

<br>

{% include sample-data-table.html %}

<br>

## Column heading / key rules

CSV Spreadsheet column heading names (or JSON or YAML keys) should:

- Avoid whitespace
- Avoid special characters except underscores
- Be lowercase

E.g.,  the heading `Current Location, City` should be replaced with `current_location_city`. You can change how this will display on your site later!

## Required fields

Each record (i.e., spreadsheet row or JSON object) needs two fields:

### pid

  - This is the Persistent ID for your collection item.
  - It cannot have whitespace!
  - It must be unique: no two records can have the same `pid`!
  - It is highly encouraged to use **the simplest pid values possible** and follow "snake case", where letters are lowercase and special characters are removed or replaced by underscores.
  - E.g. `Object Ref #1` will break. You could simplify it to `obj1` instead (like in the example spreadsheet above).

### label
  - This is where you succinctly describe the item.
  - It will show in results and at the top of the item page, e.g.: [Portrait of Hasan 'Ali Mirza Shuja al-Saltana](https://minicomp.github.io/wax/qatar/obj10/)
  - It does not have to be unique.

#### \***TIP:** keep your `pid` values as simple and arbitrary as possible and use `label` to keep track of what's what instead!
{: .no_toc }

## Fields to avoid

__Some fields are needed for the underlying software of Jekyll and Wax, and should not be used in your metadata file__. You should not manually create these fields (unless you know what you're doing!), and should avoid these keys in your metadata:

- `id` (use `pid` instead)
- `date` (use `_date` instead)
- `tags` (use `_tags` instead)
- `collection` (wax will generate this)
- `thumbnail` (wax will generate this)
- `full` (wax will generate this)
- `manifest` (wax will generate this)

Everything else should be fair game!

## Troubleshooting

- To normalize and validate your metadata records, try [Open Refine](https://openrefine.org/). You can facet fields and make sure there aren't hidden spaces or sneaky typos in your values.

- When you are ready to export your metadata file, save it as your collection name in its simplest form, for example `documents.csv`, `items.json`, `frick.yml`. This will make your job easier later.

- If you are exporting from a graphical program (e.g., Google Sheets), make sure you export using UTF-8!
