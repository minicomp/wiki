---
layout: default
title: Serving your site
nav_order: 8
parent: Wax
permalink: /wax/serving/
---

# {{ page.title }}

## Serving locally for development

If you're running Wax directly on your machine, serving
\*should\* be as simple as

```sh
bundle exec jekyll serve
```

If you're in a Docker container, you'll need to specify the host:

```sh
bundle exec jekyll serve --host 0.0.0.0
```

## Hosting / publishing online

There are many options. Our demo uses GitHub pages. You can also use FTP deployment to a server or sync files to an S3 or Min.io bucket.

Have you used these options and would like to share a "recipe" for our Wiki? Please ping us on the [Code4Lib Slack](https://docs.google.com/forms/d/e/1FAIpQLSeD77mBp0Y13mFePF8UmDwFrlbxNx3VttEjz_3dgglJeK-Zbg/viewform?c=0&w=1)!

### With GitHub Pages

If you have a wax site repository that you want to publish to GitHub pages:

1. Go to your repository page on Github.
2. Go to "Settings" > "Pages".
3. Under "Source", select the "main" branch and "root" folder and click "Save".
4. The page should now say something like "Your site is published at **https://my-username.github.io/my-repo-name**". In this example, `https://my-username.github.io` is the URL and `/my-repo-name` is the BASEURL.
5. Open your `_config.yml` file.
6. Replace the `url` field with your own url, e.g.,  `https://my-username.github.io`. This should NOT have a slash at the end.
7. Replace the baseurl with your own baseurl, which will be the same as your repository name, e.g., `/my-repo-name`. This MUST start with a slash.
8. Add, commit, and push your changes.
9. After waiting and refreshing as needed, your site should be published at your complete URL, e.g., `https://my-username.github.io/my-repo-name`.

If you have issues or questions, refer to the [GitHub Pages Documentation](https://docs.github.com/en/pages).
