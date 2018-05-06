[![logo](./../../assets/logo.png)](/)

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

![wax_still](./../../assets/wax_still.png#border-img)

Open the files in a text editor like [Atom](https://atom.io/): `$ atom .`

![wax_dir](./../../assets/wax_dir.png#border-img)

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

![pm_screen](./../../assets/pm_screen.png#border-img)

### Test with your own data
