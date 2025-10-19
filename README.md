# babs.github.io

Personal project portfolio site built with Hugo and deployed via GitHub Actions.

## Stack

- **Framework**: Hugo (v0.139.4 Extended)
- **Theme**: [Hextra](https://github.com/imfing/hextra)
- **Deployment**: GitHub Actions → GitHub Pages
- **URL**: https://babs.github.io/

## Local Development

```bash
# Install Hugo Extended v0.139.4+
# https://gohugo.io/installation/

# Fetch theme module
hugo mod get

# Run dev server
hugo server -D

# Build
hugo --gc --minify
```

## Deployment

Automatic deployment on push to `master` branch via `.github/workflows/hugo.yml`

## Structure

```
content/        # Markdown content
layouts/        # Custom Hugo layouts
static/         # Static assets
hugo.yaml       # Hugo configuration
```

## Content Management

Edit markdown files in `content/` directory. Site automatically rebuilds and deploys on push to master.
