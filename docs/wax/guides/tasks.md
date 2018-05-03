[![logo](../../logo.png)](/)

# Using Wax Tasks


### Setup

If you haven't already done so, clone the [Wax Demo site](https://minicomp.github.io/wax/) onto your machine:

```bash
$ git clone https://github.com/minicomp/wax.git
$ cd wax
$ bundle install
```

Serve it locally by running:

```bash
$ bundle exec jekyll serve
```

and navigating to `localhost:4000/wax/` in your browser.

<a href="/wax/wax_still.png"><img src="/wax/wax_still.png" width="600" style="border:1px grey solid;margin: 30px 0 30px 0;"/></a>

Open the files in a text editor like [Atom](https://atom.io/): `$ atom .`

<a href="/wax/wax_dir.png"><img src="/wax/wax_dir.png" width="600" style="margin: 30px 0 30px 0;"/></a>

### Test with current data

Test out a few Rake tasks (from `wax_tasks`) on the current data by deleting the `_qatar` and `iiif` directories:

```bash
$ rm -rf _qatar
$ rm -rf iiif
```

Then regenerate the collection pages:
```bash
$ bundle exec rake wax:pagemaster qatar
```

Regenerate the collection IIIF derivatives:
```bash
$ bundle exec rake wax:iiif qatar
```

And regenerate the Elasticlunr search index:
```bash
$ bundle exec rake wax:lunr
```

You should see:

<img src="/wax/pm_screen.png" style="margin: 0 0 30px 0;"/>

### Test with your own data
