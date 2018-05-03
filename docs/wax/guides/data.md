[![logo](../../logo.png)](/)

# Pre-preparing your Data and Metadata

I.e., the step before **'start'** below

<a href="/wax/wax_workflow.jpeg"><img src="/wax/wax_workflow.jpeg" style="border:1px grey solid;margin:30px 0 30px 0;"/></a>

### Expectations

1. Wax expects **collection metadata as key-value records** and assumes your **data are image files**.

2. **Each collection must have one metadata file** This file can be csv, or it can be a json or yaml array. (The extension must be `.csv`, `.json`, or `.yml`)

3. **Each record must have a unique `pid`** with no spaces or special characters. **An image's filename** (without the extension e.g., `.jpeg` or `.tiff`) **must exactly match its record's `pid`.**

4. **The metadata keys/headers** (e.g., `title`, `creator`, `location`, etc.) **cannot have spaces or special characters**. When applicable, use [snake case](https://en.wikipedia.org/wiki/Snake_case) and `keep_it_simple`.

5. Each record *should* have a `title` field in addition to `pid`, but it is not necessarily required.

> The `pids` and filenames are all that tie the image and its record together, so make sure they're exactly right!

### Gotchas

Because Jekyll will process and convert each to HTML, **we have to watch out for fields Jekyll already uses**, especially `id` and `date`. Make sure to rename these fields in your metadata file (e.g., `_date`).

### Tips

> __Best tip:__ try [OpenRefine](http://openrefine.org/)! Faceting and normalizing your data ahead of time (by **finding errant spaces, empty fields, typos**) will make building your site much easier. It is also **best practice to clean your raw data** than to bandaid-over it on presentation.

### Next:

> [Using Wax Tasks](/wax/guides/tasks#top)
