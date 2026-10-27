# bipinlekhak.com.np

Personal academic website of Bipin Lekhak, served by GitHub Pages from the `master` branch at
<https://bipinlekhak.com.np> (`CNAME`). GitHub Pages builds it with Jekyll; there is no theme, and
every page uses `_layouts/default.html` and `assets/css/site.css`.

## Updating

| To change | Edit |
|---|---|
| Publications | `_data/publications.yml` (the site owner's name is bolded automatically) |
| News | `_data/news.yml`, newest first |
| Bio, research, experience | `index.html` |
| CV | Replace `assets/cv/Bipin_Lekhak_CV.pdf` with the PDF built from the Overleaf CV repo |
| Portrait | Add an image under `assets/img/` and set `photo:` in `_config.yml` |

## Archive

Old reading notes live in `_posts/` and keep their original URLs (`/paper/...`, `/books/...`).
They are listed only on `/archive/`, which nothing on the site links to, and they are kept out
of the sitemap and marked `noindex`. They use MathJax: `$...$` inline and `$$...$$` for display.

## Local preview

With Ruby and Bundler:

```console
bundle install
bundle exec jekyll serve
```

Or in a container, without installing Ruby:

```console
podman run --rm -it -p 4000:4000 -v "$PWD":/site:Z -w /site docker.io/library/ruby:3.3 \
  bash -c 'gem install --no-document github-pages webrick && jekyll serve --host 0.0.0.0'
```
