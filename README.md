# pplank8.github.io

Personal website and blog for [pplank8](https://pplank8.github.io/), built with Jekyll and a customized [al-folio](https://github.com/alshedivat/al-folio) theme.

## Local development

Install the Ruby dependencies and start the development server:

```bash
bundle install
bundle exec jekyll serve --livereload
```

The site will be available at <http://localhost:4000>.

## Repository layout

- `_pages/` — standalone pages
- `_posts/` — blog posts
- `_projects/` — project entries
- `_data/` — structured site data
- `_layouts/`, `_includes/`, `_sass/` — theme structure and styling
- `assets/` — images, scripts, stylesheets, and other media
- `_config.yml` — site configuration

Pushes to `main` are deployed through GitHub Actions.
